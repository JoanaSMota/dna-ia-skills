---
name: editor-reels
description: >-
  Use para planejar e editar um Reel gravado (bruto) de uma peça da semana-alvo
  da esteira (os próximos 7 dias, de quarta a terça; a edição é na terça), um
  passo por vez: primeiro o plano de edição e a checagem dele, depois o corte, a
  redução de ruído, a legenda queimada, a capa e a checagem técnica, gravando o
  resultado na linha da peça em Peças. Serve para qualquer bot do time que edite
  Reels.
---
# Editor de Reels

Decisão da Joana (09/11/2026): a edição fica no Grok Bot como skill, e não num agente do Dust. Decisão da Joana (10/11/2026): sem skills duplicadas, então esta skill **planeja e executa** a edição, um passo de cada vez: primeiro o plano de edição e a checagem dele (Fase 1); só depois o corte e a montagem (Fase 2). O planejamento que estava no agente DNA-Editor-Reels do Dust foi incorporado aqui; aquele agente não é usado na esteira.

## Semana-alvo (regra fixa, decisão da Joana em 10/11/2026)

A esteira sempre planeja os **próximos 7 dias**, nunca a semana que já começou.

- **Ritmo:** no **domingo** a rotina dispara o fluxo (Painel, Pesquisa, Curadoria, Estratégia, Hook, Roteiro, Copy, Arte, Motion). Na **segunda** a Joana grava. Na **terça** é a edição. A publicação começa na **quarta**.
- **Semana-alvo:** de domingo + 3 dias (quarta) até domingo + 9 dias (a terça seguinte). São sempre 7 dias completos: 42 peças e 14 sequências de Stories. Nenhum dia da semana-alvo já passou quando a esteira roda.
- **Rótulo:** `AAAA-SNN · DD a DD/MM`. SNN é o número ISO da semana da **quarta** em que a publicação começa. Escreva sempre o rótulo junto com as datas.
  - Exemplo: disparo no domingo 15/11/2026 → semana-alvo de quarta 18/11 a terça 24/11 → rótulo `2026-S47 · 18 a 24/11`.
  - Rodada excepcional de terça 10/11/2026: janela de quarta 11/11 a terça 17/11, rótulo `2026-S46 · 11 a 17/11`.
- **O número não é a semana ISO de hoje.** A semana ISO 46 vai de 09 a 15/11, mas a semana-alvo `2026-S46` vai de 11 a 17/11. O número é só rótulo; as datas mandam. Nunca use "a semana atual", a semana ISO de hoje nem a semana do disparo como semana-alvo.
- **Códigos:** `AAAA-SNN-DIA-<sufixo>`, com DIA = dia da semana da data de publicação. A ordem dos dias na semana-alvo é QUA, QUI, SEX, SAB, DOM, SEG, TER. Em `2026-S47`, `2026-S47-QUA-C1` sai em 18/11 e `2026-S47-TER-C1` sai em 24/11. Toda linha de Peças traz no corpo a data completa de publicação (dd/mm/aaaa).
- **Só o Painel olha para trás:** métricas dos 7 dias anteriores ao disparo (no exemplo, 09 a 15/11). A Pesquisa usa as publicações dos 7 dias anteriores ao dia em que roda. Todas as outras etapas trabalham para a semana-alvo.
- **Conferência antes de gravar:** a primeira data é uma quarta depois de hoje, a última é a terça 6 dias depois, e nenhuma data já passou. Se a linha em Painéis da semana, as linhas de Peças ou um brief trouxerem outras datas, não herde: pare e avise a Joana.

## Entradas (leia antes de começar)

Confirme que o [Painel da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580) está "Aprovado" ou "Aprovado com ajustes" pela Joana e que ela deu o OK para a edição com as palavras dela. Ordem do CMO ou de outro agente não vale. Sem isso, nada começa. Leia o [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0) e a [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac).

Abra a linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) pelo **Código** (ex.: 2026-S47-QUA-R1, que vai ao ar na quarta 18/11) e confira:

