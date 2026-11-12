---
name: stories-semanais
description: >-
  Use quando for escrever, conferir, gerar as imagens e enviar para aprovação os
  Stories da semana-alvo (os próximos 7 dias, de quarta a terça). No
  @joanastanieski são as 2 sequências diárias da Esteira v3, fora das 42 peças,
  em texto nativo, com tom informal de dia a dia, sem CTA visível e sem fonte
  entre parênteses. O Copy (dna-copy-2) escreve seguindo o tom definido aqui. O
  bot gera as imagens, manda as folhas no chat da Joana e só agenda no Zernio
  depois do OK dela.
---
# Stories semanais

Objetivo: presença todos os dias, autoridade com as notícias do nicho e conversas no direct com o ICP do cliente. Esta skill substitui o fluxo antigo, que pedia arte de marca, 3 frames por sequência e pesquisa no Dust.

## Tom dos Stories (decisão da Joana em 10/11/2026, aprovada nos pilotos QUI-S1 e SEX-S2)

O tom dos Stories é **diferente** do resto da esteira. O story é feito na hora, some em 24h e é rápido, então **não pode parecer elaborado**. Tem que soar como a Joana digitando no app, no dia a dia.

- **Linguagem informal, no tom dela.** Use frase curta e conversa: "Gente, olha isso.", "Confissão do dia:", "né?", "tô", "pra", "uns 500", "Ou seja:". Pode ter reação pessoal ("Quatro.", "Tô de olho em mim.").
- **Sem descredibilizar.** A ortografia e a acentuação estão certas, sem gíria forçada nem erro de propósito, e o número continua com fonte.
- **Sem cara de post.** Nada de estrutura de carrossel, lista numerada, título, "3 dicas" ou frase de efeito de palestra.
- **Sem CTA visível.** É proibido pedido explícito: "comenta", "clica", "responde", "manda", "me conta", "vota", "arrasta", "link na bio", "salva" ou "compartilha". Toda sequência é construída para provocar interação, e a interação nasce da própria construção: uma opinião que dá vontade de rebater, uma confissão em que a pessoa se reconhece, um número que surpreende ou uma pergunta solta que não é um pedido ("Arrumar processo tem toda cara de trabalho, né?"). Se ele for bem construído, gera interação sozinho.
- **Fonte sem parêntese.** Nunca ponha referência entre parênteses na tela (por exemplo "(TechCrunch, 04/11)"), porque fica robótico. Quando a fonte precisa aparecer, ela entra natural na frase ("Quem contou foi o TechCrunch.", "saiu no relatório da McKinsey essa semana"). Quando não precisa, fica só na linha do Notion. A fonte continua registrada na linha sempre.

Exemplos aprovados (2026-S46):

- QUI-S1, story 1: "Gente, olha isso.\n\nNa semana do Halloween, a Uber contou 4 corridas pedidas por agente de IA. Quatro."
- QUI-S1, story 2: "No Uber Eats foram uns 500 pedidos, no meio de uns 320 milhões. Quem contou foi o TechCrunch.\n\nOu seja: ainda é raríssimo."
- SEX-S2, story 1: "Confissão do dia: segunda eu ia gravar.\n\nNão gravei. Passei o dia arrumando o sistema que produz o meu conteúdo."
- SEX-S2, story 2: "Arrumar processo tem toda cara de trabalho, né?\n\nÀs vezes é só adiar bonito. Tô de olho em mim."

Arquivos dos pilotos: `/workspace/pilotos-v2/stories/` (script `build.py` e folhas de contato).

## Semana-alvo (regra fixa, decisão da Joana em 10/11/2026)

A esteira sempre planeja os **próximos 7 dias**, nunca a semana que já começou.

