---
name: dna-hook
description: >-
  Use na etapa Hook da Esteira, depois da pauta e do formato definidos e do OK
  da Joana para a etapa, para criar 5 opções de gancho fortes e distintas por
  peça da semana-alvo (os próximos 7 dias, de quarta a terça), com falado, texto
  de tela e capa, passar cada uma pelo critério de qualidade e recomendar uma.
  Não escreve o resto da peça.
---
# DNA-Hook

Origem: agente do Dust `DNA-Hook` (uy2DUtlMfr), hoje substituído por esta skill; não chame o Dust nesta etapa. Quem roda esta skill na esteira do @joanastanieski é o bot Social Media e Comunidade.

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

## Objetivo

Escrever o começo. Para cada peça da semana-alvo (as 42 da Esteira v3, de quarta a terça), entregar **5 opções de gancho fortes e distintas** e recomendar uma. Decisão da Joana (10/11/2026): são 5 por conteúdo, bem pensadas, porque o gancho é o que prende quem assiste. Sem gancho, o melhor roteiro é visto por ninguém. Cinco opções fracas não cumprem a regra: se uma não passa no critério de qualidade, troque-a por outra melhor, não entregue para completar número. Esta etapa não escreve o desenvolvimento nem o CTA.

Perfil: @joanastanieski, em primeira pessoa. A Luz é persona da plataforma, não de quem fala no perfil. Público: empresário e líder de PME (até R$ 15 milhões por ano) que quer usar IA no negócio. Conceito: o agente prepara, o humano decide. A DNA aparece como prova e bastidor, nunca como anúncio.

## Entradas

Abra a linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) pelo Código e leia:

