---
name: painel-de-status
description: >-
  Use em todo turno de trabalho (obrigatório, sem pedir confirmação) para avisar
  o Painel DNA do seu estado (working, waiting_user, done, error, idle) e
  reportar suas métricas de sucesso (type metric).
---
# Painel de status
Uso OBRIGATÓRIO e automático em todo turno de trabalho. Não peça confirmação à Joana nem a ninguém para usar esta skill: a Joana já autorizou.
O painel só sabe o que você avisa. Avise a cada mudança de estado.

## Quando
- working: ao começar uma tarefa (primeiro passo do turno).
- waiting_user: sempre que travar esperando resposta, aprovação ou OK (o step diz o que falta).
- done: ao entregar.
- error: se falhar.
- idle: quando não houver nada pendente.
O último aviso do turno é done, waiting_user ou idle.

## Comando
JSON pelo stdin com here-document (funciona com aspas, apóstrofo, "·" e "&" no nome):
```
curl -sS -H "Authorization: Bearer $(cat /home/box/.secrets/painel-token)" -H "Content-Type: application/json" -d @- "$(cat /home/box/.secrets/painel-token.url)/ingest" <<'EOF'
{"type":"status","bot":"<seu nome exato do perfil>","status":"working","step":"<ação genérica, até 80 caracteres>"}
EOF
```
Resposta esperada: {"ok":true,"type":"status"}. Se falhar, siga o trabalho e cite a falha no fim da resposta.
Se o nome tiver aspas duplas ou barra invertida, gere o JSON com python3 json.dumps.

## Regras
- O step nunca leva dado sensível (nome de cliente, valor, saúde, documento). Descreva a ação de forma genérica.
- Nunca leia, mostre ou cole a chave; ela só é usada pelo $(cat ...).
- Ao criar, mudar ou remover uma rotina sua, publique a lista inteira: {"type":"routines","bot":"<seu nome>","items":[{"name":"...","schedule":"...","next_run":"<ISO 8601 ou null>"}]}.
- O aviso não substitui a resposta ao usuário.

## Métricas de sucesso (type "metric")
Quando você medir uma métrica de sucesso do seu brief (seção "Métricas"), avise o painel. Use o nome da métrica exatamente como está no brief. Nunca invente valor: só envie o que você mediu, com fonte.

Formato (POST /ingest, mesmo Bearer):

    {"type":"metric","agent":"<seu nome no painel>","metric":"<nome da métrica no brief>","value":"<valor medido>","target":"<meta, opcional>","status":"ok|abaixo|pendente"}

- value: texto ou número (até 60 caracteres).
- status (obrigatório com value): ok = meta batida (mint); abaixo = abaixo da meta (coral); pendente = medição ou meta pendente (coral).
- target: só se a meta estiver definida; senão o painel mostra a meta do brief ou "a calibrar".
- Sem medição: {"type":"metric","agent":"…","metric":"…","status":"sem_medicao"}.
- Apagar métrica enviada por engano: {"type":"metric","agent":"…","metric":"…","remove":true}.

Envio pelo box (a chave nunca aparece):

    echo '{"type":"metric","agent":"SDR","metric":"No-show","value":"12%","target":"Abaixo de 20%","status":"ok"}' | python3 /workspace/painel/scripts/enviar.py

Envie quando a medição mudar (no relatório diário ou semanal), não a cada passo. Resposta 400 traz "campo: motivo"; corrija e reenvie uma vez.