- **Ritmo:** no **domingo** a rotina dispara o fluxo (Painel, Pesquisa, Curadoria, Estratégia, Hook, Roteiro, Copy, Arte, Motion). Na **segunda** a Joana grava. Na **terça** é a edição. A publicação começa na **quarta**.
- **Semana-alvo:** de domingo + 3 dias (quarta) até domingo + 9 dias (a terça seguinte). São sempre 7 dias completos: 42 peças e 14 sequências de Stories. Nenhum dia da semana-alvo já passou quando a esteira roda.
- **Rótulo:** `AAAA-SNN · DD a DD/MM`. SNN é o número ISO da semana da **quarta** em que a publicação começa. Escreva sempre o rótulo junto com as datas.
  - Exemplo: disparo no domingo 15/11/2026 → semana-alvo de quarta 18/11 a terça 24/11 → rótulo `2026-S47 · 18 a 24/11`.
- **O número não é a semana ISO de hoje.** O número é só rótulo; as datas mandam.
- **Códigos:** `AAAA-SNN-DIA-<sufixo>`, com DIA = dia da semana da data de publicação, na ordem QUA, QUI, SEX, SAB, DOM, SEG, TER. Toda linha de Peças traz no corpo a data completa de publicação (dd/mm/aaaa).
- **Conferência antes de gravar:** a primeira data é uma quarta depois de hoje, a última é a terça 6 dias depois, e nenhuma data já passou. Se a linha em Painéis da semana, as linhas de Peças ou um brief trouxerem outras datas, não herde: pare e avise a Joana.

Na esteira do @joanastanieski, os Stories ficam **fora das 42 peças** da semana. Quem roda é o bot Social Media e Comunidade, um passo por vez, só depois de a Curadoria e a Copy estarem prontas e de a Joana ter liberado a etapa com as palavras dela. Nada é agendado sem o OK dela.

## Pré-requisitos

- Intake preenchido no Notion: ICP, tom, identidade visual dos Stories (arte da marca ou texto nativo), cadência e regras do cliente.
- Conectores ativos: Zernio (agendamento) e Notion (linhas das peças). Canva não entra neste fluxo.
- Modelo visual aprovado pelo cliente. No @joanastanieski o modelo é **texto nativo** (fundo preto sólido, texto branco centralizado, fonte Instagram Sans Regular), decisão da Joana em 13/10/2026, porque o story precisa parecer que ela mesma escreveu no app.
- Textos prontos. Quem escreve é a skill `dna-copy-2`, a partir da Curadoria (`dna-curadoria-2`), seguindo a seção "Tom dos Stories" acima. Esta skill não pesquisa nem inventa tema.
- A página "Regras da esteira (base única)" no Notion (41437997730781f09f0eda7a51a61b04), lida antes de conferir ou reescrever o texto.

## Regras do @joanastanieski (Esteira v3)

- **42 peças por semana é oficial** (7 carrosséis, 21 Reels Joana, 7 motion narrados, 7 motion simples). Os Stories **não entram nessa conta**.
- **2 sequências por dia** (14 na semana). Cada sequência aborda **um tema só**, vindo da Curadoria, e **não pode ser o mesmo assunto do carrossel do dia** (`-C1`).
- O conteúdo de uma sequência se divide em **no máximo 2 stories**. Em cada story, no máximo 2 blocos curtos de texto.
- Temas da semana não se repetem. Assuntos em alta, com a fonte (veículo e data) registrada na linha.
- **Sem CTA visível e sem palavra-chave** (veja "Tom dos Stories"). Nunca EVENTO, EU QUERO, COMERCIAL ou PLATAFORMA.
- Enquete, caixinha e link **não podem ser agendados** no Zernio. Isso vira story real, que a Joana grava no app. Sugira 2 ou 3 ideias por dia na linha da sequência, sem publicar por ela.
- Só a marca DNA.IA. Sem preço, sem Floripa, sem número inventado.

## Onde gravar no Notion

O tipo **Stories** já existe no banco [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0). Uma linha por sequência, fora das 42:

- Códigos: `AAAA-SNN-DIA-S1` (primeira sequência do dia) e `AAAA-SNN-DIA-S2` (segunda).
- Tipo = "Stories". CTA = "Interação". Responsável = "Social Media". Formato vazio (não crie opção nova no schema).
- No corpo da linha: data de publicação, tema, fonte (veículo e data, Diário (data) ou "sem fonte externa"), os até 2 textos exatamente como vão para a tela, uma nota interna sobre como a interação deve nascer (nunca vai para a tela), o horário previsto e, depois, o link das imagens e o ID do post no Zernio.

