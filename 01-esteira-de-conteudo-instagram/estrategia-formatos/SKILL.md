---
name: estrategia-formatos
description: >-
  Use no início de cada semana, depois que a Joana aprova o Painel da semana,
  para decidir quais formatos de Reel repetir e quais testar na semana-alvo
  (próximos 7 dias, de quarta a terça), com base no desempenho da semana
  anterior, e gravar a decisão (Formato, Repete/Testa e hipótese) nas linhas de
  Peças e no Painel. Substitui o agente DNA-Estrategia-Formatos (decisão da
  Joana, 09/11/2026); serve para qualquer bot do time que planeje formatos.
---
# Estratégia de formatos (repetir ou testar)

Decisão da Joana (09/11/2026): esta etapa é uma skill do Grok Bot, não um agente do Dust. Na esteira do @joanastanieski quem roda é o bot **Social Media e Comunidade**, na etapa 4 da [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac) (domingo, depois da Curadoria e antes do Hook).

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

**Objetivo:** descobrir qual formato viraliza para este público. Cada semana repete o que está funcionando e testa poucos formatos novos, de forma que dê para comparar.

## Quando

- Só depois do OK da Joana para este passo, nas palavras dela, e com a linha da semana em [Painéis da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580) com as "Decisões da Joana" lidas. Antes disso, **pare**.
- Só depois de a Curadoria (skill `dna-curadoria-2`) criar as linhas da semana-alvo em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) (etapa "2 Curadoria" com "Pronto para a próxima").

## Entradas

| Fonte | O que ler |
|---|---|
| Painel da semana aprovado | Números por Reel (views, retenção 3 s, tempo médio, salvamentos, compartilhamentos, seguidores), top e bottom, conclusões e **Decisões da Joana** (mandam sobre esta skill) |
| Peças da semana anterior | Formato, Tipo, Teste de formato, Hipótese do teste A/B, Salvamentos 48h/7d, Compartilhamentos 48h/7d |
| Peças da semana-alvo | As linhas criadas pela Curadoria para os próximos 7 dias, de quarta a terça (tese, tipo, pilar, território, CTA, data no corpo) |
| [Formatos e métricas](https://app.notion.com/p/413379977307819abc54ce8acf914a29) | Lista de formatos e como medir |
| Skills `formato-*` e `orquestra-o-formatos-criativos` | Matriz de escolha (o que a ideia pede: explicar, contar, contrastar, debater, ação, proximidade) |
| `mapeamento-de-modelos-de-reels` | Modelos já declarados e testes em andamento |

## Passos

1. **Placar por formato.** Monte uma tabela com cada formato usado na semana anterior: quantas peças, salvamentos 7d, compartilhamentos 7d, retenção 3 s e views (soma e média). Use só o que está no Painel ou nas linhas; o que faltar é "sem dado". Não estime.
2. **Classifique cada formato:**
   - **Repete:** ficou no topo do Painel em salvamentos ou compartilhamentos (o sinal que importa conforme o CTA da peça), ou a Joana mandou repetir.
   - **Ajusta:** desempenho no meio; repete mudando uma variável só (gancho, duração, abertura visual), escrita na hipótese.
   - **Pausa:** ficou no bottom duas semanas seguidas ou a Joana mandou cortar.
   - **Sem dado suficiente:** 1 peça só ou métrica faltando: repete mais uma vez antes de concluir.
3. **Escolha os testes.** Proposta, a validar com a Joana: a maior parte das peças fica nos formatos "Repete"; 1 a 2 formatos novos por semana, tirados das skills `formato-*` ainda não testados (ou não testados nas últimas 4 semanas). Teste um formato novo em pelo menos 2 peças da semana, para comparar. Formatos com outras pessoas (diálogo, experimento social, conflito situacional, The Office) só com o OK da Joana.
4. **Case formato com tese.** Para cada linha da semana, escolha o formato pela matriz da `orquestra-o-formatos-criativos` (o que a ideia precisa: explicar, narrar, contrastar, debater, ação, proximidade) e pela classificação acima. Nunca escolha por gosto.
5. **Grave em cada linha de Peças:**
   - **Formato** (uma das opções da base);
   - **Teste de formato:** "Repete" ou "Testa";
   - **Hipótese do teste A/B:** uma frase que dá para conferir no Painel seguinte (ex.: "tela verde com gancho de contraste salva mais que palestrinha no mesmo pilar");
   - **Etapa** "3 Estratégia", **Status** "Pronto para a próxima" (segue para o Hook, skill `dna-hook-2`, depois do OK da Joana).
6. **Grave a decisão da semana** no corpo da página da linha do Painel da semana, numa seção "Decisão de formatos": o placar por formato, o que repete, o que testa, o que pausa e as hipóteses. Assim o próximo domingo compara hipótese com resultado.
7. **Avise a Joana** em até 3 linhas: o que repete, o que testa e por quê. Pare e espere o OK dela antes do Hook.

## Saída (modelo da seção "Decisão de formatos")

```
# Decisão de formatos — [AAAA-SNN · DD a DD/MM]
Base: Painel [link] (aprovado em [data]) | Decisões da Joana aplicadas: [quais]
## Placar da semana anterior
| Formato | Peças | Salv. 7d | Comp. 7d | Retenção 3s | Classificação |
## Semana-alvo (quarta DD/MM a terça DD/MM)
- Repete: [formatos] — por quê (número + fonte)
- Testa: [formatos] — hipótese
- Pausa: [formatos] — por quê
## Linhas gravadas
| Código | Data | Formato | Repete/Testa | Hipótese |
STATUS: PRONTO | BLOQUEADO — [motivo]
```

## Checagens

- Todo "Repete", "Testa" e "Pausa" tem número com fonte ou decisão da Joana?
- Nenhum número inventado ou estimado; o que falta está como "sem dado"?
- Os testes são poucos o bastante para comparar (1 a 2 formatos novos) e cada um tem pelo menos 2 peças?
- Toda linha da semana-alvo tem Formato, Teste de formato e Hipótese, e todas as datas caem de quarta a terça da semana-alvo?
- A decisão está gravada no Painel da semana?
- O CTA continua coerente com o formato (SALVAR para ensino; COMPARTILHAR para opinião ou humor)?

## Guardrails

- As "Decisões da Joana" do Painel mandam sobre qualquer regra desta skill.
- Não comece sem o OK da Joana. Se ele ainda não veio, lembre a Joana e pare.
- Não invente métrica, causalidade nem conclusão; escreva hipóteses ("o gancho visual parece ter ajudado").
- Marca só DNA.IA; sem preço, sem Floripa, sem evento, nenhuma palavra-chave nova (ROTINA só no Mapa das 5 Rotinas).
- Não escreva gancho, roteiro nem copy: isso é das skills `dna-hook-2`, `dna-roteirista` e `dna-copy-2`.
- Refazer atualiza as mesmas linhas e incrementa "Tentativas".
