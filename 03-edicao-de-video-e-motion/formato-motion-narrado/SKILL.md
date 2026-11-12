---
name: formato-motion-narrado
description: >-
  Use esta skill ao planejar, roteirizar ou produzir um Reel de motion narrado
  (40–55 s, voz da Joana a ~3,8 palavras/s) que conta um caso, um sistema ou uma
  estratégia como uma história viciante (gancho com loop aberto, tensão,
  viradas, dado como revelação, aha e soco final, sem CTA), animado em código
  com boneco palito simples, pequeno no centro, fundo preto e legenda embaixo,
  em 6 a 10 cenas contínuas com movimento fluido e sem corte seco, e legenda em blocos curtos de 3 a 5 palavras no ritmo da fala.
---
# Formato: motion narrado

Referências (abra antes da primeira peça da semana; cópias em `/workspace/motion-ref/`):
- @seu.auditor, Tesla Roadster e ancoragem de preço, 128 s: https://www.instagram.com/reel/DerUfAKCv7_/. É a **referência de fluidez**: desenho em linha sobre preto e legenda pequena embaixo. Estudo quadro a quadro em `/workspace/pilotos-v2/motion/estudo-seu-auditor.md`.
- @marcondes.ai, system design da Netflix, 158 s: https://www.instagram.com/reel/DdochV7RJ4e/ (mascote e diagramas).

O traço dos personagens é o mesmo do motion curto (@visualhustles).

## Decisões da Joana
- **10/11/2026:** copiar as referências "na cara dura": animação ilustrada, fundo preto, **sem identidade da DNA**. O foco é a animação. Legenda pequena e discreta.
- **10/11/2026, depois dos pilotos v2:** desenho mais simples (boneco palito, sem luz nem expressão facial), menor e no centro, legenda embaixo.
- **10/11/2026, depois dos pilotos v3:** desenho aprovado, mas o narrado estava lento e a copy era "um conteúdo educativo chato. Precisa ser viciante", com curiosidade e momento aha.
- **11/11/2026, depois do piloto v4:** o movimento estava rápido "de um jeito descoordenado, desconexo", com cenas picotadas. O @seu.auditor está sempre em movimento, mas fluido. A partir daqui vale **cena contínua por ideia**, easing, sem corte seco e um protagonista por vez.
- **11/11/2026, depois do piloto v5:** "Ficou muito melhor", mas "eu leio a legenda mais rápido do que o vídeo passa". A legenda passa a trocar em **blocos de 3 a 5 palavras** no ritmo da fala, e a estimativa de voz sobe para **3,8 palavras/s**. A copy passa a seguir a seção "Motion narrado: narrativa viciante" da `dna-copy-2`.

## Quando usar
Um caso ou mecanismo que fica viciante quando desenhado passo a passo: por que uma empresa errou, como um agente funciona, por que um método dá certo.

## Copy viciante (o que a narração precisa ter antes de animar)
A narração vem da Copy (`dna-copy-2`). No motion, confira estes pontos. Se faltar algum, devolva para a Copy em vez de animar.
1. **Gancho com loop aberto (0–10 s):** um fato que choca e uma promessa sem resposta, como "tem uma linha que conta outra história" ou "era muito ou pouco?". O loop só fecha perto do fim.
2. **Tensão (10–20 s):** o tamanho do problema, com o número entrando como golpe.
3. **Virada com dado (20–35 s):** "faz sentido… até você ver outro número". O dado contradiz a explicação óbvia.
4. **História (35–50 s):** alguém fazendo algo, de preferência a própria Joana em primeira pessoa. Ação concreta, não conceito.
5. **Revelação e aha (50–65 s):** o loop do gancho fecha, e o aha reinterpreta o começo numa frase ("o diferencial virou o mínimo").
6. **Você (65–80 s):** a pergunta vira para o negócio de quem assiste, em até 4 frases.
7. **Soco final:** uma frase curta com ponta. **Sem CTA** na narração e na tela; o CTA da linha vai na legenda do post.

Uma virada a cada 10 a 15 s. Frases curtas, de até ~12 palavras, no tom da Joana falando. Todo número tem fonte e data; opinião da Joana é dita como opinião ("eu acho que…"). Total de **40 a 55 s = 150 a 200 palavras a ~3,8 palavras/s**. Se não couber, corte texto; nunca estique. As técnicas, os proibidos e o teste de nota 8 ou mais estão na seção "Motion narrado: narrativa viciante" da `dna-copy-2`.

## Cenas e ritmo (fluidez)
Números medidos no @seu.auditor: 0 cortes secos, ~9 s por cena, entrada de elemento em 0,33 a 0,5 s com ease-out forte, escada de 0,27 a 0,4 s, fade de saída de 0,23 a 0,33 s, câmera parada e ação em ~26% dos quadros.

- **6 a 10 cenas contínuas** em 40 a 55 s, uma por ideia (os 7 passos acima viram 6 a 10 cenas). O ritmo muda quando a ideia muda, não a cada frase.
- **Dentro da cena, os elementos se acumulam.** Cada frase traz um elemento novo, que é o protagonista, e o anterior é rebaixado (fica apagado, ~45%) em vez de sair. A cena só se esvazia na troca de ideia.
- **Troca de cena sem corte seco:**
  - **fade:** a cena velha sai em 14 quadros e a nova se monta em escada;
  - **deslize de câmera:** 140 px com sobreposição;
  - **morph:** um elemento comum fica no lugar e o resto troca em volta.
  Sobreposição de 12 a 16 quadros. Use o deslize para "virada", o fade para "próximo capítulo" e o morph quando um objeto volta (callback do gancho).
