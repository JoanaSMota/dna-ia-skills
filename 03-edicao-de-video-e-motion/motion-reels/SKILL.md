---
name: motion-reels
description: >-
  Use para especificar e produzir um Reel de motion (sem a Joana na tela) de uma
  peça da esteira, um passo por vez: primeiro a especificação de cenas e a
  checagem dela, depois o vídeo final animado em código vetorial no box, no
  visual copiado das referências (boneco palito simples, pequeno no centro,
  fundo preto, legenda embaixo, sem identidade da DNA) e com movimento fluido
  (cenas contínuas, easing, sem corte seco, conferido pelo checador de ritmo).
  Vale para motion narrado (40–55 s, ~3,8 palavras/s, legenda em blocos curtos) e motion simples só com
  música. Grava o resultado na linha da peça em Peças. Serve para qualquer bot
  do time que faça motion.
---
# Motion de Reels

Decisão da Joana (09/11/2026): motion fica no Grok Bot como skill, e não num agente do Dust. Decisão da Joana (10/11/2026): sem skills duplicadas, então esta skill **especifica e executa** o motion, um passo de cada vez: primeiro a especificação de cenas e a checagem dela (Fase 1); só depois o render (Fase 2). A especificação que estava no agente DNA-Motion do Dust foi incorporada aqui; aquele agente não é usado na esteira.

## Semana-alvo (regra fixa, decisão da Joana em 10/11/2026)

A esteira sempre planeja os **próximos 7 dias**, nunca a semana que já começou.

- **Ritmo:** no **domingo** a rotina dispara o fluxo (Painel, Pesquisa, Curadoria, Estratégia, Hook, Roteiro, Copy, Arte, Motion). Na **segunda** a Joana grava. Na **terça** é a edição. A publicação começa na **quarta**.
- **Semana-alvo:** de domingo + 3 dias (quarta) até domingo + 9 dias (a terça seguinte). São sempre 7 dias completos: 42 peças e 14 sequências de Stories. Nenhum dia da semana-alvo já passou quando a esteira roda.
- **Rótulo:** `AAAA-SNN · DD a DD/MM`. SNN é o número ISO da semana da **quarta** em que a publicação começa. Escreva sempre o rótulo junto com as datas.
  - Exemplo: disparo no domingo 15/11/2026 → semana-alvo de quarta 18/11 a terça 24/11 → rótulo `2026-S47 · 18 a 24/11`.
  - Rodada excepcional de terça 10/11/2026: janela de quarta 11/11 a terça 17/11, rótulo `2026-S46 · 11 a 17/11`.
- **O número não é a semana ISO de hoje.** A semana ISO 46 vai de 09 a 15/11, mas a semana-alvo `2026-S46` vai de 11 a 17/11. O número é só rótulo; as datas mandam. Nunca use "a semana atual", a semana ISO de hoje nem a semana do disparo como semana-alvo.
- **Códigos:** `AAAA-SNN-DIA-<sufixo>`, com DIA = dia da semana da data de publicação. A ordem dos dias na semana-alvo é QUA, QUI, SEX, SAB, DOM, SEG, TER. Em `2026-S47`, `2026-S47-QUA-C1` sai em 18/11 e `2026-S47-TER-C1` sai em 24/11. O banco Peças não tem propriedade "Data" (só "Dia", seleção): a data prevista de publicação fica escrita no topo do corpo de cada linha ("Data de publicação: dd/mm/aaaa"). Decisão da Joana (10/11/2026): "deixa assim", sem criar campo novo nem alterar títulos.
- **Só o Painel olha para trás:** métricas dos 7 dias anteriores ao disparo (no exemplo, 09 a 15/11). A Pesquisa usa as publicações dos 7 dias anteriores ao dia em que roda. Todas as outras etapas trabalham para a semana-alvo.
- **Conferência antes de gravar:** a primeira data é uma quarta depois de hoje, a última é a terça 6 dias depois, e nenhuma data já passou. Se a linha em Painéis da semana, as linhas de Peças ou um brief trouxerem outras datas, não herde: pare e avise a Joana.
- **Avanço:** cada passo só começa com o OK da Joana, nas palavras dela, ao passo anterior. OK do CMO ou de outro agente não vale.

