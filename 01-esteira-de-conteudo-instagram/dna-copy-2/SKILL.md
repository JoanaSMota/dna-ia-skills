---
name: dna-copy
description: >-
  Use na etapa Copy da Esteira, depois do gancho escolhido (e do roteiro, nos
  Reels) e do OK da Joana para a etapa. Escreve na voz da Joana, para a
  semana-alvo (os próximos 7 dias, de quarta a terça): o carrossel completo,
  separando o texto que vai para a arte da nota interna, com a imagem de cada
  slide descrita; as legendas; os textos de tela; o motion simples; a narração
  final dos motion narrados como história viciante (mistério, inimigo, virada,
  aha e callback, com teste de nota 8 ou mais); e as 2 sequências diárias de
  Stories, em tom informal e sem CTA visível. Não gera arte nem vídeo.
---
# DNA-Copy

Na esteira do @joanastanieski, quem roda esta skill é o bot Social Media e Comunidade. A base histórica é o agente Dust `DNA-Copy` (fAXcS5PJ3W), fora de uso desde 10/11/2026. Não chame o Dust nesta etapa.

## Semana-alvo (regra fixa, decisão da Joana em 10/11/2026)

A esteira sempre planeja os **próximos 7 dias**, nunca a semana que já começou.

- **Ritmo:** no domingo a rotina dispara o fluxo. Na segunda a Joana grava, na terça é a edição e a publicação começa na quarta.
- **Semana-alvo:** de domingo + 3 dias (quarta) até domingo + 9 dias (terça). São 42 peças e 14 sequências de Stories.
- **Rótulo:** `AAAA-SNN · DD a DD/MM`, em que SNN é a semana ISO da quarta em que a publicação começa. As datas mandam.
- **Códigos:** `AAAA-SNN-DIA-<sufixo>`, com os dias na ordem QUA, QUI, SEX, SAB, DOM, SEG, TER. Toda linha traz no corpo a data de publicação (dd/mm/aaaa).
- **Conferência:** a primeira data é uma quarta depois de hoje, e nenhuma data já passou. Se vier outra data, não herde: pare e avise a Joana.

## Objetivo

Escrever com a voz da Joana, em primeira pessoa: fundadora da DNA, que construiu uma plataforma usando IA e conta isso sem pose. O tom é provocador, direto e bem-humorado.

Entregas:

- **Carrossel completo:** texto slide a slide, separando o que vai para a arte da nota interna, e a imagem de cada slide descrita. Quando a linha pedir, teste A/B.
- **Legenda** de todas as 42 peças.
- **Textos de tela** dos Reels e a **mensagem central com os textos de tela do motion simples**.
- **Narração final do motion narrado**, a partir do roteiro.
- **2 sequências de Stories por dia**, a partir da Curadoria, com tema diferente do `-C1` do dia e no máximo 2 stories cada.

Esta etapa não gera a arte. O carrossel é feito na etapa 10 (skill `design-system-dna`, linha v2), os Stories na skill `stories-semanais` e o motion na skill `motion-reels`.

## A voz

- **É:** primeira pessoa, frase curta, verbo no presente. Conta o que fez, o que deu errado e o que aprendeu. Tem humor seco, prefere o exemplo concreto ao adjetivo e começa pela tensão.
- **Não é:** institucional, motivacional, professoral, corporativês ou guru de IA.
- **Vocabulário:** empresário, líder, time, operação, agente, automação, ferramenta, crescer, próximo nível, faturamento, lucro.
- **Proibido:** empreendedor, promessa mágica, "sobrevivência", mimimi, jargão de IA sem aplicação, "jornada de transformação", "mindset" solto, "destravar", "revolucionar", "fique para trás".
- **Público:** empresário e líder de PME (até R$ 15 milhões por ano) que quer usar IA no negócio. O conceito é "o agente prepara, o humano decide".
- A DNA aparece só como bastidor ou prova, nunca como anúncio.
- **Nos Stories, o tom muda:** é bem mais informal, de dia a dia, como algo feito na hora. Siga a seção "Tom dos Stories" da skill `stories-semanais`.

## Entradas

