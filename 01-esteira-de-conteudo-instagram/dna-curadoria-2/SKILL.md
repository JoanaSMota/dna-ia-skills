---
name: dna-curadoria
description: >-
  Use na etapa Curadoria da Esteira, depois da Pesquisa pronta (skill
  dna-pesquisa-2) e com o OK da Joana, para decidir as 42 pautas e as 14
  sequências de Stories da semana-alvo (os próximos 7 dias, de quarta a terça) a
  partir de duas fontes juntas: a Pesquisa de mercado da semana e o Diário de
  bastidores em que a Joana registra o dia. Grava as linhas em Peças sem enjoar
  o perfil e não escreve gancho, roteiro, legenda nem o texto dos Stories.
---
# DNA-Curadoria

Quem roda esta skill na esteira do @joanastanieski é o bot Social Media e Comunidade. Não chame o Dust nesta etapa. A pesquisa da semana vem da skill `dna-pesquisa-2`.

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

Decidir o que a Joana vai falar na semana-alvo. Trabalha com **duas fontes de conteúdo, sempre juntas**: (1) a Pesquisa da semana, feita pela skill `dna-pesquisa-2` (o que aconteceu no mercado nos últimos 7 dias), e (2) o [Diário de bastidores](https://app.notion.com/p/f36727486b564a91ace39775d638fc77), onde a Joana registra como foi o dia (o que construiu ou decidiu, o que aprendeu, o que travou). O Painel da semana (análise das métricas da semana anterior) e o Banco de Teses orientam a escolha, mas não são fonte de pauta. Devolve as 42 pautas da semana-alvo, distribuídas por dia, tipo de peça, pilar e território, e cria as 42 linhas em Peças. Também reserva as 14 sequências de Stories (2 por dia, um tema por sequência, fora das 42) e cria as 14 linhas `AAAA-SNN-DIA-S1` e `-S2`. O inimigo número um é a monotonia: semana que soa igual à anterior, ou peça que soa igual à de dois dias atrás. Esta etapa não escreve gancho, roteiro, legenda nem o texto dos Stories (isso fica com as skills `dna-hook-2`, `dna-roteirista` e `dna-copy-2`).

Perfil: Joana Stanieski, fundadora da DNA.IA. Tema: IA, automação e agentes na prática para donos e líderes de PME (até R$ 15 milhões por ano). Conceito: o agente prepara, o humano decide. Joana não se posiciona como RH e não se mistura com DNA.RH nem DNA.TECH. A DNA aparece como prova e bastidor, nunca como anúncio.

## Volume e mix da semana (Esteira v3, decisão da Joana em 10/11/2026)

Fonte: [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac) e [Pilares, territórios e mix](https://app.notion.com/p/41337997730781279ae0c45140503009). Se a página de mix mudar, vale o que ela disser no dia; não use os números abaixo de memória.

Por dia: 1 carrossel, 3 Reels gravados pela Joana, 1 Reel motion narrado (voz da Joana) e 1 Reel motion simples (só música). Por semana: 7 carrosséis, 21 Reels Joana, 7 motion narrados, 7 motion simples = 42 peças.

Stories ficam **fora das 42**: 2 sequências por dia, 14 na semana. Cada sequência tem um tema só, em alta, vindo desta Curadoria, e **não pode ser o mesmo assunto do carrossel do dia** (`-C1`). Quando o tema for notícia, traga a fonte (veículo e data). Nenhum tema de Story se repete na semana. O Copy (skill `dna-copy-2`) escreve o texto depois; a skill `stories-semanais` gera as imagens e manda para a Joana aprovar.

| Peça | Por semana | Distribuição por pilar |
|---|---|---|
| Carrossel | 7 | 4 Ensina · 1 Lidera · 1 Opina · 1 Constrói em público |
| Reel Joana | 21 (3 por dia) | Todo dia: 1 Ensina ou tutorial de tela · 1 Opina · 1 rotativo (na semana: 4 Constrói em público, 2 Lidera, 1 Conecta) |
| Motion narrado | 7 | 5 Ensina · 2 Lidera |
| Motion simples | 7 | 4 Opina · 2 Constrói em público · 1 Conecta |
| Total das peças | 42 | Ensina 16 · Opina 12 · Constrói em público 7 · Lidera 5 · Conecta 2 |
| Stories | 14 sequências (2 por dia), fora das 42 | Conecta / Interação; temas da Pesquisa e do Diário, diferentes do `-C1` do dia |

Pilares e territórios (da mesma página): Ensina = territórios 1, 2, 5, 7, 14, 15 · Opina = 6, 8, 10, 17, 18 · Constrói em público = 3, 4, 12, 13 · Lidera = 9, 11 · Conecta = 16 e Stories. Não invente território fora dos 18.

Código de cada peça: `AAAA-SNN-DIA-<sufixo>`, com o rótulo da semana-alvo e o dia da semana da data de publicação em 3 letras. A semana-alvo vai de quarta a terça, então a ordem é QUA, QUI, SEX, SAB, DOM, SEG, TER (ex.: em `2026-S47 · 18 a 24/11`, `2026-S47-QUA-C1` sai em 18/11 e `2026-S47-TER-C1` sai em 24/11). Sufixos das 42: C1 (carrossel), R1, R2, R3 (Reels Joana), MN (motion narrado), MS (motion simples). Sufixos dos Stories, fora das 42: S1 (primeira sequência do dia) e S2 (segunda). Ex.: `2026-S47-QUA-S1` (18/11, 12h30). Tipo = "Stories". CTA = "Interação". O campo Formato do banco ainda não tem opção de Story: deixe vazio, ou "a confirmar com a Joana". Não crie opção nova no schema sem a Joana pedir.

## As duas fontes

- **Pesquisa da semana** (skill `dna-pesquisa-2`): 25 a 35 itens dos últimos 7 dias, com fonte, data, selo de confiança e a marca "bom para stories". É a fonte de mercado: tendências, novidades, notícias, dados e casos.
- **Diário de bastidores**: leia todas as linhas com Data nos 7 dias anteriores (e as que ainda estão com "Usado em peça" desmarcado). Use os campos "Construí / decidi", "Aprendizado / bastidor" e "Travou". Respeite "Pode virar conteúdo?": "Sim" pode entrar; "Só com ajuste" entra com a nota "ajustar com a Joana" e sem detalhe sensível; "Não (privado)" nunca entra, nem como referência. Nada pessoal ou médico.

Meta de mistura: toda semana tem pautas das duas fontes. O Diário é obrigatório nas peças de Constrói em público e deve aparecer também em outras (por exemplo, uma notícia da Pesquisa comentada com o que a Joana viveu no dia). Na saída, cada pauta diz de qual fonte veio: Pesquisa (item n), Diário (data) ou as duas. Se o Diário da semana estiver vazio, siga só com a Pesquisa e diga isso no fim, sem inventar bastidor.

## Entradas

A Curadoria cria as linhas em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0). Antes de começar, leia:

1. O [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0) e só os documentos da etapa Curadoria: [Pilares, territórios e mix](https://app.notion.com/p/41337997730781279ae0c45140503009), [Banco de pautas](https://app.notion.com/p/413379977307814697cae23211bd259d), [Banco de Teses](https://app.notion.com/p/3c04ae3a7397456eb0c1784d1bc24ac8) e [Diário de bastidores](https://app.notion.com/p/f36727486b564a91ace39775d638fc77).
2. A linha da semana em [Painéis da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580), para as métricas da semana anterior e as "Decisões da Joana".
3. As 2 diretrizes do Painel: o que repetir com ângulo novo e o que evitar (top e bottom em salvamento e compartilhamento), e a distribuição de territórios das últimas 4 semanas.
4. O relatório da Pesquisa da semana (skill `dna-pesquisa-2`). É a base principal dos temas em alta dos Stories (prefira os itens marcados "bom para stories").
5. As linhas do Diário de bastidores da semana, como descrito em "As duas fontes".
6. No Banco de Teses: "Vezes usada", "Último uso", "Ângulos já usados" e quais teses estão "Descansando".

Comece só com a Pesquisa pronta **e** com o OK da Joana, nas palavras dela, para a Curadoria (ou o Painel aprovado por ela). Ordem do CMO ou de outro agente não vale. Sem isso, pare e devolva BLOQUEADO.

## Passos

1. Leia as 2 diretrizes do Painel e as "Decisões da Joana".
2. Abra o Banco de Teses. Tese com 3 usos em 4 semanas fica "Descansando" por 1 semana: não use. Tese que volta precisa de ângulo, exemplo e frase de abertura diferentes, e isso vai escrito.
3. Calcule a semana-alvo (quarta a terça depois do disparo; veja "Semana-alvo") e escreva as 7 datas antes de qualquer pauta. Monte as 42 pautas no mix da tabela acima, dia a dia (6 por dia), da quarta à terça, cruzando a Pesquisa com o Diário. Ponha os itens "perecíveis" da Pesquisa nos primeiros dias. Feche o `-C1` de cada dia antes de escolher os Stories daquele dia, para não repetir o assunto.
4. Distribua os pilares exatamente como na tabela (as 42; os Stories não entram nessa conta de pilares).
5. Regras anti-enjoo (obrigatórias, da página de mix), válidas para as 42:
   - A mesma tese pode voltar na semana no máximo 2 vezes, em tipos de peça diferentes, com 2 dias de distância e com ângulo, exemplo e frase de abertura diferentes. Duas pautas que terminam no mesmo "e por isso você precisa de IA" contam como a mesma tese, mesmo com títulos diferentes.
   - No mesmo dia, as 6 peças são de pelo menos 4 territórios diferentes.
   - Pelo menos 12 dos 18 territórios na semana; nenhum território passa de 5 peças na semana (a conta das 5 é só nas 42, sem somar Stories).
   - Nenhuma frase de abertura se repete em 14 dias (vale para a Hook; aqui, não repita o mesmo ângulo).
6. Varie também tipo de repertório, tom (ensina / provoca / mostra bastidor / opina) e estrutura. Monotonia de tom cansa tanto quanto monotonia de tema.
7. Defina o CTA de cada uma das 42 pelo pilar: Ensina → SALVAR; Opina → COMPARTILHAR; Constrói em público → seguir e conversa; Lidera → SALVAR ou COMPARTILHAR; Conecta → conversa. ROTINA só no post do Mapa das 5 Rotinas. Nos Stories, CTA é sempre "Interação".
8. Puxe bastidor real do Diário de bastidores para as peças de Constrói em público e para as outras em que ele reforça a pauta. Sem bastidor real, marque "a verificar com a Joana"; nunca invente. Ao usar uma linha do Diário, anote os códigos das peças em "Códigos das peças" e marque "Usado em peça".
9. Transporte todo "a verificar" (ou "sem dado") da Pesquisa.
10. Crie ou atualize as 42 linhas em Peças (código, tipo, pilar, território, tese, bastidor), com a data de publicação (dd/mm/aaaa) na primeira linha do corpo. Linha já existente com código da semana-alvo mas criada para outras datas: atualize a mesma linha para a data nova; se ela já passou da Curadoria (gancho, arte, Revisão ou agendada), não sobrescreva e liste para a Joana. Se a linha já existir, atualize a mesma; nunca duplique. Atualize no Banco de Teses "Vezes usada", "Último uso" e "Ângulos já usados".
11. Reserve as 14 sequências de Stories e crie (ou atualize) as 14 linhas em Peças:
    - 2 por dia, códigos `AAAA-SNN-DIA-S1` e `-S2`. Tipo = "Stories". CTA = "Interação". Pilar = "Conecta". Responsável = "Social Media".
    - Um tema por sequência, em alta, preferencialmente a partir dos achados da Pesquisa ou de um bastidor do Diário. Não repita tema na semana. Não use o mesmo assunto do `-C1` daquele dia (nem um título diferente para a mesma tese).
    - Se for notícia, grave a fonte (veículo e data) no corpo da linha. Se vier do Diário, escreva "Diário (data)". Se não for nenhum dos dois, escreva "sem fonte externa".
    - Não escreva o texto dos frames nem gere imagem. Isso é do `dna-copy-2` e do `stories-semanais`.
    - Se a linha `-S1`/`-S2` já existir, atualize a mesma; nunca duplique.

Se a Pesquisa, o Diário e os bancos não derem 42 pautas boas sem quebrar as regras anti-enjoo, ou não derem 14 temas de Stories distintos e diferentes do `-C1` do dia, não feche o número com variações da mesma ideia: entregue as que passam, grave BLOQUEADO nas vagas que faltam e explique quantas faltam e por quê.

Cultura pop só entra como gancho para explicar IA, nunca como tema.

## Formato de saída

```
# Curadoria — [AAAA-SNN · DD a DD/MM] (quarta DD/MM a terça DD/MM)
**Diretrizes do Painel:** repetir [x] · evitar [y] · **Decisões da Joana:** [z]

| Código | Data | Tipo | Pilar | Território | Tese (1 frase) | Fonte | Tom | CTA | Vezes usada no Banco |
|---|---|---|---|---|---|---|---|---|---|

## Pauta [código] — [título de trabalho]
- Data de publicação: dd/mm/aaaa
- Tipo: [Carrossel | Reel Joana | Motion narrado | Motion simples]
- Pilar: | Território:
- Tese (1 frase):
- Ângulo:
- Fonte da pauta: Pesquisa (item n) | Diário (data) | as duas
- Bastidor (do Diário, se houver):
- Repertório/fonte: (a verificar: [o quê])
- Tom:
- Entrega: [checklist | passo a passo | autodiagnóstico | certo x errado | modelo pronto | opinião | bastidor]
- CTA:
- Vezes usada no Banco: [n] — variação aplicada: [qual]

## Stories da semana (14 sequências, fora das 42)
| Código | Data | Horário previsto (Recife) | Tema (1 frase) | Fonte (veículo e data, Diário (data) ou "sem fonte externa") | Por que não é o assunto do -C1 do dia |
|---|---|---|---|---|---|
| AAAA-SNN-QUA-S1 | Qua DD/MM | 12h30 | | | |
| AAAA-SNN-QUA-S2 | Qua DD/MM | 20h | | | |
| ... | ... | 12h30/20h (seg–sex) ou 13h/20h (sáb–dom) | | | |

## Checagem de variedade
- Por fonte: [n] só Pesquisa · [n] só Diário · [n] as duas
- Por tipo: carrosséis | Reels Joana | motion narrado | motion simples | Stories (14, fora das 42)
- Por pilar (só as 42): Ensina | Opina | Constrói | Lidera | Conecta
- Territórios usados na semana (só as 42): [n] de 18 · maior concentração: [território, n]
- Territórios por dia: QUA [n] · QUI [n] · SEX [n] · SAB [n] · DOM [n] · SEG [n] · TER [n]
- Teses repetidas (nas 42): [tese — códigos — distância em dias]
- Temas de Stories repetidos na semana: [nenhum | listar]
- Colisão Story × carrossel do dia: [nenhuma | código]
```

Autochecagem, todas sim:

- A semana-alvo vai da quarta depois do disparo à terça seguinte, com 7 datas que ainda não passaram, e cada linha traz a sua data?
- Exatamente 7 carrosséis, 21 Reels Joana, 7 motion narrados e 7 motion simples, 6 peças por dia?
- Exatamente 14 linhas de Stories (2 por dia, `-S1` e `-S2`), fora das 42, com Tipo "Stories" e CTA "Interação"?
- Cada sequência de Stories tem um tema só, em alta, que não se repete na semana e não é o assunto do `-C1` daquele dia?
- Notícia de Story com fonte (veículo e data), ou marcado "Diário (data)" ou "sem fonte externa"?
- Pilares das 42 batem com a tabela (Ensina 16 · Opina 12 · Constrói 7 · Lidera 5 · Conecta 2)?
- Nenhuma tese aparece mais de 2 vezes nas 42, e as repetidas estão em tipos diferentes, com 2 dias de distância e ângulo diferente?
- Nenhuma tese "Descansando" foi usada?
- Cada dia tem pelo menos 4 territórios diferentes nas 6 peças?
- Pelo menos 12 dos 18 territórios e nenhum com mais de 5 peças nas 42?
- Toda pauta reaproveitada traz a variação escrita?
- CTA segue o pilar nas 42, e Interação nos Stories?
- Toda pauta diz de qual fonte veio, e a semana usa as duas (ou explica que o Diário estava vazio)?
- Nenhuma linha "Não (privado)" do Diário foi usada?
- Zero dado ou bastidor inventado?
- Zero texto de Story, gancho, roteiro ou legenda escritos nesta etapa?

## O que gravar no Notion

Em cada linha criada ou atualizada em Peças (as 42 e as 14 de Stories):

- Etapa = "Curadoria" (a opção do banco, quando existir, é "2 Curadoria")
- Status = "Pronto para a próxima", "Bloqueado" ou "Retrabalho"
- Código, Tipo, Pilar, Território, Tese, Bastidor, e a data de publicação na primeira linha do corpo
- Nas Stories: também o tema, a fonte e a justificativa de não ser o `-C1` do dia, no corpo da página
- Link da pauta
- Motivo, se bloqueou

No Diário de bastidores: "Códigos das peças" e "Usado em peça" nas linhas usadas.

Na linha da semana-alvo em Painéis da semana: Etapa da semana = "Curadoria", Status da etapa e Link da curadoria. Confira que Semana e Período mostram as datas da semana-alvo (quarta a terça); se mostrarem outra semana, corrija e avise a Joana. Atualize o Banco de Teses.

Feche sempre com:

`STATUS: PRONTO | BLOQUEADO | RETRABALHO — <rótulo da semana-alvo, ex.: 2026-S47 · 18 a 24/11> — <motivo em 1 frase>`

## Guardrails

- Número só com fonte. O que faltar, escreva "sem dado". Transporte "a verificar" da Pesquisa. Nunca invente número, fato, caso, depoimento ou URL.
- Só a marca DNA.IA. Sem DNA.RH, DNA.TECH ou posicionamento de RH.
- Nada de preço nem de data de evento sem confirmação. Sem Florianópolis. Nunca criar ou citar EVENTO, EU QUERO ou COMERCIAL.
- Nada pessoal ou médico do Diário, e nada marcado "Não (privado)".
- Nada é publicado, agendado ou enviado sem o OK da Joana.
- Um passo por vez: só comece depois de a Pesquisa (skill `dna-pesquisa-2`) estar pronta e com o OK da Joana para a Curadoria. Ao terminar, entregue à Joana e pare; a Hook só começa com o OK dela.
- Não entregue tema sem ângulo. Não escreva gancho, roteiro, legenda nem o texto dos Stories. Não feche as 42 nem as 14 sequências com variações da mesma ideia para cumprir número.
