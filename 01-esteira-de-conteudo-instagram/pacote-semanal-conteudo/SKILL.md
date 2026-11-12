---
name: pacote-semanal-conteudo
description: >-
  Use na rotina de domingo de manhã (Disparo da esteira) para montar o Painel da
  semana do @joanastanieski: métricas dos 7 dias anteriores + relatório visual,
  gravados em Painéis da semana na linha da semana-alvo (próximos 7 dias, de
  quarta a terça), e PARAR até a Joana decidir. Substitui o antigo pacote
  semanal.
---
# Painel da semana

Esta skill substitui o antigo "Pacote semanal de conteúdo" (09/11/2026). O pacote único com aprovação semanal acabou: a produção segue a [Esteira de produção — fluxo e gatilhos](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac), e os agentes começam pelo [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0).

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

Objetivo: dar à Joana, no domingo de manhã, uma leitura clara do que funcionou nos 7 dias anteriores para ela decidir os ajustes da semana-alvo (os próximos 7 dias, de quarta a terça; veja "Semana-alvo"). Nada de produção começa antes dessa decisão.

## Quando

Domingo, 9h (horário de Recife), pela rotina de disparo do Social Media e Comunidade. A antiga rotina "Pacote semanal de conteúdo" de domingo às 17:51 está pausada e foi substituída por este disparo.

## 1. Métricas dos 7 dias anteriores ao disparo

Puxe os números do Zernio e do Instagram Insights, peça por peça, usando o código de cada linha em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) (salvamentos e compartilhamentos em 48h e 7d, retenção por formato). Não estime nada; o que faltar entra como "sem dado".

| Métrica | Fonte (Zernio) |
|---|---|
| Por Reel: views, retenção 3s, tempo médio, salvamentos, compartilhamentos, seguidores ganhos, horário | `analytics_get_analytics` (sort_by views; campos `ig_reels_*`, `follows`) |
| Top 3 Reels (gancho, formato, horário, views) | mesmo, ordenado |
| Seguidores da semana | `accounts_get_follower_stats` (requer o add-on de analytics) |
| Melhor horário | `analytics_get_best_time_to_post` (vem em UTC, converta) |
| Stories: alcance, respostas, votos, perguntas | analytics / Insights |
| Palavra-chave ROTINA (só no post do Mapa das 5 Rotinas) e DMs disparadas | logs das automações (`comment_automations_list_comment_automation_logs`) |
| Seguidores novos dentro do ICP | amostra manual de 20 perfis novos (cargo/porte na bio). Se não der para ver, "sem dado" |
| Conversas qualificadas → reuniões → vendas | quem informa é o cliente (DM, WhatsApp ou CRM) |

Escreva de 3 a 5 conclusões em linguagem simples, cobrindo:

- qual horário rendeu mais;
- qual gancho ou formato repetir e qual testar (insumo da skill `estrategia-formatos`, que roda depois do OK da Joana);
- o que cortar;
- se a qualidade do seguidor subiu ou caiu.

## 2. Relatório visual

Monte uma imagem-resumo com os números e as conclusões, na v2 Biblioteca da Luz (skill `design-system-dna`, único design system vigente desde 12/11/2026). Papel, tinta e âmbar só no destaque; nada de azul ou da v1 Produto, que é legado; sem ícone decorativo e sem caixa com contorno; verde e vermelho só em números.

## 3. Gravar o Painel e PARAR

1. Em [Painéis da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580), crie (ou atualize, se já existir) a linha da **semana-alvo** com os números, as conclusões e o link do relatório visual. Semana = rótulo com as datas e o período das métricas (ex.: `2026-S47 · 18 a 24/11 (métricas de 09 a 15/11)`). Período = quarta a terça da semana-alvo (ex.: 18/11 a 24/11), nunca a semana do disparo.
2. Mude o Status para **"Enviado para a Joana"** e mande a ela o relatório visual com até 3 linhas, pedindo "aprovado", "aprovado com ajustes" ou o que mudar.
3. **PARE.** Não rode Pesquisa, Curadoria nem nenhuma outra etapa até a Joana dar o OK nas palavras dela (ou a linha mostrar Status "Aprovado" ou "Aprovado com ajustes" com as "Decisões da Joana" preenchidas). Nas checagens de domingo, se o Painel ainda espera a Joana, lembre a Joana em vez de seguir.

## 4. Próximo passo

Depois do OK, siga a [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac) a partir da etapa 2 (Pesquisa), um passo de cada vez, com o OK da Joana entre um passo e outro. Cada etapa lê a linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) antes de começar e grava Etapa, Status e link ao terminar.

## Agendamento

Só por peça, depois do OK final da Joana naquela peça (etapa 16 da Esteira), seguindo as notas de Zernio da skill `producao-reels`: ISO com offset, `instagramThumbnail` para a capa, nunca "publicar agora", `posts_list` antes de qualquer nova tentativa e ID do post gravado na linha.

## Guardrails

- Não agende, não publique e não impulsione nada sem o OK explícito da Joana na peça.
- Sem número inventado: toda métrica tem fonte; o que faltar entra como "sem dado".
- Não diga "agendado" sem ter conferido.
- Marca DNA.IA; perfil da fundadora (a DNA aparece só como prova ou bastidor).
- Correção da Joana vira regra: registre no Painel ("Decisões da Joana") e na memória.