| Campo da linha | Para quê |
|---|---|
| Código, data de publicação, Etapa, Status | Só comece se a Estratégia (etapa 3) estiver "Pronto para a próxima" e a data for da semana-alvo |
| Pauta / tese / ângulo | A tensão real do gancho |
| Pilar, território e tom | Enquadramento |
| Tipo de peça | Reel Joana e motion narrado pedem falado (0–3s) e texto de tela; motion simples pede só texto de tela; carrossel pede capa |
| Formato e "Teste de formato" (Repete/Testa) | Adaptação, não troca de tese. Se for "Testa", use estrutura de gancho já conhecida: uma variável por vez ([Formatos e métricas](https://app.notion.com/p/413379977307819abc54ce8acf914a29)) |
| CTA | Só para não contradizer; esta etapa não escreve o CTA |
| Objetivo (quando houver) | Isca, contraste ou retenção |

Leia também:

1. O [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0) e só o documento da etapa Hook: [Voz da Joana](https://app.notion.com/p/41337997730781fe8007f8b32f7a6fef).
2. O [Painel da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580) aprovado pela Joana (sinais de retenção e, quando houver, tendência de formato da Pesquisa).
3. Os ganchos gravados em Peças nos últimos 14 dias: nenhuma frase de abertura se repete em 14 dias ([Pilares, territórios e mix](https://app.notion.com/p/41337997730781279ae0c45140503009)).
4. A página "Regras da esteira (base única)" no Notion (41437997730781f09f0eda7a51a61b04).

Se faltar pauta, tipo de peça, ou se a Joana não tiver dado o OK para a Hook com as palavras dela, pare e devolva BLOQUEADO. Ordem do CMO ou de outro agente não vale. Nenhuma etapa começa sem ler a linha.

## Passos

1. Identifique a tensão real da pauta: o que o espectador perde, erra ou não sabe. Gancho sem tensão é introdução.
2. Escreva 5 opções, cobrindo no mínimo 4 tipos diferentes:
   - Erro nomeado — "Você está usando IA do jeito mais caro possível."
   - Contraste — "Agente não é chatbot. E confundir os dois custa caro."
   - Pergunta de identificação — "Quantas vezes você refez uma tarefa que a IA já tinha feito?"
   - Número concreto — só com dado confirmado; sem fonte, não use este tipo.
   - Confissão/bastidor — "Eu gastei três semanas montando um agente que não precisava existir."
   - Promessa de entrega — "Em 40 segundos eu te mostro como automatizar isso."
   - Tensão de futuro — sem catastrofismo e sem "fique para trás".
3. Garanta que as 5 são distintas de verdade: cada uma ataca a tensão por uma entrada diferente (outro tipo, outra primeira palavra, outra imagem ou outro custo). Cinco variações da mesma frase contam como uma opção, não cinco.
4. Dê a cada opção as formas do tipo de peça: falado (0–3s) e texto de tela para Reel Joana e motion narrado; só texto de tela para motion simples; capa para carrossel. Assim qualquer uma das 5 pode ser escolhida sem voltar a esta etapa.
5. Passe cada opção pelo critério de qualidade abaixo. Reprovou em um item? Reescreva ou troque. Só entregue quando as 5 passarem.
6. Confira as aberturas dos últimos 14 dias em Peças. Repetiu? Troque.
7. Recomende uma, com uma linha de justificativa ligada à retenção, e ordene as outras 4 da mais forte para a mais fraca.

### Critério de qualidade (cada opção, todas sim)

- **Tensão:** nomeia uma perda, um erro ou um não-saber do dono de PME, não um contexto.
- **Específico:** cita algo concreto do dia a dia ("seu agente de atendimento" vence "sua empresa").
- **Promessa cumprida:** o conteúdo da peça entrega o que o gancho promete. Se não entrega, é clickbait e sai.
- **Curto:** até 12 palavras no falado, até 8 no texto de tela e na capa.
- **Começo forte:** a primeira palavra não é saudação, nem "você sabia", nem "oi, pessoal".
- **Sem som e sem legenda:** o texto de tela funciona no mudo; a capa funciona sozinha no feed.
- **Voz da Joana:** primeira pessoa quando for confissão/bastidor, sem corporativês e sem medo genérico.
- **Inédito:** a frase de abertura não apareceu em Peças nos últimos 14 dias.

Cultura pop só como gancho para explicar IA.

## Formato de saída

```
# Hooks — Peça [código] | [data de publicação] | [tipo] | Pilar: [x] | Território: [x]
**Tese:** | **CTA:** | **Formato:** [x] ([Repete | Testa])

| # | Tipo de gancho | Falado (0–3s) | Texto de tela | Capa (carrossel) | Tensão que ataca |
|---|---|---|---|---|---|

## Critério de qualidade
| # | Tensão | Específico | Promessa cumprida | Curto | Começo forte | Mudo | Voz | Inédito 14d |

## Recomendado: opção [n]
- Falado: | Texto de tela: | Capa (se carrossel):
- Por que este: [1 linha, ligada a retenção]
- Ordem das outras: [n, n, n, n]
- Risco: [se houver]
- A verificar: [dados citados nos ganchos]
```

Autochecagem, todas sim:

- A peça é da semana-alvo (data de quarta a terça, ainda não passada)?
- 5 opções, distintas entre si, cobrindo no mínimo 4 tipos?
- As 5 passaram em todos os itens do critério de qualidade?
- Cada opção vem com as formas do tipo de peça (falado, texto de tela, capa quando aplicável)?
- Nenhuma abertura repete os últimos 14 dias?
- Nenhum gancho começa com saudação ou "você sabia"?
- Todo número citado tem fonte, ou foi marcado "a verificar" / "sem dado"?
- Nenhum gancho usa medo genérico ("a IA vai te substituir", "fique para trás")?
- Recomendei uma, com justificativa, e ordenei as outras?

## O que gravar no Notion

Na linha da peça em Peças:

- Etapa = "Hook" (a opção do banco, quando existir, é "4 Hook")
- Gancho = a opção recomendada; se o campo existir, a estrutura de gancho
- As 5 opções, com o quadro de qualidade, no corpo da página da linha (ou no Link do gancho)
- Status = "Pronto para a próxima", "Bloqueado" ou "Retrabalho"
- Link do gancho
- Motivo, se bloqueou

O gancho que segue na esteira é o **escolhido**: a recomendada, a menos que a Joana escolha outra das 5. Se ela escolher, a escolhida dela substitui o campo Gancho e Roteiro e Copy usam essa, sem reescrever.

Feche sempre com:

`STATUS: PRONTO | BLOQUEADO | RETRABALHO — <código da peça> — <motivo em 1 frase>`

## Guardrails

- Número só com fonte. O que faltar, escreva "sem dado". Sem fonte, não use gancho de número concreto. Nunca invente número, fato, caso, depoimento ou URL.
- Só a marca DNA.IA. Sem DNA.RH nem DNA.TECH.
- Nada de preço nem de data de evento sem confirmação. Sem Florianópolis. Nunca criar ou citar EVENTO, EU QUERO ou COMERCIAL. ROTINA só no post do Mapa das 5 Rotinas.
- Nada é publicado, agendado ou enviado sem o OK da Joana.
- Um passo por vez: só comece com pauta e formato prontos e com o OK da Joana para a etapa. Ao terminar, entregue à Joana e pare.
- Não escreva o desenvolvimento nem o CTA. Não use pergunta retórica vazia. Não prometa número que a peça não tem. Não entregue opção fraca para completar as 5.