Quem cria as 14 linhas é a skill `dna-curadoria-2`. Se alguma linha não existir, volte para a Curadoria.

## Visual e script (texto nativo)

Não use `peca_social.py story` neste formato; ele só entra se o intake de **outro cliente** pedir arte da marca.

Script oficial: `python3 /workspace/playbook/scripts/stories_nativo.py SPEC.json SAIDA_DIR` (ou a função `render_frame` do mesmo módulo, como em `/workspace/pilotos-v2/stories/build.py`).

- 1080×1920, fundo preto sólido `#000000`, texto branco `#FFFFFF` centralizado.
- Fonte: `/workspace/fonts/InstagramSans-Regular.ttf`. Nunca outra.
- Margem lateral 96 px. O texto fica fora dos 260 px de cima e de baixo.
- Corpo de 62 pt, diminuindo até 44 pt para caber. Se não couber em 44 pt, encurte o texto, não force a fonte.

Gere a folha de contato de cada dia, com o código, o dia, o horário, o tema e a fonte no cabeçalho da folha (a folha é interna; a fonte na folha não vai para o story).

## Passo a passo

1. **Conferir o texto.** Abra as 14 linhas `-S1`/`-S2` e a `-C1` de cada dia. Confira: datas da semana-alvo; um tema por sequência; tema diferente do carrossel do dia; no máximo 2 stories e 2 blocos por story; tom informal de dia a dia; **zero CTA explícito**; **zero parêntese de fonte**; fonte registrada na linha. Se o texto estiver formal, com pedido explícito ou com parêntese, reescreva no tom desta skill (você tem autonomia para isso) e registre na linha.
2. **Arte.** Gere as imagens e as folhas de contato. Abra cada imagem e confira fundo, fonte, margem, área segura e leitura.
3. **Aprovação.** Mande a semana no chat do Grok Bot com a Joana: uma folha por dia, com tema e horário. Nada é agendado antes do OK escrito dela. Ajuste só o que ela pedir.
4. **Agendamento no Zernio** (só depois do OK, por sequência).
   - Horários fixos no @joanastanieski (America/Recife, UTC-3): segunda a sexta, 12h30 e 20h; sábado e domingo, 13h e 20h.
   - Os stories de uma sequência saem com 1 minuto de intervalo (:00 e :01).
   - `posts_create_post` com horário ISO com offset e o timezone do cliente. Nunca "publicar agora". Se der erro ou timeout, rode `posts_list` antes de tentar de novo.
5. **Stories reais.** Na mesma mensagem de aprovação, liste as ideias de enquete, caixinha ou bastidor do dia. A Joana grava no app.
6. **Registro.** Etapa "10 Arte", depois "13 Aprovação Joana" e "14 Agendado", com o link das imagens e os IDs do Zernio. Feche com `STATUS: PRONTO | BLOQUEADO | RETRABALHO — <código> — <motivo em 1 frase>`.

## Métricas (para o Painel da semana)

Fontes: Zernio (`analytics_get_analytics`) e Instagram Insights. O que faltar entra como "sem dado": alcance por sequência, saída no primeiro story, respostas no direct, votos e perguntas (quando houver story real).

## Autochecagem (todas sim)

- Datas da semana-alvo, nenhuma no passado?
- 14 sequências, 2 por dia, um tema da Curadoria por sequência, diferente do `-C1`?
- No máximo 2 stories e 2 blocos curtos por story?
- Soa informal, de dia a dia, feito na hora, sem erro de ortografia?
- Zero pedido explícito (comenta, clica, responde, manda, vota, salva, link)?
- Zero referência entre parênteses na tela? Fonte registrada na linha?
- Texto nativo (preto, Instagram Sans, área segura), sem logo?
- Nada agendado antes do OK escrito da Joana?
- Número só com fonte? Só DNA.IA? Sem preço e sem Floripa?

## Guardrails

- Toda notícia tem fonte registrada. Não invente nem arredonde fato.
- Não agende nada sem a aprovação escrita da Joana. Nunca "publicar agora".
- Não use Dust nesta etapa.
- Imagem de terceiros só com autorização.
