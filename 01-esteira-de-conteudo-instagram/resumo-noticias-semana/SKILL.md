---
name: resumo-noticias-semana
description: >-
  Use quando a Joana pedir "minhas notícias", um resumo das notícias da semana
  ou quiser se atualizar sobre o mercado de IA, inclusive numa ligação: lê a
  Pesquisa mais recente da esteira (ou roda uma nova) e entrega um resumo pronto
  para ser lido em voz alta.
---
# Resumo de notícias da semana

Serve para manter a Joana atualizada sobre o mercado de IA, automação e agentes ao longo da semana, a partir da Pesquisa da esteira. Funciona por chat e por ligação.

## 1. Achar a pesquisa

1. Procure a página de Pesquisa mais recente da esteira no Notion: as subpáginas da [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac), ou o campo "Link da pesquisa" da semana em [Painéis da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580).
2. Se a pesquisa mais recente tiver mais de 7 dias, ou se a Joana pedir novidades de hoje, rode a skill `dna-pesquisa-2`. Neste uso, ela pede só o OK da Joana para pesquisar (o próprio pedido de notícias já conta) e não abre nenhuma etapa da esteira.
3. Itens novos que saíram depois da pesquisa entram só se você conferir data e fonte na própria página.

## 2. Montar o resumo

- Agrupe em cinco blocos: tendências; ferramentas; regulação e riscos; dados; casos de empresas.
- Para cada item, use uma ou duas frases faladas: o que aconteceu, o número principal (só se tiver fonte), o veículo e o dia. Exemplo: "A Uber disse que só 4 corridas foram pedidas por agentes de IA, num total de 320 milhões. TechCrunch, dia 4."
- Itens do X são opinião: diga "termômetro do X". Itens "a verificar" são ditos como "ainda a verificar".
- Pedido de resumo curto: os 6 a 8 itens mais fortes. Pedido de "ler tudo": todos, numerados.

## 3. Entregar

- **Na ligação**: frases completas, sem markdown, sem link e sem símbolo. Escreva números e porcentagens por extenso ("57 por cento"). Termine dizendo que a lista completa, com os links, está na página da Pesquisa no Notion.
- **No chat**: uma frase de abertura e depois os itens como lista, cada um com o link da fonte.
- Se a ligação acabar, mande no chat uma mensagem curta com o link da página.

## Guardrails

- Número só com fonte. Nunca invente notícia, data ou veículo.
- O resumo é só para a Joana. Nada é publicado, enviado a terceiros ou vira peça sem o OK dela.
- Ler ou resumir a pesquisa não inicia a Curadoria nem nenhuma outra etapa da esteira.