- **Tempo de cada frase:** antes da voz, a estimativa do passo 5 da `motion-reels`; depois da voz, os tempos reais do passo 10. O % de ação e o que fazer se passar de 60% estão no passo 12.
- **Curvas:**
  - entrada `EZ_IN` (0,3 a 0,5 s);
  - saída `EZ_OUT` (0,2 a 0,3 s);
  - deslocamento `EZ_MOVE` (0,4 a 0,9 s, maior para objeto grande);
  - gesto com antecipação de 60 a 120 ms e follow-through de 40 a 80 ms (`mv`);
  - trajetos em arco (`arcpt`).
  Nada linear, a não ser o loop ambiente e a câmera.
- **Um protagonista por vez:** no máximo 1/3 dos elementos em movimento ativo. Grupo (fileira de bonecos, moedas) entra em escada e depois fica parado; personagens principais só respiram (`t_amb`).
- **Nunca parado:** um início de movimento a cada 0,4 a 1,2 s e nenhum trecho acima de 3 s sem ação. Câmera: regra de câmera do passo 12 da `motion-reels`.
- **Boneco:** pernas por IK com pés travados (`fig_ik`, `walker`). Quem entra em cena chega andando, acelera e freia, e as poses mudam por interpolação (`pose_kf`), sem pulo de pose.
- **Objeto grande** (documento, cartão) cresce no lugar ou anda pouco. Viagem longa de objeto grande vira salto no checador.

## Visual
- Fundo preto (#0A0A0A), traço creme (#F0EADC) de ~7 px, âmbar (#E8B04C) só no que importa. Boneco palito com cabeça redonda e sem rosto; robô com cabeça quadrada, antena e dois pontos âmbar (a IA).
- Pequeno e no centro: personagens com ~230 a 260 px de altura, conteúdo entre y ≈ 560 e 1250, chão cinza em y ≈ 1180 e bastante preto em volta.
- Números grandes em âmbar dentro do palco: contam com `count` e entram com `EZ_POP` só no número da revelação.
- Molduras, gráficos e setas **se desenham** (`draw_on`, `rect_on`); barras enchem a partir da base; rótulos em mono 22 a 30 px.
- Sem identidade da DNA, sem logo de marca citada (só o nome falado e na legenda).

## Texto na tela
- **Legenda embaixo, em blocos curtos de 2 a 6 palavras** (alvo de 3 a 5), quebrando na pontuação e nunca depois de palavra fraca ("de", "o", "que", "não"). Antes da voz, o texto e o tempo vêm da narração (`legenda_blocos`); depois da voz, do que a Joana falou, palavra por palavra (passo 10 da `motion-reels`). Work Sans 44 px, creme, uma linha, centralizada em y ≈ 1560, sem pílula. O bloco velho some antes de o novo aparecer, nunca os dois juntos.
- **Sem rótulo no topo.**
- **Fonte:** mono 22 px em y ≈ 1665, nas frases com número (`source_track`).

## Som
- Ordem e voz: a Joana grava a partir do roteiro, sobe o áudio na Pasta do Drive, e só então a animação começa, no ritmo da voz real (passo 10 da `motion-reels`). Não há vídeo-guia sem voz para ela assistir.
- Quando a voz chegar: fluxo da voz real no passo 10 da `motion-reels` (texto, alinhamento, legenda do que ela falou, divergências). Depois, só SFX de movimento (sem música de fundo, regra de 12/11/2026) pela seção Som da `motion-reels` (`sfx_motion.py --sem-trilha`). No narrado, marque na lista `SFX` da cena a virada, o aha e o callback.

## Checklist antes de entregar
- [ ] A narração veio da Copy com nota 8 ou mais no teste viciante (`dna-copy-2`), com gancho em 2 s e loop aberto fechado perto do fim?
- [ ] Virada a cada 10 a 15 s, dado como revelação, aha numa frase e soco final sem CTA?
- [ ] 40 a 55 s a ~3,8 palavras/s, sem tempo morto?
- [ ] 6 a 10 cenas contínuas, com a cena trocando só quando a ideia muda?
- [ ] Cada frase traz um protagonista, e o anterior é rebaixado, não sai?
- [ ] `checa_ritmo_motion.py` deu **PASSA**?
- [ ] Na folha de 12 fps de uma troca de cena e de uma caminhada: sem salto, sem pose pulando, pés travados?
- [ ] Boneco simples, pequeno, no centro; legenda embaixo em blocos de 3 a 5 palavras (nenhum acima de 6 nem acima de ~3 s na tela) e nunca sobreposta?
- [ ] Todo número na tela tem fonte com data; fonte nova conferida por você mesmo na matéria original (sem consultar a Joana)?
- [ ] Com a voz: passo 10 e seção Som da `motion-reels` feitos (legenda do que ela falou, divergências, `sfx_motion.py` com folha de eventos)?
- [ ] Capa conforme o passo 14 da `motion-reels`?
