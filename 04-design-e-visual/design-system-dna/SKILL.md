---
name: design-system-dna
description: >-
  Use ao criar ou revisar qualquer peça visual da DNA (DNA.IA, DNA.RH,
  DNA.TECH): carrossel do Instagram, capa de Reel, legenda queimada, landing
  page, site, tela da Plataforma, keynote, documento, PDF, proposta,
  fluxograma ou diagrama. Desde 12/11/2026 existe um design system só, a v2
  "Biblioteca da Luz" (sala escura, papel, tinta, âmbar, Newsreader e Work
  Sans). A v1 "direção Produto" (azul, clean, fundo branco) é legado e não
  pode ser usada. Traz os scripts e o checklist antes de entregar.
---
# Design system DNA

Toda peça visual da DNA segue este sistema. Não existe peça "rápida" fora dele.

**Existe um design system só: a v2 "Biblioteca da Luz".** Desde 12/11/2026, por decisão da Joana, ela vale para tudo: carrossel, capa de Reel, legenda queimada, documentos, PDFs, propostas, keynote, landing page, site, fluxogramas e a área do cliente da Plataforma.

A v1 "direção Produto" (azul #1F58F0, clean, fundo branco, Instrument Sans e Geist Mono) é **legado**. Não use, não consulte e não copie dela. Se encontrar uma peça, um script ou uma página antiga nesse visual, não reaproveite: refaça na v2 e avise o seu líder.

Os Stories do @joanastanieski continuam em texto nativo (skill `stories-semanais`). Os motion seguem as referências da skill `motion-reels`.

## Fonte da verdade

- Documento completo: `/workspace/design-system/DESIGN-SYSTEM-v2-biblioteca-da-luz.md`. Ele foi escrito para a Plataforma, e as seções 3 (tokens), 8 (copy) e 10 (faça e não faça) valem para todas as peças.
- Se um valor não estiver no documento, ele é "a definir". Não invente e não puxe da v1.

## Regras fixas para qualquer peça

- **Cores:**
  - Sala #140B06 e madeira #3A2314 / #2A1810 nos fundos escuros. Papel #F7EFE1 (claro #FBF4E8, fundo #EFE3CF) onde se lê. Tinta #1C120A no texto e nos títulos; tinta suave #4A3728 no texto longo; marrom #6B5440 nos metadados.
  - Âmbar #E8B04C só no que a luz toca: o destaque, a ação principal, o número-chave. Âmbar de texto #8A5A1E nos rótulos pequenos em caixa alta.
  - Verde #3F6B3A e vermelho #9A3A1E só em texto de estado ou número.
- **Fontes:** Newsreader nos títulos, nas datas grandes e nos números de destaque (500, -0,015em). Work Sans no texto, nos botões, rótulos e metadados (400 e 600).
- **Proibido:** branco puro, preto puro, azul #1F58F0, cinza frio, Instrument Sans, Geist Mono e Montserrat. Também não pode borda em volta de cartão, caixa dentro de caixa, ícone decorativo ou emoji como ícone.
- **Separação:** espaço e fio de 1 px em rgba(28,18,10,.10). O destaque é um bloco em papel fundo, sem contorno.
- **Logo Régua:** continua, nos arquivos de `/workspace/design-system/logo/` e sem redesenhar. Use papel #F7EFE1 sobre a sala e tinta #1C120A sobre o papel. Corte a partir de 48 px de altura; abaixo disso, a versão pequena.

## Documentos, PDFs, propostas e keynote

- Página em papel #F7EFE1. Capa e divisórias podem usar a sala #140B06 com o texto em papel.
- Título em Newsreader e texto em Work Sans 15 a 16 px, com line-height 1,5. Rótulo de seção (eyebrow) em Work Sans 11 px, caixa alta, 600, em âmbar de texto.
- Preço, prazo e número-chave em Newsreader. O âmbar aparece em no máximo um destaque por página.
- Gere em HTML e exporte para PDF; abra cada página em PNG e confira antes de entregar.

## Capa de Reel

- `python3 /workspace/playbook/scripts/capa_reel.py VIDEO "Frase de 3 a 5 palavras" SAIDA.jpg --t <segundo> [--tag "ETIQUETA"] [--logo IA]`. O script já vem na v2: frase em Newsreader na cor papel, etiqueta em Work Sans e sombra na cor da sala.
- Use o bruto, não o editado, para a legenda queimada não aparecer. Abra o `_200px.jpg`: se não der para ler, encurte a frase.

## Legenda queimada

- Work Sans, sem caixa e sem contorno colorido: `editar_reel.py ... --font "Work Sans"`.

## Fluxogramas

- `python3 /workspace/playbook/scripts/fluxograma.py SPEC.json SAIDA.png` já usa a v2 como tema padrão. O tema também está em `/workspace/playbook/temas/biblioteca-da-luz.json`.

## Carrossel do Instagram: v2 "Biblioteca da Luz"

**Documento-fonte:** o design system v2 da plataforma (`/home/box/agent-data/agents/4694c20c-2671-430f-8c9a-ee2b5cda0350/attachments/72d2b032360220b324d5e49eacc51c640edeb85a0d16ba914a079fa17f341be4.md`). No carrossel ele é adaptado para chamar atenção no feed.

**Script oficial:** `python3 /workspace/playbook/scripts/carrossel_biblioteca.py SPEC.json SAIDA_DIR`. Ele gera um PNG de 1080×1350 por slide e a folha de contato. Os modelos aprovados estão em `/workspace/playbook/carrossel-biblioteca/` (`exemplo-QUA.json`, `exemplo-SEG.json`, as imagens em `img/` e os PNGs prontos).

**SPEC.** `{"code": "...", "slides": [...]}`. Cada slide tem:

- `tipo`: `capa`, `imagem`, `papel` ou `fecho`.
- `img`, o caminho da imagem do slide, e `focus`, de 0 a 1, que indica onde cortar na vertical.
- `titulo`, com `<em>` para destacar em âmbar o número ou a palavra-chave.
- `texto`, opcional.
- `lista`, opcional, com `<b>` permitido.
- `fonte`, opcional e pequena, só no slide do dado.
- `nota`, que é a direção interna e **nunca é renderizada**.

Só `titulo`, `texto`, `lista` e `fonte` vão para a arte, e eles vêm do campo "na arte" da copy (skill `dna-copy-2`).

**Visual:**

- Fundo sala `#140B06`. O texto sobre a imagem fica em papel `#F7EFE1`, e o apoio em papel a 86%.
- Âmbar `#E8B04C` só em destaque: o número, o "1." do passo, os marcadores da lista e a seta da capa.
- Cartão de papel `#F7EFE1` com tinta `#1C120A`, raio de 22 px e sombra funda, só nos slides "como aplicar" (`papel`) e no fecho.
- Títulos em Newsreader 500 (opsz 72, -0,015em): de 112 a 124 px na capa e de 92 a 104 px nos slides internos. Texto em Work Sans 400, com 42 px.
- A imagem ocupa o topo do slide, de 760 a 880 px, ou o slide inteiro na capa, e se funde na sala por um degradê escuro. O texto fica embaixo.
- Margem lateral de 80 px. Nada de caixa com contorno, ícone decorativo, emoji, azul `#1F58F0`, branco puro ou preto puro.

**Imagens ilustrativas (obrigatórias).**

- Todo slide tem imagem, e ela é criada com GenerateImage. Por padrão, **sem foto da Joana** ("sem foto minha, cria a imagem", 10/11/2026).
- O estilo é a biblioteca cinematográfica: madeira escura, veludo, estantes de livros, abajur e velas, luz âmbar de fim de tarde e poeira no feixe de luz.
- Cada slide traz **um objeto-metáfora** do que ele diz: uma etiqueta só iluminada para "um número só", uma chave entre várias para "uma mudança", relógio e calendário para "prazo", pergaminhos empilhados para "transcrição".
- A imagem não tem pessoas nem texto escrito. Deixe espaço escuro embaixo para o texto.
- Para manter a unidade, use `/workspace/playbook/carrossel-biblioteca/ref-sala-dir.jpg` e `ref-sala-esq.jpg` como referência de estilo.
- Gere a imagem, abra e confira. Se tiver texto, gente ou objeto errado, gere de novo.

**Leitura sem esforço.**

- Cada slide tem uma ideia só: o título carrega a ideia, e o texto tem no máximo 2 frases curtas ou uma lista de até 4 itens.
- Nenhum rótulo interno vai para a arte: função do slide, pilar, "contexto", "liderança", "o que o Sebrae viu" ou direção de arte. Se aparecer, o problema está na copy: volte para `dna-copy-2` em vez de cortar no olho.


## Passos

1. Identifique o formato: carrossel, capa, documento, fluxograma ou tela. Stories são texto nativo.
2. Gere a peça com o script oficial do formato, sempre na v2.
3. Abra a imagem final e confira cada item do checklist. Corrija e gere de novo até passar.
4. Peças que vão para fora da DNA seguem a skill `envio-via-lais`.

## Checklist de qualquer peça

- [ ] Só cores da v2. Nenhum azul, branco puro, preto puro ou cinza frio.
- [ ] Newsreader nos títulos e Work Sans no texto. Nada de Instrument Sans, Geist Mono ou Montserrat.
- [ ] Âmbar só no destaque, no máximo um por bloco.
- [ ] Zero borda em cartão, caixa dentro de caixa ou ícone decorativo.
- [ ] Logo Régua na cor e na versão certas para o tamanho.
- [ ] Todo valor fora do documento da v2 foi sinalizado como "a definir".

## Checklist do carrossel (v2)

- [ ] Sala #140B06, papel #F7EFE1, tinta #1C120A, âmbar #E8B04C só em destaque. Nenhum azul, branco puro ou preto puro.
- [ ] Newsreader nos títulos e Work Sans no texto.
- [ ] Todo slide tem imagem ilustrativa criada, sem foto da Joana, sem pessoas e sem texto na imagem, no estilo da biblioteca.
- [ ] Só o texto "na arte" da copy aparece. Zero rótulo, nota ou função do slide.
- [ ] Uma ideia por slide, leitura em poucos segundos.
- [ ] Cartão de papel só no "como aplicar" e no fecho.
- [ ] Folha de contato gerada e conferida.