Na esteira do @joanastanieski quem roda é o bot **Social Media e Comunidade** (etapa 11 Motion da [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac), no domingo, depois da Copy; a voz dos narrados é gravada na segunda e o acabamento fica na terça, para a publicação começar na quarta). Qualquer bot do time pode usar esta skill, desde que siga as regras da conta.

Volume da semana (Esteira v3): 1 motion narrado e 1 motion simples por dia = 7 narrados + 7 simples. Faça um por vez. Na primeira semana, faça a prévia de 1 de cada tipo e espere o OK da Joana antes de produzir o resto.

Dois tipos (campo **Tipo** da linha):

| Tipo na linha | Skill de formato | Duração | Cenas | CTA |
|---|---|---|---|---|
| Motion narrado (-MN) | `formato-motion-narrado` | 40–55 s (150–200 palavras a ~3,8 palavras/s) | 6 a 10 cenas contínuas; a cena troca quando a ideia muda | só na legenda do post (SALVAR ou COMPARTILHAR); a narração e a tela não têm CTA |
| Motion simples (-MS) | `formato-motion-musica` | 6–12 s, sem narração | 1 a 3 cenas contínuas, uma ideia numa imagem (ver a skill) | COMPARTILHAR (mensagem/opinião) ou SALVAR se ensina, na legenda do post |