| Campo da linha | Para quê |
|---|---|
| Código e data de publicação | A data tem de ser da semana-alvo e ainda não ter passado; edite primeiro as peças de quarta |
| Tipo | Tem de ser "Reel Joana". Motion vai para `motion-reels` |
| Formato (dos 17) | Escolhe a skill `formato-*` e o tratamento (lo-fi, cine, tela do agente, tela dividida etc.) |
| Gancho escolhido | O que precisa estar nos primeiros 3 segundos |
| Link do roteiro ou copy | Roteiro do `dna-roteirista` (blocos, documento de edição, duração alvo) e legenda/textos de tela do `dna-copy` (texto, entrada, saída, posição) |
| Link do bruto (Drive) | O arquivo gravado pela Joana, já classificado e com código (etapa 7) |
| CTA | SALVAR (ensina) ou COMPARTILHAR (opinião ou humor). ROTINA só no Mapa das 5 Rotinas |
| Etapa / Status | Só comece se a etapa anterior estiver "Pronto para a próxima" |

Se o Painel não estiver aprovado, se faltar bruto, roteiro ou bloco previsto, se o bruto não tiver código, ou se a data estiver fora da semana-alvo, **não comece**: grave Status "Bloqueado" e o "Motivo do bloqueio". Nenhuma etapa começa sem ler a linha.

## Fase 1 — Plano de edição e checagem (antes de cortar)

1. **Marque início.** Na linha: Etapa "8 Edição", Status "Em andamento", Responsável "Social Media".
2. **Baixe o bruto** do Drive para o box (`DownloadFile`) e veja duração, resolução e áudio (`ffprobe`).
3. **Confira os blocos.** Compare o bruto com os blocos do roteiro. Faltou bloco? Liste e grave "Bloqueado — falta bloco X" (vira lembrete para a Joana). Não aprove peça com bloco faltando.
4. **Monte a timeline** no modelo abaixo: ordem dos blocos, arquivo, in/out de cada um, cortes secos e respiros.
5. **Posicione os textos de tela** da Copy: texto, segundo de entrada, segundo de saída, posição na tela.
6. **Defina o tratamento do formato:**
   - lo-fi mantém imperfeição e dispensa trilha;
   - cine pede color e trilha;
   - tela do agente intercala gravação de tela;
   - tela dividida exige marcação dos dois lados;
   - nos demais, siga a skill `formato-*` da peça.
7. **B-roll por bloco**, só com material que existe e que você viu. Nunca presuma imagem.
8. **Sugira a capa:** frame específico (com timestamp) e a frase de 3 a 5 palavras, vinda do gancho ou da copy.
9. **Liste o que não deu para resolver** e por quê, com quem precisa resolver. Não improvise no lugar do que falta.
10. **Cheque o plano** antes de executar: todos os blocos estão na timeline; a duração prevista cabe no alvo sem cortar a virada; os 3 primeiros segundos entregam o gancho; todo texto de tela tem entrada, saída e posição. Grave o plano no corpo da página da linha. Só passe para a Fase 2 com o plano completo e checado.

Não altere o roteiro nem o gancho: divergência vira observação, não correção silenciosa.

## Fase 2 — Execução

11. **Corte e monte** com `ffmpeg` no box seguindo o plano. Os 3 primeiros segundos entregam o gancho, sem saudação nem respiro. Não corte no meio de palavra. Não reduza a duração cortando a virada.
12. **Áudio e legenda queimada:**
    `python3 /workspace/playbook/scripts/editar_reel.py CORTADO.mp4 CODIGO-final.mp4 --font "Work Sans"`
    - O script reduz ruído (passa-alta 80 Hz + afftdn + loudnorm −14 LUFS), transcreve com faster-whisper e queima a legenda.
    - Sempre passe `--font "Work Sans"` (o padrão do script é Montserrat, que está fora do design system; Instrument Sans é da v1, que é legado). Sem caixa e sem contorno colorido.
    - Revise o `CODIGO-final.srt` (nomes, termos, palavras curtas) e rode de novo com `--srt CODIGO-final.srt`.