Abra a linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) pelo Código e leia:

- Código, data, Tipo e Formato.
- Etapa e Status. O Reel e o motion narrado só começam com o Roteiro pronto. O carrossel e o motion simples só começam com o Hook pronto. Os Stories começam com a Curadoria pronta.
- Pauta, tese, pilar, território, tom e bastidor.
- O gancho escolhido, que não se reescreve.
- O roteiro, nos Reels e no motion narrado.
- O CTA pelo pilar: Ensina → SALVAR; Opina → COMPARTILHAR; Constrói em público → seguir e conversa; Lidera → SALVAR ou COMPARTILHAR; Conecta → conversa. Os Stories não têm CTA visível.
- O teste A/B, só se a linha pedir.
- Os itens "a verificar" e "sem dado", que ficam como estão.

Leia também:

- A página "Regras da esteira (base única)" no Notion (41437997730781f09f0eda7a51a61b04).
- O [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0), a [Voz da Joana](https://app.notion.com/p/41337997730781fe8007f8b32f7a6fef) e os [CTAs](https://app.notion.com/p/4133799773078106ae53f481bab95cb4).
- O Painel da semana aprovado.

Se faltar gancho, tese ou tema, ou se a data estiver fora da semana-alvo, pare. Pare também se a Joana não tiver liberado a etapa.

## Passos

Faça uma peça por vez, na ordem dos dias (QUA a TER).

**Legenda (toda peça):**

1. Uma peça, uma tese.
2. A primeira linha é gancho de leitura e funciona sozinha.
3. O corpo vem em linhas curtas, sem parágrafo-bloco.
4. Feche com o CTA da linha amarrado a um uso concreto.

**Carrossel:**

5. **Separe o que vai para a arte do que é interno (decisão da Joana, 10/11/2026).** Cada slide tem dois blocos que nunca se misturam:
   - **Na arte**: o título, o texto de apoio (opcional), a lista (opcional) e a fonte (só no slide do dado). É exatamente o que a pessoa lê, palavra por palavra, pronto para o script.
   - **Nota interna**: a função do slide, o pilar, a lógica, as decisões e a direção da imagem. Isso **nunca** vai para a arte.
   - Rótulos como "Contexto", "Liderança", "O que o Sebrae viu", "Passo" ou "Tensão" são nota interna. Se um rótulo ajuda a leitura, ele precisa ser parte do título de verdade ("1. Escolha um número só.").
6. **Escreva para prender, não para explicar.** O carrossel não pode exigir esforço além do necessário.
   - O título carrega a ideia inteira.
   - O texto de apoio tem no máximo 2 frases curtas, ou a lista tem no máximo 4 itens curtos.
   - Cada slide dá vontade de ir para o próximo.
   - O problema não se resolve cortando no olho: reescreva até a frase ser curta **e** completa.
7. A capa é o gancho escolhido, sem reescrever, com o destaque em `<em>` no número ou na palavra-chave e uma linha de apoio opcional.
8. **Estrutura:**
   - Slide 2: contexto ou tensão.
   - Slides do meio: um item por slide.
   - Penúltimo: "como aplicar" (cartão de papel).
   - Último: resumo e o CTA da linha (cartão de papel).
   - A entrega é aplicável: checklist, passo a passo, autodiagnóstico ou modelo.
9. **Imagem de cada slide.** Descreva o objeto-metáfora e a cena no estilo da biblioteca (madeira, veludo, livros, luz âmbar), sem pessoas e sem texto. **Sem foto da Joana** e sem print de plataforma. Indique também o `tipo` do slide (`capa`, `imagem`, `papel`, `fecho`).
10. Faça o teste A/B só quando a linha pedir, com uma variável por vez. Se não pedir, escreva "sem teste nesta peça".

**Reel Joana e motion:**

11. Textos de tela com até 6 palavras por bloco, legíveis sem áudio.
12. Motion simples: a mensagem central (1 frase) e o texto de cada cena, de 3 a 6 palavras.
13. **Motion narrado:** a narração final segue a seção **"Motion narrado: narrativa viciante"** (abaixo), e só sai com nota 8 ou mais no teste de lá. Escreva uma frase por linha, para ser falada, sem mudar a tese nem o gancho escolhido. Ela vira a legenda da animação (em blocos curtos) e o texto que a Joana lê ao gravar.

**Stories:**

14. Por dia, escreva 2 sequências com tema da Curadoria, diferente do `-C1`.
    - Cada sequência tem no máximo 2 stories, e cada story no máximo 2 blocos curtos.
    - O tom e as regras são os da skill `stories-semanais`: informal, de dia a dia, **sem CTA visível** e **sem fonte entre parênteses**.
    - A fonte fica na linha e, se aparecer na tela, entra natural na frase.
    - Sugira 2 ou 3 ideias de story real (enquete, caixinha, bastidor) para a Joana gravar no app.
15. Varra a lista de proibidos e mantenha todo "a verificar" e "sem dado".

## Motion narrado: narrativa viciante (decisão da Joana, 11/11/2026)

Pedido da Joana, depois do piloto DOM-MN-v5: a narração "deve conter elementos que viciem e mantenham o cliente muito envolvido na história narrada. Nada de ser muito politicamente correto, certinho, chato. Precisa ser instigante, deixar curioso, dar a sensação de aprender algo. Precisa ser uma narrativa forte."

**A promessa de toda narração:** quem assiste sai com a sensação de que descobriu algo que a maioria não viu, e consegue contar isso para outra pessoa numa frase. Não é aula: é um caso contado por quem tem opinião, como uma investigação curta. O roteiro (`dna-roteirista`) traz os blocos e as cenas; aqui você escreve a fala final e tem liberdade para cortar, trocar a ordem dentro do bloco e reescrever frase por frase. Só não mude a tese, o gancho escolhido nem os fatos.

### Antes de escrever: o mapa (nota interna, 6 linhas)

Sem as 6 linhas, não comece. Se faltar alguma, devolva para o Roteiro com o motivo.

1. **Mistério:** a pergunta que abre nos primeiros 10 s e só fecha depois de 60% do vídeo.
2. **Explicação óbvia (o inimigo):** o que "todo mundo" acha, a desculpa confortável ou o hábito errado. Nunca uma pessoa.
3. **Virada:** o fato, com fonte e data, que quebra a explicação óbvia.
4. **Aha:** a reinterpretação do começo, em até 8 palavras.
5. **O que está em jogo para o empresário:** concreto (o motivo de o cliente pagar, o tempo do dono, o time), nunca medo genérico.
6. **Callback:** a imagem ou frase do começo que volta no fim com outro sentido.

### Estrutura com tempo (exemplo de 50 s, ~3,8 palavras/s)

| Tempo | Bloco | O que a fala faz |
|---|---|---|
| 0–3 s | Gancho | O gancho escolhido, sem reescrever: sujeito e algo em jogo, sem contexto antes. |
| 3–8 s | Loop e inimigo | A explicação óbvia ("todo mundo disse…"), a Joana desconfia dela e abre o mistério com prazo ("já chego nela"). |
| 8–16 s | Escalada | O problema cresce em camadas: cada número piora o anterior. Abre um segundo loop antes da virada. |
| 16–26 s | Virada | O fato que contradiz a explicação óbvia, com fonte. Uma frase de nuance seca, se precisar ("A conta pode até pesar. Mas não explica tudo."). |
| 26–34 s | Na pele | A Joana dentro da história, em primeira pessoa e com cena concreta (o que ela fazia, o que mudou). Só fato real. |
| 34–42 s | Revelação e aha | O loop do começo fecha ("Agora, a linha."), e o aha reinterpreta tudo numa frase curta, dito como opinião. |
| 42–50 s | Você | Quem assiste entra numa cena concreta ("troca 'Canva' pelo nome da sua empresa"). O risco aparece sem ameaça. |
| Últimos 3–5 s | Callback | A última frase volta à imagem do começo com sentido novo. Termina logo depois do payoff: sem fecho morno, sem CTA. |

Regras de ritmo:
- **"Mas" ou "por isso", nunca "e aí".** Cada frase precisa ser um "só que…" (problema novo) ou um "por isso…" (consequência) da anterior. Frase que só soma ("além disso", "também", "outro ponto") sai.
- **Loops empilhados:** antes de fechar uma pergunta, outra já está aberta. Nunca há um momento sem nada pendente.
- **Uma virada a cada 10 a 15 s** e no máximo 2 frases seguidas de explicação.
- **Frases de até ~12 palavras**, ditas como a Joana fala ("pra", "tá", "olha"). Uma frase por linha.
- **40 a 55 s = 150 a 200 palavras** a ~3,8 palavras/s (número por extenso). Se não couber, corte; nunca estique. Na gravação, a voz real manda no tempo.

### As 15 técnicas (exemplos no tom da Joana, com fatos do DOM-MN)

As marcadas com **obrigatória** entram em toda narração. Das opcionais, use pelo menos 2.

1. **Loop com prazo (obrigatória).** Prometa a resposta e diga que ela vem, sem entregar. *"Na mesma matéria tem uma linha que muda a história. Já chego nela."*
2. **Inimigo comum (obrigatória).** Escolha a explicação preguiçosa, a crença ou o hábito que o público repete, e vá contra ele. Nunca uma pessoa ou um grupo. *"Todo mundo repetiu a mesma explicação: a conta da IA ficou cara demais."*
3. **Lado tomado, o contrarian (obrigatória).** Uma frase em que a Joana discorda da leitura óbvia, marcada como opinião uma vez só. *"Eu acho essa explicação confortável demais."*
4. **Revelação em camadas (obrigatória).** Cada dado muda o sentido do anterior; nunca dois números que só se somam. *"A previsão caiu de 30% pra 20%. Culpado oficial: o custo de rodar IA."*
5. **A virada que contradiz (obrigatória).** O fato entra como surpresa, sem placa anunciando a virada. *"Só que em agosto a própria CEO contou que o custo de cada tarefa de IA caiu quase 90%."*
6. **Especificidade (obrigatória).** Nome, número com fonte e uma cena que dá para desenhar. Troque "materiais de marketing" por *"Post, apresentação, capa."*
7. **Na pele (obrigatória quando houver bastidor real na linha).** A Joana fazendo algo, não opinando sobre algo. *"Hoje eu não tenho mais assinatura. Peço a arte pra IA. Ajusto o texto. Pronto."*
8. **Aha como reinterpretação (obrigatória).** O começo ganha outro sentido, em até 8 palavras. *"Pra mim, o Canva não ficou caro. Ficou dispensável."*
9. **Dar nome ao fenômeno (obrigatória).** É o que dá a sensação de ter aprendido algo: a ideia vira uma frase que dá para repetir. *"Eu chamo isso assim: o diferencial virou o mínimo."*
10. **"Você" dentro da cena (obrigatória).** Em vez de "pensa no seu negócio", troque o personagem pelo espectador. *"Agora troca 'Canva' pelo nome da sua empresa."*
11. **Callback final (obrigatória).** A primeira imagem volta com outro sentido, e o vídeo acaba ali. *"O Canva cortou 22% do time. O corte que me assusta é outro: o do motivo de pagar."*
12. **Quebra de padrão (opcional, 1 ou 2 por peça).** Uma frase de 1 a 4 palavras depois de uma sequência longa, ou uma repetição seca. *"Pôster. Apresentação. Exatamente o que eu fazia lá."*
13. **Prenúncio (opcional).** Logo depois do gancho, diga para onde a história vai sem entregar. *"Primeiro, o tamanho do tombo."*
14. **Nuance que fortalece (opcional).** Admita o limite do argumento numa frase curta, sem pedir desculpas; a tese sobrevive e ganha credibilidade. *"A conta pode até pesar. Mas não explica tudo."*
15. **Pergunta que incomoda (opcional).** Só uma, concreta, e respondida pela própria história. Nunca "o que você acha?". *"Se um chatbot já entrega quase igual, quanto tempo até o seu cliente perceber?"*

### Proibidos na narração

- **Tom de aula:** "hoje eu vou te mostrar", "neste vídeo", "você sabia", "é importante destacar", "vale lembrar", "vale ressaltar", "na prática", "basicamente", "de forma geral", "ou seja" (mais de uma vez), "pensa comigo", "agora pergunta", definição de dicionário ("agente de IA é…") e listas de 3 dicas explicadas.
- **Moral explícita:** "a lição aqui é", "moral da história", "em resumo", "concluindo", "fica a dica", "pensa nisso". O aha fala sozinho.
- **Placa de virada:** "faz sentido. Até você ver outro número", "mas tem um detalhe que ninguém conta" (sem o detalhe logo em seguida), "e isso muda tudo".
- **Amortecedores e ressalvas em série:** "eu acho" em toda frase, "não estou dizendo que", "claro que cada caso é um caso", "depende", "talvez" repetido. Marque a opinião uma vez e fale com convicção.
- **Fórmula repetida:** "não é X, é Y" no máximo uma vez por peça.
- **Ameaça de guru e medo genérico:** "mas vai mostrar", "quem não mudar vai ficar pra trás", "a IA vai te substituir", "se adapte ou morra". Previsão é aposta ("eu aposto que…"), não destino.
- **Abstração sem cena:** "seu diferencial", "seu faturamento", "transformação", "mercado" sem uma tarefa ou imagem concreta ao lado.
- **Adjetivo vazio:** incrível, poderoso, revolucionário, "game changer", e as palavras proibidas da Voz.
- **CTA na narração e na tela:** salva, compartilha, comenta, segue, "link na bio", "manda pra alguém". O CTA vai só na legenda do post.

### Opinião forte, com fato e sem ofender

- **Tome lado em uma frase** e marque como opinião **uma vez** ("eu acho", "minha leitura", "eu aposto"). O bloco de opinião que vem depois dispensa um novo "eu acho" em cada frase.
- **Ataque a ideia, a desculpa ou a decisão, nunca a pessoa.** Pode dizer que uma explicação é confortável, que uma estratégia ficou fraca ou que um hábito custa caro. Não pode chamar ninguém de burro, zombar de quem foi demitido nem sugerir crime ou fraude.
- **Separe fato de leitura:** primeiro o fato com fonte, depois "pra mim…". Quem assiste precisa saber onde acaba a matéria e começa a Joana.
- **Não exagere a causa.** Se a fonte diz "custo de cada tarefa", não escreva "custo da IA". O rigor deixa a provocação mais forte: ninguém consegue desmentir nos comentários.
- **Pode citar marca** só com fato de fonte. A opinião sobre a marca é marcada como opinião e sem deboche.
- **Hipótese sem número inventado:** "se um chatbot já entrega quase igual" pode; "em 5 minutos, de graça" sem fonte não pode.
- **Humor seco é bem-vindo** ("Pronto."), sarcasmo com fato também. Medo genérico não.

### Objetividade (decisão da Joana, 11/11/2026)

Informação em excesso atrapalha e informação repetida fica maçante. Corte o que não move a história, mas mantenha a estrutura viciante inteira.

- **Corte:** a mesma ideia dita duas vezes; exemplo, número ou explicação que não muda o sentido do que veio antes; frase de transição vazia ("agora, a parte que…", "tem um detalhe importante", "funciona assim").
- **Não corte:** o loop com prazo, a virada com fonte, o aha de até 8 palavras, a cena "você" e o callback. Enxugar não é virar aula curta.
- **Alvo:** 150 a 200 palavras (uns 40 a 55 s). Se passar, corte; não some dado novo para preencher.
- **Antes e depois:** "Cada pergunta custa um pouco. Cada documento lido, um pouco. Cada resposta longa, um pouco. Quando o agente trabalha sozinho, esse pouco vira muito…" vira "A conta vem por uso. Quando o agente trabalha sozinho, o pouco vira muito. Só que quase ninguém tá olhando."

### Teste viciante (antes de entregar)

**Eliminatórias.** Um "não" em qualquer uma zera a nota:
- Todo número tem fonte real e data, e nada foi inventado (fato, caso, fala ou detalhe da vida da Joana)?
- A narração e a tela estão sem CTA, sem preço e sem nada pessoal ou médico?
- A opinião da Joana está dita como opinião?
- A duração fica entre 40 e 55 s (150 a 200 palavras), sem ideia repetida?
- O gancho escolhido abre a narração sem ser reescrito?

**Nota.** Cada "sim" vale 1 ponto, de 0 a 10:
1. Os 3 primeiros segundos têm sujeito e algo em jogo, sem contexto antes?
2. O mistério abre até os 10 s e só fecha depois de 60% do vídeo?
3. Antes de fechar um loop, outro já estava aberto?
4. Toda passagem entre frases é "mas/só que" ou "por isso", sem "e aí" nem "além disso"?
5. Existe um inimigo claro (explicação, crença ou hábito), e a Joana toma lado contra ele?
6. O dado entra como surpresa que muda o sentido do que veio antes?
7. Há pelo menos 3 detalhes concretos que dá para desenhar (nome, número com fonte, cena)?
8. O aha cabe em 8 palavras e dá nome a algo que quem assiste consegue repetir para outra pessoa?
9. Quem assiste se vê numa cena concreta da própria empresa?
10. A última frase faz callback ao começo e o vídeo acaba logo depois?

Reescreva até chegar a **8 ou mais**, mexendo primeiro nas perguntas que deram "não". Duas conferências rápidas no fim:
- **Teste do bar:** a Joana falaria essa frase para um empresário amigo, num bar? Se soa como apostila ou como LinkedIn, reescreva.
- **Teste do corte:** apague cada frase, uma de cada vez. Se a história não perde nada, a frase sai.

Registre a nota e as perguntas que deram "não" no bloco "Narração final" da linha.

### Exemplo ruim (aula, nota 2)

> Hoje eu vou te mostrar o que aconteceu com o Canva. A empresa demitiu 22% do time, cerca de 1.271 pessoas. É importante destacar que o motivo foi o custo da IA. Isso mostra que a inteligência artificial está transformando o mercado. Por isso, é fundamental que você, empresário, reveja o seu diferencial. Afinal, quem não se adaptar vai ficar para trás. Salva esse vídeo!

Por que é ruim: abre anunciando a aula, não tem mistério nem virada, e repete a explicação óbvia em vez de ir contra ela. Tem abstração ("transformando o mercado", "seu diferencial"), ameaça de guru e CTA na fala. Ninguém aprende nada que já não sabia.

### Exemplo bom (DOM-MN reescrito, ~260 palavras, ~74 s, nota 9; comprimento antigo: hoje enxugue para 150 a 200 palavras, como no DOM-MN v3 do Notion)

Fontes: TechCrunch, 04/11/2026 (22%, 1.271, primeira desaceleração em dez anos, previsão de 30% para 20%, custo de IA, disputa com chatbots); Fortune, 12/08/2026 (custo de cada tarefa caiu quase 90%).

> O Canva cortou 22% do time.
> Mil duzentas e setenta e uma pessoas.
> E todo mundo repetiu a mesma explicação: a conta da IA ficou cara demais.
> Eu acho essa explicação confortável demais.
> Porque na mesma matéria tem uma linha que muda a história. Já chego nela.
> Primeiro, o tamanho do tombo.
> Primeira vez em dez anos que o Canva cresce menos.
> A previsão caiu de 30% pra 20%.
> Culpado oficial: o custo de rodar IA.
> Só que em agosto a própria CEO contou um detalhe.
> O custo de cada tarefa de IA caiu quase 90%.
> E o corte veio mesmo assim.
> A conta pode até pesar. Mas não explica tudo.
> Eu usava o Canva toda semana. Post, apresentação, capa.
> Hoje eu não tenho mais assinatura.
> Peço a arte pra IA. Ajusto o texto. Mudo o formato. Pronto.
> Não foi raiva do Canva. Só deixou de fazer sentido pagar.
> Agora, a linha.
> Ela diz que o Canva disputa com chatbots.
> Chatbots que deixam qualquer pessoa montar pôster e apresentação.
> Pôster. Apresentação. Exatamente o que eu fazia lá.
> Pra mim, o Canva não ficou caro. Ficou dispensável.
> Eu chamo isso assim: o diferencial virou o mínimo.
> Agora troca "Canva" pelo nome da sua empresa.
> E troca "pôster" por aquilo que o seu cliente te paga pra fazer.
> Se um chatbot já entrega quase igual, o problema não começa no caixa.
> Começa no dia em que o cliente percebe.
> O Canva cortou 22% do time.
> O corte que me assusta é outro: o do motivo de pagar.

Por que funciona: o inimigo é a explicação confortável, e o mistério (a linha da matéria) abre aos 8 s e fecha aos 48 s. A virada usa a própria CEO, com a nuance numa frase seca. A Joana entra na história com uma cena real, o aha dá nome ao fenômeno e o espectador troca de lugar com o Canva. O fim volta ao "22% do time" com outro sentido. Nota 9: perde o ponto 4 porque ainda há um "E" de soma ("E todo mundo repetiu…").

## Formato de saída

```
# Copy [código] — [título] | Publicação: [dd/mm/aaaa] | [tipo]
**Tese / tema:** | **Pilar:** | **CTA:**

## Carrossel (só carrossel)
### Slide 1 · tipo: capa
NA ARTE
- Título: "..." (destaque: ...)
- Texto: "..."
NOTA INTERNA (não vai para a arte)
- Função: capa (gancho escolhido)
- Imagem: [objeto-metáfora e cena, sem pessoas e sem texto]
### Slide 2 · tipo: imagem
NA ARTE
- Título: | Texto: | Fonte (só no slide do dado):
NOTA INTERNA
- Função: contexto/tensão | Imagem:
...
### Slide N · tipo: fecho
NA ARTE
- Título (resumo): | Texto (CTA):

### Teste A/B
- Hipótese: | Variável: | A: | B: | Métrica: — ou "sem teste nesta peça"

## Legenda
## Textos de tela (Reel e motion)
## Motion simples
## Narração final (só motion narrado)
- Mapa (nota interna): mistério | explicação óbvia (o inimigo) | virada + fonte | aha | o que está em jogo | callback
- Narração, uma frase por linha, com [tempo estimado]
- Teste viciante: nota __/10 (perguntas que deram "não" e o que foi reescrito)
- Fontes: número → veículo, data

## Stories (só linhas -S1 / -S2)
- Código | Tema | Fonte (registro, não vai entre parênteses na tela) | Data e horário
- Story 1 (exatamente como vai para a tela):
- Story 2:
- Como a interação nasce (nota interna):
- Ideias de story real:

## A verificar
```

## Autochecagem (todas sim)

- A peça é da semana-alvo e está em primeira pessoa?
- Tem uma tese só e zero palavra proibida?
- No carrossel, cada slide separa "na arte" e "nota interna", e nada interno está no bloco da arte?
- No carrossel, cada slide se lê em poucos segundos, com uma ideia, e tem a imagem descrita sem foto da Joana nem print?
- A capa é o gancho escolhido e o último slide traz o CTA?
- Os textos de tela têm até 6 palavras, e a narração foi escrita para ser falada?
- No motion narrado, a narração passou nas eliminatórias e tirou 8 ou mais no teste viciante?
- Nos Stories, o tom é informal, sem pedido explícito e sem parêntese de fonte, e a fonte está registrada na linha?
- Zero dado inventado?

## O que gravar no Notion

Na linha da peça, Etapa "9 Copy" e Status "Pronto para a próxima", "Bloqueado" ou "Retrabalho", com a copy no corpo da linha. Os Stories vão só nas linhas `-S1` e `-S2`. Feche com `STATUS: PRONTO | BLOQUEADO | RETRABALHO — <código> — <motivo em 1 frase>`.

## Guardrails

- Número só com fonte; o que faltar fica "sem dado". Nunca invente fato, caso, depoimento ou URL.
- Só a marca DNA.IA. Sem preço, sem Florianópolis.
- Nunca EVENTO, EU QUERO ou COMERCIAL. ROTINA só no Mapa das 5 Rotinas. Nenhuma palavra-chave nova.
- Nada é publicado, agendado ou enviado sem o OK da Joana.
- Não reescreva gancho nem roteiro, e não gere arte nesta etapa.