Pelo mix da semana ([Pilares, territórios e mix](https://app.notion.com/p/41337997730781279ae0c45140503009)): narrados são 5 Ensina e 2 Lidera; simples são 4 Opina, 2 Constrói em público e 1 Conecta. Use o CTA que está na linha, na legenda do post.

Referências oficiais do @joanastanieski (abra antes da primeira peça da semana; cópias e frames em `/workspace/motion-ref/`):
- Motion curto só com música: https://www.instagram.com/reel/DfcBmyGvz5r/, https://www.instagram.com/reel/DfZ4RyixvuV/, https://www.instagram.com/reel/DfUeShIRTPC/
- Motion longo narrado: https://www.instagram.com/reel/DerUfAKCv7_/ (a referência de fluidez), https://www.instagram.com/reel/DdochV7RJ4e/
- Estudo quadro a quadro do @seu.auditor, com os números que o checador usa: `/workspace/pilotos-v2/motion/estudo-seu-auditor.md`.

## Decisões da Joana sobre o motion

- **10/11/2026:** copie as referências "na cara dura", inclusive o visual. Animação ilustrada com bonecos palito em fundo preto, **sem identidade da DNA** (sem paleta da marca, sem logo). O foco é a animação, gostosa de ver e que dá curiosidade. O texto é pequeno e discreto. O conteúdo (tese, roteiro, copy) continua sendo nosso, nunca o das referências. O Design System DNA **não** se aplica ao motion.
- **10/11/2026, depois dos pilotos v2:** "Se preocupe menos com detalhes de luz, expressão facial… os desenhos podem ser mais simples, boneco palito, e deixe menor também, concentrado no dentro da tela e mantendo a legenda embaixo." Boneco palito em linha, sem rosto e sem luz, com ~250 px de altura no terço do meio da tela, e legenda pequena embaixo.
- **10/11/2026, depois dos pilotos v3:** desenho aprovado. O narrado estava lento ("eu terminava de ler e ainda sobrava tempo") e a copy era educativa e chata; precisa ser viciante, com curiosidade e momento aha. A regra virou narração a 3,4 palavras/s, sem tempo morto, 60 a 90 s, e roteiro com gancho, loop, viradas e aha.
- **11/11/2026, objetividade:** informação em excesso e repetida atrapalha. Narração enxuta, 40 a 55 s (150 a 200 palavras), mantendo a estrutura viciante (regra de corte na `dna-copy-2`, subseção "Objetividade").
- **11/11/2026, depois do piloto v4:** o desenho continua aprovado. O problema era outro: o movimento estava rápido "de um jeito descoordenado, desconexo", com as cenas picotadas. O @seu.auditor está sempre em movimento, mas de forma fluida. A regra virou **cenas contínuas que se montam aos poucos**, easing em tudo, sem corte seco, um protagonista por vez e ritmo que muda com a ideia, não a cada frase. Tudo isso conferido pelo checador.
- **11/11/2026, depois do piloto v5:** fluidez aprovada ("Ficou muito melhor"). Ajuste: "eu leio a legenda mais rápido do que o vídeo passa". A legenda troca em blocos de 3 a 5 palavras no ritmo da fala (`legenda_blocos`), e a estimativa de voz sobe para 3,8 palavras/s. O teste é o `2026-S46-DOM-MN-v5b-sem-voz.mp4`.
- **11/11/2026, SAB-MN v7 → v8:** com a voz real, a legenda passa a ser o que ela falou, trocando na palavra exata (passo 10). No v7 faltaram os sons: "faltaram os sons do vídeo né? Que vão junto com a fala, para deixar a experiência mais prazerosa". SFX e trilha viraram passo obrigatório (seção Som). O v8 com som foi aprovado: "Parabéns, ele ficou muito bom". Referência de acabamento: `2026-S46-SAB-MN-v8-som.mp4`.
- **11/11/2026, QUA-MS v3 publicado:** "a música tá muito chata, mas resolva isso para os próximos" e "Cria uma capa que desperte curiosidade". A batida seca saiu do padrão. A trilha musical seguinte também foi reprovada, por excesso de agudos; a regra do som que vale está na seção Som. A capa não entrega a resposta (passo 14).

## Ordem do motion narrado (decisão da Joana, 11/11/2026)

No narrado, a ordem é esta, e não o contrário:

1. o roteiro (e a narração final da Copy) está aprovado;
2. a Joana pega o roteiro, grava a narração com o texto na mão e sobe o áudio na Pasta do Drive da peça;
3. só com o áudio na pasta a peça vai para criação e edição, no ritmo da voz real.

Nenhuma animação de MN começa antes do áudio. Depois da Copy, a linha fica na Etapa "6 Aguardando gravação", com o roteiro fácil de ler na página e o campo "Pasta do Drive" preenchido. Não entregue vídeo-guia sem voz e não peça para ela gravar assistindo à animação. O fluxo da voz real (passo 10) e o som continuam valendo, só que o render já nasce sincronizado com a fala.

## Entradas (leia antes de começar)

Confirme que o [Painel da semana](https://app.notion.com/p/c0c02b71d2ec4014bca145987d917580) está "Aprovado" ou "Aprovado com ajustes" pela Joana. Sem isso, nada começa. Leia o [Norteador](https://app.notion.com/p/41337997730781e6aa53f741117a54f0) e a seção Motion de [Formatos e métricas](https://app.notion.com/p/413379977307819abc54ce8acf914a29).

Na linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0), pelo **Código**:

| Campo | Para quê |
|---|---|
| Data de publicação (topo do corpo) e Dia | Data prevista; tem de estar dentro da semana-alvo |
| Tipo | Motion narrado ou Motion simples |
| Gancho escolhido | O que aparece e é dito nos 2 primeiros segundos |
| Link do roteiro ou copy | Narrado: roteiro do `dna-roteirista` e narração final da `dna-copy-2`. Simples: mensagem central e textos de tela da `dna-copy-2` (não tem roteiro) |
| Pasta do Drive | Pasta da peça no Drive. No narrado, a Joana sobe o áudio aqui. Sem esse link preenchido, o pacote de gravação não está pronto |
| CTA | SALVAR ou COMPARTILHAR, só na legenda do post. ROTINA só no Mapa das 5 Rotinas |
| Tese / Pilar / Território | Para não desviar da ideia |
| Etapa / Status | Só comece se a Copy (etapa 9) estiver "Pronto para a próxima" |

Visual e regras de tela de cada tipo: skills `formato-motion-narrado` e `formato-motion-musica`.

Se o Painel não estiver aprovado, ou se faltar roteiro, narração (narrado), textos de tela (simples) ou gancho: grave "Bloqueado" com o motivo e não improvise.

## Fase 1 — Especificação e checagem (antes de animar)

1. **Marque início.** Na linha: Etapa "11 Motion", Status "Em andamento", Responsável "Social Media".
2. **Confira a copy.** No narrado, a narração recebida precisa ter gancho com loop aberto, tensão, viradas, dado como revelação, aha e soco final, sem CTA e sem tom de aula, em 40 a 55 s a ~3,8 palavras/s, e com a nota do teste viciante (8 ou mais) registrada pela Copy. Se ela vier como aula, sem nota ou passar de 55 s ou repetir ideia, devolva para a Copy (`dna-copy-2`) com o motivo em vez de animar. No simples, a ideia tem que estar clara no 1º segundo.
3. **Mapeie as ideias, não as frases.** Narrado: agrupe a narração em **6 a 10 cenas**, uma por ideia (gancho, tensão, virada, história, revelação, aha, você, soco). Simples: 2 a 4 cenas. A cena só troca quando a ideia muda.
4. **Para cada cena**, escreva:
   - o cenário que fica (chão, personagens, objeto principal);
   - o que entra a cada frase, sempre um protagonista por vez;
   - o que é rebaixado quando o novo entra (fica apagado e não sai);
   - a transição de entrada (fade com montagem em escada, deslize de câmera ou morph de um elemento comum);
   - a fonte de cada número.
   O desenho mostra o que a legenda diz naquele instante.
5. **Tempo.** Cada frase dura (palavras faladas ÷ 3,8) + 0,12 s, com mínimo de 1 s; número conta por extenso. A legenda de cada frase é quebrada em blocos de 3 a 5 palavras com `legenda_blocos`. Não há pausa entre frases nem entre blocos. A cena começa 0,25 s antes da sua primeira frase.
6. **Trilha por função.** O narrado não é animado nesta fase: depois da Copy, a linha vai para a Etapa "6 Aguardando gravação" (ordem acima). O simples usa a trilha musical da seção Som. Nunca use música por nome sem direito de uso confirmado.
7. **Cheque a especificação** com a autochecagem e grave no corpo da página da linha. Só passe para a Fase 2 com tudo checado.

## Fase 2 — Execução em código (rota padrão)

8. **Anime em código vetorial** com o motor `/workspace/playbook/scripts/motion_palito.py`. No narrado, este passo só começa quando o áudio da Joana já está na Pasta do Drive (passo 10). Sem o áudio, não renderize. É skia-python: rode com `/workspace/.venv-motion/bin/python`, porque o python3 do sistema não tem skia. O render manda os quadros para o ffmpeg em `bgra` e sai em MP4 1080x1920, 30 fps, H.264.
   - **Um arquivo por peça:**
     - uma função por cena `cN(c, t)`, em tempo absoluto;
     - a lista de frases (legenda exata + fala por extenso para contar palavras);
     - `SCENES = [Scene(t0, t1, fn, trans, z)]`;
     - `CAPS = m.legenda_blocos([(t0, t1, legenda, palavras_faladas), …])` e um `draw(c, t)` que chama `play`, `caption_track(c, t, CAPS)` e `source_track`.
     Estrutura de exemplo: `/workspace/pilotos-v2/motion/v5b/` (`falas.py` + script da peça).
   - **API v5 de fluidez (use sempre em peça nova):**

     | Grupo | Funções |
     |---|---|
     | Curvas | `EZ_IN` (entrada, cubic-bezier .16,1,.3,1), `EZ_OUT` (saída, .7,0,.84,0), `EZ_MOVE` (deslocamento, .65,0,.35,1), `EZ_POP` (chegada com passada) |
     | Entrada e saída | `ein(t,t0)` (0,42 s), `eout(t,t1)` (0,24 s), `vis(t,t0,t1)` |
     | Gesto | `mv(t,t0,d)`: antecipação de 90 ms + follow-through de 60 ms |
     | Keyframes | `kf(t, [(t,valor,ease),…])` |
     | Arcos | `arcpt(p,a,b,h)` |
     | Linhas que se desenham | `draw_on`, `rect_on` |
     | Contador | `count` |
     | Ambiente | `amb` (loop lento) |
     | Boneco | `fig_ik` (comprimentos fixos, pernas por IK com pés travados, respiração com `t_amb`); `pose_kf` (poses interpoladas, braços chegando 50 ms depois do tronco); `walker` (anda de A a B com pé travado, acelera e freia) |
     | Câmera e cenas | `cam` (push + deriva; o padrão do motor é ±3 px, mas a peça usa a regra de câmera do passo 12); `Scene` + `play` (sobreposição de 14 quadros entre cenas: `'fade'`, `'slide'` ou `'morph'`) |
     | Legenda e fonte | `legenda_blocos` (quebra cada frase em blocos de 2 a 6 palavras no ritmo da fala); `caption_track` (bloco velho some antes do novo, sem sobrepor); `source_track` |

     A API antiga (`fig`, `pose_seq`, `pop`, `drop`, `caption`…) continua lá para os pilotos v3/v4, mas não é usada em peça nova: o quique e as trocas de 0,14 s davam o efeito picotado.
   - **Palco:** chão em y ≈ 1180, conteúdo entre y ≈ 560 e 1250, legenda em y ≈ 1560 (Work Sans 44 px), fonte em mono 22 px em y ≈ 1665.
   - **Por que código e não GenerateVideo:** com boneco palito simples, o código dá traço igual do começo ao fim, controle exato de curva e tempo, e zero letra inventada. O GenerateVideo desenhava luz e rosto e deformava. Use o GenerateVideo só se a cena pedir algo que o código não desenha bem, e nunca desacelere o clipe.
9. **Regras de movimento** (mais detalhe e números nas skills de formato):
   - Nada linear, a não ser loop ambiente e câmera.
   - Entrada de 0,3 a 0,5 s, saída mais curta, e escada de ~0,3 s entre elementos de um grupo.
   - Trajeto em arco; nada atravessa mais de 1/3 da tela num movimento só.
   - Um protagonista por vez; no máximo 1/3 dos elementos em movimento ativo. O resto respira (ambiente abaixo do limiar de ação).
   - Um início de movimento a cada 0,4 a 1,2 s dentro da cena; nenhum trecho parado acima de 3 s.
   - Objeto grande se move devagar. Se o checador acusar salto, alongue a duração ou faça o objeto crescer no lugar em vez de viajar.
10. **Narrado — só depois do áudio.** Não entregue vídeo-guia sem voz. Quando o áudio chegar na Pasta do Drive (exemplo completo: `/workspace/pilotos-v2/motion/v7/`):
    1. **Baixe** o áudio da pasta da peça no Drive (`DownloadFile`) para `vN/` e guarde o original; nunca apague o áudio dela do Drive.
    2. **Texto:** faster-whisper `large-v3` com `compute_type='float32'`, `language='pt'`, `condition_on_previous_text=False` e sem `initial_prompt`, sobre o áudio convertido para 16 kHz mono com passa-alta + loudnorm (`v7/transc.py`). `int8` e `large-v3-turbo` pulam trechos e inventam palavras; não use. Confira trechos duvidosos de novo com o áudio cortado (`v7/clip.py`).
    3. **Tempos:** alinhamento forçado MMS_FA (torchaudio, venv `/workspace/.venv-align`, `v7/align.py` → `words_real.json`). O tempo por palavra do whisper adianta 0,3 a 0,6 s nas pausas; não use direto.
    4. **Voz para o mix:** corte o silêncio inicial para a fala começar em ~0,25 s (`OFF` no `falas.py`), passa-alta de 70 Hz e loudnorm -14 LUFS / -1,5 dBTP (`voz-mix.m4a`). Redução de ruído (`editar_reel.py`) só se o áudio tiver ruído.
    5. **Legenda = o que ela FALOU**, não o roteiro: `LINHAS` do `falas.py` com o texto falado, e `legendas()` monta blocos de 2 a 6 palavras (`leg_blocos`) que começam e terminam nas palavras reais. Bloco acima de 1,7 s é partido ao meio; `|` na linha força quebra (o aha fica sozinho, como "Era eu."). Número fica em algarismo ("42"), contando como a voz diz.
    6. **Cards e rótulos na palavra falada:** os tempos da animação usam `wt(linha, 'palavra')` (início real da palavra), não offset fixo da frase.
    7. **Divergências:** liste no relatório toda diferença entre fala e roteiro. Deslize que **inverte o sentido** (ex.: "o que precisa de você… vai pra um agente") vira aviso para regravar só aquela frase; a legenda não repete o trecho errado.
    8. Renderize com a voz, rode o checador (passo 12) e aplique o **Som** (seção abaixo) antes de entregar. Nunca entregue motion com voz sem SFX (e sem música de fundo, regra de 12/11/2026).
11. **Simples:** 120 BPM = um tempo a cada 0,5 s; escreva os tempos da peça em batidas (`b(n) = n*0,5`), com os gestos principais começando na batida. Fim com a última ação fechando ou parada limpa para o loop. A trilha e os SFX saem juntos pelo `sfx_motion.py --trilha 120` (seção Som). Exemplo: `/workspace/pilotos-v2/motion/quams_v3/quams_v3.py`.
12. **Rode o checador:** `python3 /workspace/playbook/scripts/checa_ritmo_motion.py video.mp4`. Ele mede o palco quadro a quadro e reprova por:
    - corte seco;
    - movimento brusco (mudança mediana por quadro acima de 0,30);
    - agitação (ação em mais de 60% dos quadros);
    - tremor;
    - movimento sem easing;
    - trecho parado acima de 4 s.
    Ele foi calibrado no @seu.auditor, que passa, e no v4 picotado, que reprova. Só entregue com **PASSA**. Se reprovar, ele diz o segundo exato: corrija a cena e renderize de novo.
    Com a voz a ~3,8 palavras/s, o % de ação sobe. Se passar de 60%, encurte os deslocamentos longos (objeto que cresce, caminhada) e pare os loops (boca, brilho) quando a ação acaba, em vez de desacelerar a cena.
    **Regra de câmera (vale para narrado e simples):** o zoom de câmera (`cam`) avança na mesma velocidade em todas as cenas, `z = (1.0, 1.0 + min(0.05, 0.0028 * duração_da_cena))`, sem acelerar em cena curta, e o balanço fica em ±2 px (subclasse `_cam` com `drift=2.0`, como no `sabmn_v7.py`). Senão a câmera sozinha conta como ação.
13. **Confira os frames você mesmo:**
    - folha de frames com um quadro por frase;
    - folha a 12 fps de pelo menos uma troca de cena e de uma caminhada;
    - lado a lado com um frame de `/workspace/motion-ref/`.
    Procure texto encostado em objeto, legenda sobreposta ou com mais de 6 palavras, elemento cortado e quadro vazio demais. O checador não vê composição.
14. **Capa (narrado e simples):** a capa **desperta curiosidade e não entrega a resposta**: mostra o problema ou o contraste ainda aberto (o caos, a dúvida, o antes) com uma pergunta ou frase que pede o vídeo, nunca o fecho, a moral ou a frase final do vídeo. Ex.: QUA-MS v3 = os vários agentes enrolados + "Mais agentes, menos feito?" (e não "Comece com um."). Função `capa(path, t, linhas)` no script da peça (ou `capa_v3b.py` ao lado): quadro da própria animação, sem legenda, com uma frase de 3 a 5 palavras em Work Sans ~104 px, em 1 ou 2 linhas, uma palavra em âmbar, dentro do miolo 4:5 (y 285 a 1635, 90 px de margem lateral). Salve também a versão de 200 px e confira a leitura. Não use `capa_reel.py`: ele é para Reels com a Joana (v2 Biblioteca da Luz). Exemplo: `quams_v3/capa_v3b.py saida.png 5.6`.
15. **Suba e grave.** Drive (pasta da semana) com `UploadFile`. Na linha: "Link do final (Drive)" e Status "Pronto para a próxima" (segue para "12 Revisão"; no narrado, só depois da voz), com a especificação atualizada no corpo da página.

Primeira semana: prévia de 1 de cada tipo para o OK da Joana antes de produzir o resto. HeyGen está pausado: não use.

## Som (SFX e trilha) — obrigatório em todo motion

Decisão da Joana (11/11/2026): o som acompanha a ação e "deixa a experiência mais prazerosa". Esta seção é a única fonte da regra; as skills de formato só apontam para cá.

**REGRA VIGENTE (Joana, 12/11/2026): motion NÃO tem música de fundo.** "Motion não precisa ter música, só precisa ter os barulhinhos... que sejam prazerosos." Vale para narrado e simples: o som é só a voz (no narrado) e os SFX dos movimentos, atrativos e prazerosos, mantendo o timbre de madeira (marimba de madeira do tique, plops macios e baques fofos). Rode sempre sem trilha: narrado com `--sem-trilha`; simples sem `--trilha` (se o script exigir trilha, adicione a opção de desligar em vez de usar música). As linhas sobre trilha/música abaixo ficam só como histórico e não valem mais. A música da prévia do AVULSO-MN-fluxo (11/11) foi reprovada: "A música tá muito ruim".

**Regra do som (2º feedback, 11/11/2026):** "continuou ruim, porque ela tem muitos tons agudos que incomodam... deixar a música baixinha, uma música que massageie o ouvido, e focar nos efeitos sonoros prazerosos. Lembre-se, o objetivo é viciar." Então:
- **Os SFX são o foco**, no estilo ASMR: macios, encorpados (graves e médios), cauda curta, sem estalo agudo, e cada repetição varia de leve (altura ±5%, cauda ±12%, nível ±1,5 dB) para não cansar.
- **A música fica baixinha e quente:** pad macio, Rhodes abafado, baixo redondo, pulso grave, notas longas e ataque lento. Sem prato, chimbal, lead brilhante ou chiado.
- **Nada agudo:** tudo abaixo de ~3,5 kHz. Confira na análise espectral: energia acima de 4 kHz perto de 0% no simples. No narrado, o que passar disso é só a voz.

- **Ferramenta:** `/workspace/playbook/scripts/sfx_motion.py` (v3), rodado com `/workspace/.venv-motion/bin/python`. Ele roda o `draw()` da cena num canvas mínimo (sem renderizar vídeo), anota o quadro exato de cada evento, sintetiza os sons em numpy (sem arquivo de terceiros, sem dúvida de direito), mixa e troca só o áudio do mp4 (o vídeo é copiado).
  - Narrado: `sfx_motion.py CENA.py voz-mix.m4a VIDEO_COM_VOZ.mp4 SAIDA.mp4 --folha SAIDA-eventos.md`
  - Simples: `sfx_motion.py CENA.py - VIDEO.mp4 SAIDA.mp4 --trilha 120 --seed N --folha SAIDA-eventos.md` (trilha calma de `trilha_musical.py`; use um seed novo por peça). Não use `--batida` nem os estilos antigos `leve`/`lofi`/`pop`, que ela reprovou.
- **Sons:** pop = plop de bolha 190–280 Hz; pop suave = plop 130–190 Hz; tique (✓) = dois toques de marimba de madeira (520 e 780 Hz); ding = sino quente 523 Hz; whoosh = sopro grave 250–900 Hz; impacto = baque grave fofo; passos e esteira graves. Todos com ataque de 3 a 6 ms (sem clique) e saturação suave para dar corpo.
- **Eventos automáticos:** troca de cena (`SCENES`) → whoosh com pico no meio da sobreposição; `text()` que aparece (rótulo, card, número que conta) → pop; `doc()` e `bubble()` → pop suave; `check()` → tique; `walker()` → passos. A legenda e a fonte não fazem som. Ele limpa excessos: um som de cada tipo por vez, intervalo mínimo por tipo e nada de rajada de pops na montagem de cena nova.
- **Eventos manuais**, na lista `SFX = [(t, tipo, dur, 'descrição')]` do script da cena: virada e aha → `impacto` ou `ding`; esteira ou máquina andando → `esteira` (com duração); qualquer ação desenhada com `rect`/`rect_on` que mereça som (documento pulando, computador se desenhando) → `pop` ou `pop2`. `SFX_IGNORA = {'texto', …}` cala rótulos que não devem soar.
- **Níveis dos SFX** (pico em janela de 50 ms, em relação ao RMS da voz; no simples, de uma voz virtual): impacto -12, ding -13, whoosh -14, tique -15, pop -16, esteira -17, passos e pop suave -18. `--sfx-db` desloca todos juntos.
- **Trilha:**
  - Narrado: pad ambiente sem melodia, a **-30 dB sob a voz** e -26 dB nas pausas, com ducking (ataque 40 ms, soltura 350 ms), entrada de 0,6 s e fade de 0,8 s (`--trilha-db`, `--sem-trilha`).
  - Simples: trilha calma a -36 dB da voz virtual, que fica 10 a 16 dB abaixo dos SFX e abaixa mais 6 dB sob cada um (ducking).
  - A trilha calma (`trilha_musical.py`, estilo `calmo`) leva acordes com 7ª (I–vi–IV–V e variações), pad, Rhodes com motivo de notas longas que muda por frase, baixo redondo e pulso grave nos tempos 1 e 3, tudo num passa-baixa de 3,2 kHz.
  - Exemplo para ouvir: `/workspace/pilotos-v2/motion/2026-S46-QUA-MS-v3-teste-som-asmr.mp4`.
- **Master:** -14 LUFS integrado, pico verdadeiro ≤ -1,0 dBTP já no AAC, 0 amostras clipadas (limitador sobreamostrado a -2 dBFS só nos picos). O script imprime os níveis e escreve a **folha de eventos** (tempo, quadro, som, ação, linha da cena), que sobe junto com o vídeo.
- **Confira:** abra a folha de eventos; se um momento importante ficou sem som ou um som caiu no lugar errado, ajuste `SFX`/`SFX_IGNORA` e rode de novo (leva segundos).

## Autochecagem (sim/não)

Especificação (Fase 1):
- A data de publicação da linha está dentro da semana-alvo e não já passou?
- A narração tem loop aberto, viradas, dado como revelação, aha e soco final, sem CTA, em 40 a 55 s?
- Narrado em 6 a 10 cenas (simples em 2 a 4), com a cena trocando só quando a ideia muda?
- Cada frase tem o que entra, o que é rebaixado e a fonte do número?
- Os 2 primeiros segundos entregam o gancho?
- Zero música de fundo (só voz e SFX de movimento com timbre de madeira)?
- Zero dado inventado; todo número tem fonte na tela?

Vídeo final (Fase 2):
- Visual das referências: boneco palito simples, pequeno, no centro, fundo preto, âmbar só de destaque, sem identidade da DNA, legenda embaixo?
- Checador com **PASSA** (0 cortes secos, sem brusco, agitado, tremido, linear ou parado)?
- Um protagonista por vez, trajetos em arco, nenhuma troca seca entre cenas?
- Cada frase mostra o que a legenda diz; legenda em blocos de 3 a 5 palavras, trocando no ritmo da fala e nunca sobreposta?
- Abri o vídeo, a folha de frames, a folha de 12 fps e o lado a lado com a referência?
- Narrado: a animação só começou depois do áudio na Pasta do Drive?
- Narrado com voz: legenda com o texto que a Joana falou, tempos por alinhamento forçado, divergências listadas e deslize que inverte sentido avisado?
- Som aplicado com `sfx_motion.py` (folha de eventos aberta, -14 LUFS, pico ≤ -1 dBTP, 0 clipadas)?
- Capa no estilo do motion, conferida em 200 px, e sem entregar a resposta do vídeo?

## Modelo de saída (vai na linha da peça)

```
# Motion [Código] — [título] | Tipo: [narrado | simples]
Data de publicação: dd/mm/aaaa | Duração: | Cenas e trocas: | CTA (legenda do post): | Pilar: | Território:
## Cenas
| # | Ideia | Entra | Dur. | Cenário que fica | O que entra a cada frase | Transição | Fonte |
## Narração (narrado) ou textos de tela (simples)
## Checador
- PASSA/REPROVA — cortes secos, mudança mediana, % de ação, tremor, sem easing, maior trecho parado
## Trilha
- Função: [trilha calma 120 BPM, seed | voz + trilha ambiente] — SFX: [folha de eventos] — LUFS / pico — direito de uso: [confirmado | a verificar]
## Capa
- Cena [n] — texto (pergunta ou problema aberto, sem a resposta):
## Checagem (Fase 1 e Fase 2)
## Pendências
- [item] — a verificar com: [quem]
STATUS: PRONTO | BLOQUEADO | RETRABALHO — [código] — [motivo]
```

## Guardrails

- Nenhuma etapa começa antes de o Painel ser aprovado pela Joana. Fase 2 só com a Fase 1 completa e checada.
- Não diga que renderizou sem ter aberto o arquivo, a folha de frames e o resultado do checador.
- Não altere a narração nem os textos de tela entregues: divergência vira observação, ou devolução para a Copy se a narração vier como aula ou passar de 55 s.
- Texto pequeno e embaixo: motion é animação, não slide.
- Nunca resolva ritmo com corte seco nem com ação desacelerada: troque a cena com sobreposição e acrescente o próximo elemento.
- Número só com fonte; o que faltar é "sem dado". Fonte nova, fora da linha, você mesmo confere na matéria original e decide (a Joana não quer ser consultada sobre checagens miúdas); se não se confirmar, o número sai.
- Nada de foto ou imagem da Joana; voz da Joana em primeira pessoa no narrado.
- Sem preço, sem Floripa, evento só com orientação da Joana, nada de EVENTO, EU QUERO ou COMERCIAL. ROTINA só no Mapa das 5 Rotinas.
- Não agende nem publique: só depois do OK final da Joana na peça (etapa 13 Aprovação Joana; o agendamento é a etapa 14). Nada é enviado sem o OK da Joana.
- Refazer atualiza a mesma linha e incrementa "Tentativas".
- Feche sempre com a linha de STATUS.
