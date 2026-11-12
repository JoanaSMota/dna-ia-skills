---
name: dna-materiais-pdf
description: >-
  Use na etapa de Materiais em PDF da Esteira, só depois de a Joana liberar esta
  skill e de o Painel estar aprovado, para transformar peças que já performaram
  em conteúdo e especificação página a página de um PDF prático. Não gera o
  arquivo final e está vetada até a Joana liberar.
---
# DNA-Materiais-PDF

**Uso vetado até a Joana liberar.** A Joana confirmou a Esteira e a rotina de domingo, mas deixou o DNA-Materiais-PDF de fora. Se esta skill for aberta antes da liberação, pare imediatamente, não produza material, grave BLOQUEADO com o motivo "uso vetado até a Joana liberar" e feche com a linha de STATUS. Não chame o agente do Dust nem diagrama nada.

Agente do Dust: `DNA-Materiais-PDF` (JAdXpUpBb3). Quando for liberado, quem roda esta skill na esteira do @joanastanieski é o bot Social Media e Comunidade.

## Objetivo

Transformar conteúdos que já foram criados e publicados no perfil @joanastanieski em materiais práticos em PDF (iscas, guias, checklists, modelos prontos, autodiagnósticos), para ampliar o repertório além do "Mapa das 5 Rotinas". Esta etapa escreve o conteúdo e a especificação página a página. Quem diagrama e gera o PDF final é o bot Social Media e Comunidade, no design system oficial. Não afirme que gerou o arquivo.

Ritmo da fonte: 1 material a cada 1 ou 2 semanas. Qualidade acima de volume.

Perfil: @joanastanieski, primeira pessoa, direta, provocadora e bem-humorada. Público: empresário e líder de PME (até R$ 15 milhões por ano) que quer usar IA no negócio. Conceito: o agente prepara, o humano decide. A DNA aparece como prova e bastidor, nunca como anúncio.

## Entradas

Só comece com o [Painel da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580) em "Aprovado" ou "Aprovado com ajustes". Sem Painel aprovado, devolva BLOQUEADO.

Leia:

1. O [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0) e o Painel aprovado (ranking por salvamento e compartilhamento).
2. As linhas das peças de origem em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0): código, tese, gancho, roteiro/copy, links.
3. [Banco de Teses](https://app.notion.com/p/3c04ae3a7397456eb0c1784d1bc24ac8), a voz da Joana e a [página de CTAs](https://app.notion.com/p/4133799773078106ae53f481bab95cb4).
4. A skill `design-system-dna` (v2 Biblioteca da Luz, único design system vigente desde 12/11/2026).

Na linha do material (Tipo = "Material PDF", código no padrão 2026-S47-PDF1): leia Etapa e Status. Se a linha não existir, crie uma com esse código; nunca duplique. Nenhuma etapa começa sem ler a linha.

Sem dado de salvamento ou compartilhamento no Painel, não escolha peça de origem: grave BLOQUEADO.

## Passos

1. Leia o Painel aprovado e escolha 1 a 2 peças de origem com melhor salvamento/compartilhamento. Sem número no Painel, não produza.
2. Defina o tipo de material pela tese: checklist, passo a passo, autodiagnóstico, modelo pronto, certo x errado, guia curto. Um problema, uma entrega prática.
3. Escreva na voz da Joana, em primeira pessoa.
4. Estruture página a página (capa, 3 a 8 páginas de miolo, página final com próximo passo). Cada seção precisa ser acionável, não só descritiva.
5. Todo número, fato, caso ou ferramenta citado traz a fonte (veículo, link, data) ou a peça de origem. Sem fonte: "sem dado" / "a verificar" e fora do texto final.
6. Especifique o visual pela v2 Biblioteca da Luz (skill `design-system-dna`): página em papel #F7EFE1, capa e divisórias na sala #140B06, texto em tinta #1C120A, metadados em marrom #6B5440, âmbar #E8B04C só no destaque; Newsreader nos títulos e Work Sans no texto; sem borda em cartão, sem caixa dentro de caixa, sem ícone decorativo (separar com fio de 1 px e espaço); logo Régua DNA.IA em tinta sobre o papel. Nada de azul, branco puro ou da v1 Produto, que é legado.
7. Proponha como o material chega ao público SEM criar palavra-chave nova: hoje só existe ROTINA, e ela é exclusiva do Mapa das 5 Rotinas. Palavra-chave nova ou automação nova só com OK da Joana: deixe como pendência, marcada "PROPOSTA — precisa do OK da Joana". Enquanto não houver OK, o CTA da peça de lançamento é SALVAR ou COMPARTILHAR.
8. Não reaproveite o Mapa das 5 Rotinas como se fosse novo.

A revisão é do Social Media (na fonte deste agente, não existe etapa "Revisão CMO"). O OK final é da Joana.

## Formato de saída

```
# Material PDF [código] — [título]
Peças de origem: [códigos] | Motivo (Painel): [salvamentos/compartilhamentos com fonte]
Tipo: [checklist | passo a passo | autodiagnóstico | modelo pronto | certo x errado | guia]
Promessa (1 frase):

## Páginas
| # | Título | Texto | Elemento visual (do design system) |

## Fontes
- [fato] — [fonte, link, data]

## Distribuição proposta
- [sem palavra-chave nova; pendências para a Joana]

## Pendências
- [item] — a verificar com: [quem]

Revisão: Social Media | Aprovação final: Joana
```

Autochecagem, todas sim:

- O material resolve um problema só, com entrega prática?
- Veio de peça que performou no Painel, com o número e a fonte?
- Todo fato tem fonte; nada inventado?
- Voz da Joana em primeira pessoa?
- Visual só com o Design System DNA (oficial)?
- Nenhuma palavra-chave nova, nenhum preço, nenhuma marca além de DNA.IA?
- Terminei com a linha de STATUS?

## O que gravar no Notion

Na linha do material em Peças:

- Etapa = a etapa vigente do material (não use "Revisão CMO": a revisão é do Social Media)
- Status = "Pronto para a próxima", "Bloqueado" ou "Retrabalho"
- Link do conteúdo
- Peças de origem e, se houver, a palavra-chave proposta
- Motivo, se bloqueou

Feche sempre com:

`STATUS: PRONTO | BLOQUEADO | RETRABALHO — <código do material> — <motivo em 1 frase>`

Enquanto o uso estiver vetado, a linha de STATUS é BLOQUEADO, com o motivo da vedação.

## Guardrails

- Uso vetado até a Joana liberar.
- Número só com fonte. O que faltar, escreva "sem dado". Sem número no Painel, não produz. Nunca invente número, caso, depoimento, URL ou ferramenta.
- Só a marca DNA.IA. Sem DNA.RH nem DNA.TECH.
- Nada de preço nem de data de evento sem confirmação. Sem Florianópolis. Nunca criar ou citar EVENTO, EU QUERO ou COMERCIAL. ROTINA só no Mapa das 5 Rotinas. Nenhuma palavra-chave nova sem OK da Joana.
- Nada é publicado, agendado ou enviado sem o OK da Joana.
- Um passo por vez. Nenhuma etapa começa antes de o Painel ser aprovado pela Joana.
- Não afirme que gerou o PDF. Não crie palavra-chave nem automação. Não use cor, fonte ou elemento fora do design system.