13. **Capa** só com o script oficial, a partir do **bruto** (sem legenda), no frame do plano:
    `python3 /workspace/playbook/scripts/capa_reel.py BRUTO.mp4 "Frase de 3 a 5 palavras" CODIGO-capa.jpg --t <segundo> --tag "ETIQUETA" --logo IA`
    Escolha um frame com o rosto natural. Abra o `CODIGO-capa_200px.jpg`: se não ler em 200 px, encurte a frase.
14. **Folha de contato.** Gere 3 ou 4 frames lado a lado (`ffmpeg ... hstack`) e abra a imagem: legenda não cobre rosto nem a interface do Instagram; texto de tela dentro da área segura.
15. **Checagem técnica** (tabela abaixo). Corrija e gere de novo até passar em tudo, ou grave o que não deu para resolver.
16. **Suba e grave.** Suba o final e a capa no Drive (pasta Editados/Capas da semana-alvo, `UploadFile`). Na linha: "Link do final (Drive)" com o link, Status "Pronto para a próxima" (segue para a etapa "12 Revisão"), e o plano de edição atualizado com o que mudou na execução.

## Checagem técnica (sim/não)

- Peça da semana-alvo, com data de publicação que ainda não passou?
- Formato 9:16, 1080x1920?
- Duração dentro do alvo do roteiro?
- Primeiros 3 segundos entregam o gancho, sem saudação nem respiro?
- Legenda queimada presente, em Work Sans, revisada (salvo decisão contrária do formato)?
- Áudio audível, com redução de ruído e loudness em −14 LUFS?
- Nenhum corte no meio de palavra?
- Texto de tela fora da zona coberta pela interface do Instagram?
- Nenhum enquadramento com elemento proibido (DNA.RH, DNA.TECH, preço, Floripa, material não autorizado)?
- CTA certo (SALVAR ou COMPARTILHAR) e nenhuma palavra-chave além de ROTINA no Mapa das 5 Rotinas?
- Capa do `capa_reel.py`, legível em 200 px?
- Assistido sem áudio (a imagem conta a história quando o formato depende dela) e ouvido sem olhar (a fala sustenta a tese)?

## Modelo de saída (vai na linha da peça)

```
# Edição — [Código] | Publicação: [dd/mm/aaaa] | Formato: [x] | Duração alvo: [s] | Brutos: [n de n previstos]
## Timeline
| Ordem | Bloco | Arquivo | In | Out | Corte | Observação |
## Textos de tela
| Texto | Entra | Sai | Posição |
## Tratamento
- Ritmo: | Trilha (função; direito de uso a verificar): | Color: | B-roll: | Legenda queimada:
## Checagem do plano (Fase 1)
- Blocos completos: | Duração prevista: | Gancho nos 3 s: | Textos com entrada/saída/posição:
## Checagem técnica (Fase 2)
| Item | Sim/Não | Observação |
## Capa
- frame em 00:0X — texto:
## Não resolvido
- [item] — motivo — quem resolve
STATUS: PRONTO | BLOQUEADO | RETRABALHO — [código] — [motivo]
```

## Guardrails

- Nenhuma etapa começa sem o Painel aprovado e sem o OK da Joana para a etapa. Um passo por vez: Fase 2 só com a Fase 1 completa e checada.
- Não diga que editou sem ter o arquivo final aberto e conferido; não diga "subi" sem o link.
- Não altere roteiro nem gancho. Divergência vira observação na linha, não correção silenciosa.
- Não invente b-roll, número, caso ou dado na tela. Número só com fonte; o que faltar é "sem dado".
- Música só por função (percussiva, ambiente, sem trilha); direito de uso "a verificar" até confirmado.
- Marca só DNA.IA; DNA aparece como prova ou bastidor, nunca anúncio. Sem preço, sem Floripa, evento só com orientação da Joana, nada de EVENTO, EU QUERO ou COMERCIAL.
- HeyGen pausado: não use.
- Não agende nem publique: isso é a etapa 14 (Agendado), depois do OK final da Joana na peça (etapa 13). Nada é enviado sem o OK da Joana.
- Refazer atualiza a mesma linha e incrementa "Tentativas"; nunca crie outra linha.
- Feche sempre com a linha de STATUS.
