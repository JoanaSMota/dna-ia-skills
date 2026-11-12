---
name: Fluxo da equipe de conteúdo
description: >-
  Use para saber quem faz o quê numa peça de conteúdo do @joanastanieski:
  ponteiro para a Esteira v3 (o Social Media coordena e produz com as skills do
  Grok Bot), a regra da semana-alvo (próximos 7 dias, de quarta a terça) e o
  filtro de gancho de referência.
---
# Fluxo da equipe de conteúdo (ponteiro)

Esta skill foi substituída em 09/11/2026 pela [Esteira de produção — fluxo e gatilhos](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac) (versão 3). Papéis, etapas, gatilhos e checagens estão lá. Agentes começam pelo [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0).

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

Resumo dos papéis (o detalhe está na Esteira):

- **Social Media e Comunidade:** coordena e produz tudo — dispara a esteira, monta o Painel, roda as skills do Grok Bot, faz as artes dos carrosséis (design system v2 Biblioteca da Luz), decide os formatos (skill `estrategia-formatos`), faz os motions (skill `motion-reels`), classifica e codifica os brutos, edita os Reels (skill `editor-reels` + skill do formato), revisa e agenda depois do OK da Joana.
- **Especialistas (skills do Grok Bot, rodadas pelo Social Media):** `dna-pesquisa-2`, `dna-curadoria-2`, `dna-hook-2`, `dna-roteirista`, `dna-copy-2`, `stories-semanais` e `dna-materiais-pdf` (vetada até a Joana liberar). Cada uma faz uma etapa e grava o status na linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0). Os agentes do Dust com esses nomes não são mais usados na esteira (decisão da Joana, 10/11/2026).
- **Skills do Grok Bot (execução, rodadas pelo Social Media):** `estrategia-formatos` (repetir ou testar formato, a partir do Painel), `editor-reels` (edição dos Reels gravados) e `motion-reels` (motions narrados e só com música). Decisão da Joana, 09/11/2026.
- **Joana:** decide o Painel, grava os Reels e a voz dos motions narrados na segunda, sobe os brutos no Drive sem código e dá o OK final por peça. Cada passo da esteira só segue com o OK dela.

Os bots Designer e Editor de Vídeo não fazem parte da esteira.

## Filtro de gancho (o líder mata se falhar)

- O espectador certo se reconhece numa crença ou dúvida real.
- Fica um buraco que só este vídeo fecha.
- Não adianta a conclusão e não descreve o nosso bastidor.
- Não usa fábrica de acusação.
- Atrai quem se importa com resultado do negócio, não com dica genérica de Instagram.
- A promessa do gancho é exatamente o que o meio entrega.

Este filtro é referência para a skill dna-hook-2 e para a etapa de Revisão.
