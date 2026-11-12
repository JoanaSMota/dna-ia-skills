---
name: producao-reels
description: >-
  Use quando for planejar, roteirizar, editar, gerar capa, legendar ou agendar
  Reels de Instagram de um cliente (ganchos, roteiros no Drive, edição com
  redução de ruído e legenda queimada, capa, legenda com CTA de palavra-chave,
  agendamento no Zernio). Leia antes de escrever o primeiro gancho, editar um
  bruto ou abrir o agendador. No @joanastanieski, só edição, capa e Zernio: o
  resto vem da Esteira.
---
# Produção de Reels

> **No @joanastanieski vale a [Esteira](https://app.notion.com/p/41337997730781c6b9a1cdbaa68265ac) (versão 3).** A semana-alvo é sempre a dos próximos 7 dias, de quarta a terça: domingo dispara, segunda grava, terça edita, quarta publica. Lá, a edição segue a skill `editor-reels` (motions: `motion-reels`), e esta skill serve de apoio para edição, capa, legenda queimada e as notas do Zernio. Regras do perfil:
> - Pesquisa, gancho, roteiro, formato e CTA vêm da linha da peça em [Peças](https://app.notion.com/p/ee0dafe28f3e41f0afee2a39b81e50a0) (skills `dna-pesquisa-2`, `dna-hook-2`, `dna-roteirista`, `dna-copy-2` e `estrategia-formatos`; os agentes do Dust não são mais usados). Não monte Doc de ganchos nem mix próprio.
> - O campo **Data** da linha é a data prevista de publicação: é por ele que se agenda.
> - A Joana sobe os brutos na pasta Brutos **sem nome nem código**; o Social Media classifica, dá o código da peça e grava o link na linha.
> - Capa só com `/workspace/playbook/scripts/capa_reel.py` da skill `design-system-dna`. Legenda queimada em Work Sans (v2 Biblioteca da Luz), sem contorno colorido e sem caixa. Nada de Montserrat nem Instrument Sans.
> - CTA: SALVAR (Reel que ensina) ou COMPARTILHAR (opinião ou humor). Nenhuma palavra-chave além de ROTINA, e ROTINA só no post do Mapa das 5 Rotinas.
> - Aprovação é por peça (OK final da Joana, nas palavras dela), não por pacote semanal. Repetir ou testar formato é decisão da skill `estrategia-formatos` a partir do Painel da semana.
> - Nas outras contas (clientes), a skill vale inteira como está abaixo.

## Semana-alvo (regra fixa, decisão da Joana em 10/11/2026)

A esteira sempre planeja os **próximos 7 dias**, nunca a semana que já começou.

- **Ritmo:** no **domingo** a rotina dispara o fluxo (Painel, Pesquisa, Curadoria, Estratégia, Hook, Roteiro, Copy, Arte, Motion). Na **segunda** a Joana grava. Na **terça** é a edição. A publicação começa na **quarta**.
- **Semana-alvo:** de domingo + 3 dias (quarta) até domingo + 9 dias (a terça seguinte). São sempre 7 dias completos: 42 peças e 14 sequências de Stories. Nenhum dia da semana-alvo já passou quando a esteira roda.
- **Rótulo:** `AAAA-SNN · DD a DD/MM`. SNN é o número ISO da semana da **quarta** em que a publicação começa. Escreva sempre o rótulo junto com as datas.
  - Exemplo: disparo no domingo 15/11/2026 → semana-alvo de quarta 18/11 a terça 24/11 → rótulo `2026-S47 · 18 a 24/11`.
  - Rodada excepcional de terça 10/11/2026: janela de quarta 11/11 a terça 17/11, rótulo `2026-S46 · 11 a 17/11`.
- **O número não é a semana ISO de hoje.** A semana ISO 46 vai de 09 a 15/11, mas a semana-alvo `2026-S46` vai de 11 a 17/11. O número é só rótulo; as datas mandam. Nunca use "a semana atual", a semana ISO de hoje nem a semana do disparo como semana-alvo.
- **Códigos:** `AAAA-SNN-DIA-<sufixo>`, com DIA = dia da semana da data de publicação. A ordem dos dias na semana-alvo é QUA, QUI, SEX, SAB, DOM, SEG, TER. Em `2026-S47`, `2026-S47-QUA-C1` sai em 18/11 e `2026-S47-TER-C1` sai em 24/11. O campo **Data** do banco Peças é a data prevista de publicação (decisão da Joana em 10/11/2026): preencha esse campo em toda linha, sem alterar o título nem criar campo novo, e repita a data completa (dd/mm/aaaa) na primeira linha do corpo.
- **Só o Painel olha para trás:** métricas dos 7 dias anteriores ao disparo (no exemplo, 09 a 15/11). A Pesquisa usa as publicações dos 7 dias anteriores ao dia em que roda. Todas as outras etapas trabalham para a semana-alvo.
- **Conferência antes de gravar:** a primeira data é uma quarta depois de hoje, a última é a terça 6 dias depois, e nenhuma data já passou. Se a linha em Painéis da semana, as linhas de Peças ou um brief trouxerem outras datas, não herde: pare e avise a Joana.
- **Avanço:** cada passo só começa com o OK da Joana, nas palavras dela, ao passo anterior. OK do CMO ou de outro agente não vale.

Objetivo: fazer Reels que atraiam **seguidores qualificados** (o ICP do cliente), aumentem a percepção de valor e levem a conversas de venda. Volume de views não é o objetivo.

## 0. Pré-requisitos (confira antes de começar)

- **Intake preenchido.** Na página de intake do cliente no Notion devem estar: marca, ICP e anti-ICP, mecanismo, pilares, tom, provas aprovadas, ofertas, palavras-chave de CTA, cadência, pastas e regras do cliente. Se faltar ICP, palavra-chave ou provas aprovadas, pergunte. Não invente.
- **Conectores ativos:**
  - Google Drive, para roteiros, brutos e legendas.
  - Zernio, para agendamento, automações e métricas.
  - Notion, para o pacote semanal e o intake.
  - Opcionais: Dust ou outra IA de copy, Canva, HeyGen e Apify.
- **Box com ferramentas de edição:**
  - `ffmpeg` com libass.
  - `pip install faster-whisper numpy pillow`.
  - Os scripts do Apêndice salvos em `~/conteudo/scripts/`. Se não existirem, crie-os a partir do Apêndice.
- **Pastas no Drive:** `<Marca>/Conteúdo/` com as subpastas `Roteiros`, `Brutos`, `Editados`, `Capas`, `Legendas` e `Já postados`.

## 1. Pesquisa (semanal)

- Junte notícias e tendências do nicho da semana. Use a IA de pesquisa do cliente (ex.: Dust), busca web e X.
- Cada item precisa de fonte (veículo, link e data). Item sem fonte não entra.
- Opcional: com o Apify, levante Reels de alto engajamento do nicho para fazer engenharia reversa. Copie a estrutura, nunca o conteúdo.

## 2. Ganchos e roteiros

Crie um Google Doc em `Roteiros/` chamado `ROTEIROS — Semana DD/MM a DD/MM — <Marca>`, com as datas da semana que vai ao ar (no @joanastanieski, a semana-alvo de quarta a terça), nunca as da semana em que o Doc foi feito:

- Lista **numerada** de ganchos, cada um com uma checkbox `☐` para o cliente marcar, o tipo, a duração e o CTA. Agrupe os ganchos por cenário de gravação (sentado, tela, em pé). Assim o cliente grava um bloco de cada vez.
- **Mix:**
  - A maioria são aulas virais (ensino que dá vontade de salvar).
  - Uma parte é polêmica que termina em ensino.
  - O restante é bastidor ou prova.
- **Durações:** curto de 30–45s e longo de 60–90s. Inclua pelo menos 1 série por semana (parte 1, 2, 3).
- **Cada roteiro informa:**
  - **Formato validado.** Comece pelos fáceis: tela dividida e tela verde. Depois: palestrinha, narrado e storytelling visual. Formatos com outras pessoas só com OK do cliente, caso a caso.
  - **Estrutura:** AIDA, Jeito errado x jeito certo, IHC (identificação, história, conteúdo), Ele/Eu/Você e o futuro, ou Análise.
  - **Arco:** gancho (0–3s) → interesse → desejo + ação.
  - **Ingredientes:** contraste, conflito e familiaridade, com promessa clara e um momento "ahá".
  - Texto na tela, legenda, frase da capa e CTA.
- **Ganchos de comprador.** Nomeie o cargo, o porte ou a dor do ICP já no gancho. Fale de dinheiro, tempo, time e concorrente. Evite ganchos que só atraem curiosos, como "top ferramentas grátis" ou trends sem mecanismo.
- **Exagero.** O gancho pode exagerar no tom. O fato correto, com a fonte, vai na legenda ou numa seção NOTAS no fim do Doc. Nunca use dado falso nem claim fora da lista aprovada.

## 3. Gravação (quem grava é o cliente)

- O cliente grava em lote com um teleprompter (ex.: Instagram Edits) e sobe os vídeos em `Brutos/`, com o nome no formato `NN-palavra-do-gancho.mp4`.
- Nenhum Reel é agendado antes de o bruto estar na pasta.

## 4. Edição (no box)

1. Baixe o bruto do Drive para o box.
2. `python3 ~/conteudo/scripts/editar_reel.py BRUTO.mp4 NN-final.mp4`. O script:
   - reduz ruído (passa-alta 80 Hz + `afftdn` + `loudnorm` −14 LUFS);
   - transcreve com faster-whisper, com tempo por palavra;
   - queima a legenda em blocos de 3 palavras, em CAIXA ALTA, branca, extra-bold e com contorno.
3. **Revise a legenda.** Abra o `NN-final.srt`, corrija nomes, termos e palavras perdidas e rode de novo com `--srt NN-final.srt`. O Whisper erra nomes próprios e palavras curtas.
4. Gere uma folha de contato com 3 ou 4 frames (`ffmpeg ... hstack`) e olhe antes de entregar. A legenda não pode cobrir o rosto nem a UI do Instagram.
5. Salve o vídeo em `Editados/`.

## 5. Capa

- `python3 ~/conteudo/scripts/capa_reel.py BRUTO.mp4 "FRASE DE 3 A 5 PALAVRAS" NN-capa.jpg --t <segundo> [--tag "ETIQUETA"]`.
- Use o **bruto**, não o editado, para a legenda queimada não aparecer na capa.
- Escolha um segundo em que o rosto esteja natural, com olhos abertos e sem boca torta.
- **Padrão:** frase de 3–5 palavras, toda em letra grande, extra-bold e branca, centralizada na área segura do grid (o miolo 4:5).
- **Teste:** abra o `NN-capa_200px.jpg`. Se não der para ler em 200px, encurte a frase.
- Para seguir o estilo do cliente (fonte e cor), use `--font` e as regras do intake.
- Salve em `Capas/`.

## 6. Legenda e CTA

Crie um Doc em `Legendas/` com **o mesmo nome do vídeo**, com esta estrutura:

1. Linha 1 continuando o gancho.
2. De 2 a 4 linhas de valor: o ensino e o fato correto, com a fonte.
3. Uma prova aprovada.
4. CTA: "Comenta PALAVRA que eu te mando … no direct".
5. De 3 a 5 hashtags do nicho.

A palavra-chave dispara uma DM automática no Zernio. Veja a seção 7.

## 7. Zernio — notas de uso (obrigatórias)

- **Descubra as ferramentas antes de chamar.** O conector expõe ferramentas básicas (`posts_create`, `posts_update`, `posts_list`, `accounts_list`, `analytics_*`) e um catálogo completo via `search_tools` + `call_tool` (ex.: `posts_create_post`, `comment_automations_*`, `ad_campaigns_*`). Leia o schema de cada uma antes de usar.
- **Conta certa.** Rode `accounts_list` e sempre passe o `account_id`, porque agências têm várias contas.
- **Mídia.** O vídeo precisa de uma URL pública HTTPS. Opções:
  - `media_generate_upload_link`: o cliente sobe pelo navegador e você confere com `media_check_upload_status`;
  - presign do Zernio;
  - arquivo do Drive conectado ao Zernio (`fileId` + `accountId`).
  - Valide com `validate_media`.
- **Agendar com capa (preferido).** Use `call_tool` → `posts_create_post`. Passe:
  - `media_items` com o vídeo e `instagramThumbnail` (URL pública da capa);
  - o horário em ISO **com offset** (ex.: `2026-11-18T18:30:00-03:00`), na data do campo Data da linha, e o `timezone` do cliente. Data já passada não agenda.
  - Antes, rode um `validate_post` como teste.
- **Agendar no modo simples.** `posts_create` só aceita `schedule_minutes` (minutos a partir de agora). Crie com um valor qualquer no futuro e logo depois ajuste com `posts_update`, passando `scheduled_for` em ISO com offset. Confira o horário final com `posts_get`.
- **Nunca use "publicar agora"** (`publish_now`, `posts_publish_now`). Ele publica na hora, e cada nova tentativa duplica o post. Se uma criação der erro ou timeout, rode `posts_list` (status scheduled) **antes** de tentar de novo, para não duplicar.
- **Stories** podem ser agendados como `contentType: story` no `posts_create_post`. Para manter a ordem, deixe 1 minuto entre os frames. Enquete, link e figurinhas interativas não são agendáveis: o cliente posta esses no app.
- **Automações de DM (palavra-chave):**
  - Liste com `comment_automations_list_comment_automations` e veja os logs com `comment_automations_list_comment_automation_logs`.
  - Pode criar com `comment_automations_create_comment_automation`, mas só com OK do cliente sobre o texto da DM.
  - **Regra operacional:** não conte com a edição de uma automação existente pelo conector. Na operação de origem deste método, mudar o texto da DM pelo conector não funcionou de forma confiável. Peça ao cliente para editar no painel do Zernio e depois confira com `get`/`list`.
  - Antes do primeiro post com uma palavra nova, confira se a automação existe, está ativa e se o link entregue está público.
- **Anúncios.** Crie sempre **pausados**. `ad_campaigns_create_ad_campaign` já cria pausado. No `boost_post`, deixe ou ponha em pausa logo em seguida. Quem ativa é só o cliente, com orçamento aprovado por escrito. Não gaste nada sem OK.
- **Saúde da conta.** Use `accounts_get_all_accounts_health`. Se o token estiver inválido ou perto de vencer, avise o cliente para reconectar a conta no Zernio. O agente não reconecta sozinho.

## 8. Agendamento (só depois do "aprovado")

- Agende somente o que foi aprovado (no @joanastanieski, peça por peça, com o OK final da Joana).
- **Cadência:** a do intake. Sem histórico, teste 3 horários por dia durante 2 semanas e coloque o Reel mais forte no horário vencedor. `analytics_get_best_time_to_post` ajuda, mas o horário vem em UTC: converta.
- Registre o ID de cada post num arquivo ou numa tabela da semana.
- Depois de publicado, mova o vídeo, a capa e a legenda para `Já postados/`.

## 9. Revisão por lote

- Lotes de 3 no mesmo formato.
- Toda semana, puxe por Reel: views, retenção 3s, tempo médio, salvamentos, compartilhamentos, seguidores ganhos e palavras-chave recebidas.
- Refaça os 2 melhores ganchos em outro formato. Corte o formato que ficar 2 lotes seguidos abaixo da média.

## Guardrails

- Não publique, não agende e não gaste nada sem OK do cliente.
- Não invente número, depoimento ou métrica. Quando faltar, escreva "sem dado".
- Vídeo de avatar ou gerado por IA só vai ao ar depois de o cliente aprovar o vídeo final.
- Marca consistente: mesma capa, tom e mecanismo.
- Reporte só o que você verificou. Nunca diga "agendado" ou "rodando" sem conferir.
- Toda correção do cliente vira regra: salve na memória e na seção "Regras do cliente" do intake.

## Apêndice A — `~/conteudo/scripts/editar_reel.py`

~~~python
#!/usr/bin/env python3
"""Edita um Reel bruto: redução de ruído + legenda queimada (estilo Captions).
Uso: python3 editar_reel.py ENTRADA.mp4 SAIDA.mp4 [--lang pt] [--font "Montserrat"] [--words 3]
Requer: ffmpeg (com libass) e `pip install faster-whisper`.
Gera também SAIDA.srt (legenda) e SAIDA.words.json (palavras com tempo) ao lado da saída.
"""
import argparse, json, subprocess, tempfile, os

p = argparse.ArgumentParser()
p.add_argument("inp"); p.add_argument("out")
p.add_argument("--lang", default="pt")
p.add_argument("--font", default="Montserrat")
p.add_argument("--words", type=int, default=3, help="palavras por bloco de legenda")
p.add_argument("--model", default="medium")
p.add_argument("--srt", default="", help="SRT já revisado: pula o Whisper e queima este texto")
p.add_argument("--marginv", type=int, default=560, help="distância da base (px em 1920) — fora da UI do Instagram")
a = p.parse_args()
tmp = tempfile.mkdtemp()
wav = os.path.join(tmp, "clean.wav")

# 1) Redução de ruído: passa-alta 80 Hz + afftdn (FFT) + normalização de loudness para -14 LUFS
subprocess.run(["ffmpeg", "-v", "error", "-y", "-i", a.inp, "-vn", "-ac", "1", "-ar", "48000",
                "-af", "highpass=f=80,afftdn=nr=12:nf=-30:tn=1,loudnorm=I=-14:TP=-1.5:LRA=11", wav], check=True)

# 2) Transcrição com tempo por palavra (ou SRT revisado)
base = os.path.splitext(a.out)[0]
def from_srt(path):
    import re
    out = []
    for blk in open(path, encoding="utf-8").read().strip().split("\n\n"):
        ls = blk.strip().splitlines()
        if len(ls) < 3: continue
        t = re.findall(r"(\d+):(\d+):(\d+),(\d+)", ls[1])
        st, en = [int(h)*3600+int(m_)*60+int(s_)+int(ms)/1000 for h, m_, s_, ms in t]
        out.append([[st, en, " ".join(ls[2:])]])
    return out
if a.srt:
    blocks = from_srt(a.srt); W = [w for b in blocks for w in b]
else:
  from faster_whisper import WhisperModel
  m = WhisperModel(a.model, device="cpu", compute_type="int8")
  import numpy as np  # decodifica via ffmpeg (evita incompatibilidade de versões do PyAV)
  pcm = subprocess.run(["ffmpeg", "-v", "error", "-i", wav, "-ac", "1", "-ar", "16000", "-f", "s16le", "-"], capture_output=True, check=True).stdout
  audio = np.frombuffer(pcm, np.int16).astype(np.float32) / 32768
  segs, _ = m.transcribe(audio, language=a.lang, word_timestamps=True, vad_filter=True)
  W = [[w.start, w.end, w.word.strip()] for s in segs for w in s.words if w.word.strip()]
  json.dump(W, open(base + ".words.json", "w"), ensure_ascii=False)
  blocks = [W[i:i+a.words] for i in range(0, len(W), a.words)]

# 3) Blocos de N palavras -> ASS (branco, extra-bold, contorno preto) + SRT
def ts_ass(t): h=int(t//3600); m_=int(t%3600//60); s=t%60; return f"{h}:{m_:02d}:{s:05.2f}"
def ts_srt(t): ms=int(round(t*1000)); return f"{ms//3600000:02d}:{ms//60000%60:02d}:{ms//1000%60:02d},{ms%1000:03d}"
ass = f"""[Script Info]
ScriptType: v4.00+
PlayResX: 1080
PlayResY: 1920

[V4+ Styles]
Format: Name, Fontname, Fontsize, PrimaryColour, SecondaryColour, OutlineColour, BackColour, Bold, Italic, Underline, StrikeOut, ScaleX, ScaleY, Spacing, Angle, BorderStyle, Outline, Shadow, Alignment, MarginL, MarginR, MarginV, Encoding
Style: Cap,{a.font},96,&H00FFFFFF,&H00FFFFFF,&H00000000,&H64000000,-1,0,0,0,100,100,0,0,1,6,2,2,90,90,{a.marginv},1

[Events]
Format: Layer, Start, End, Style, Name, MarginL, MarginR, MarginV, Effect, Text
"""
srt = []
for i, b in enumerate(blocks):
    st, en = b[0][0], b[-1][1]
    if i + 1 < len(blocks): en = min(max(en, st + 0.3), blocks[i+1][0][0])
    txt = " ".join(w[2] for w in b).upper()
    ass += f"Dialogue: 0,{ts_ass(st)},{ts_ass(en)},Cap,,0,0,0,,{txt}\n"
    srt.append(f"{i+1}\n{ts_srt(st)} --> {ts_srt(en)}\n{' '.join(w[2] for w in b)}\n")
assf = os.path.join(tmp, "caps.ass"); open(assf, "w").write(ass)
if not a.srt: open(base + ".srt", "w").write("\n".join(srt))

# 4) Render 1080x1920, áudio limpo, legenda queimada
vf = f"scale=1080:1920:force_original_aspect_ratio=increase,crop=1080:1920,setsar=1,ass={assf}"
subprocess.run(["ffmpeg", "-v", "error", "-y", "-i", a.inp, "-i", wav, "-map", "0:v:0", "-map", "1:a:0",
                "-vf", vf, "-c:v", "libx264", "-preset", "medium", "-crf", "20", "-pix_fmt", "yuv420p", "-r", "30",
                "-c:a", "aac", "-b:a", "128k", "-ar", "44100", "-movflags", "+faststart", "-shortest", a.out], check=True)
print("OK", a.out, f"{len(W)} palavras, {len(blocks)} blocos")
~~~

## Apêndice B — `~/conteudo/scripts/capa_reel.py`

~~~python
#!/usr/bin/env python3
"""Gera a capa de um Reel (1080x1920) a partir de um frame do vídeo.
Uso: python3 capa_reel.py VIDEO.mp4 "FRASE DE 3 A 5 PALAVRAS" SAIDA.jpg [--t 2.0] [--font CAMINHO.ttf] [--tag "ETIQUETA"]
Spec: frame natural do rosto; frase em CAIXA ALTA, branca, extra-bold, centralizada na área
segura do grid (o miolo 1080x1350 que aparece no perfil, e longe das bordas); sombra para leitura.
Gera também SAIDA_200px.jpg (teste de legibilidade em 200px de largura). Requer ffmpeg + Pillow.
"""
import argparse, subprocess, tempfile, os
from PIL import Image, ImageDraw, ImageFont, ImageFilter

p = argparse.ArgumentParser()
p.add_argument("video"); p.add_argument("frase"); p.add_argument("out")
p.add_argument("--t", type=float, default=2.0, help="segundo do frame (escolha um com o rosto natural)")
p.add_argument("--font", default="", help="TTF extra-bold/black (ex.: Montserrat-ExtraBold.ttf)")
p.add_argument("--tag", default="", help="etiqueta pequena opcional no topo da área segura")
a = p.parse_args()
words = a.frase.split()
if not 3 <= len(words) <= 5: print(f"AVISO: a frase tem {len(words)} palavras (padrão: 3 a 5)")

fr = os.path.join(tempfile.mkdtemp(), "f.png")
subprocess.run(["ffmpeg", "-v", "error", "-y", "-ss", str(a.t), "-i", a.video, "-frames:v", "1",
                "-vf", "scale=1080:1920:force_original_aspect_ratio=increase,crop=1080:1920", fr], check=True)
img = Image.open(fr).convert("RGB")

def font(sz):
    cands = [a.font] if a.font else []
    cands += ["/usr/share/fonts/truetype/sand-box/google/Montserrat/Montserrat-VariableFont_wght.ttf",
              "/usr/share/fonts/truetype/dejavu/DejaVuSans-Bold.ttf"]
    for c in cands:
        if c and os.path.exists(c):
            f = ImageFont.truetype(c, sz)
            try: f.set_variation_by_name("ExtraBold")
            except Exception: pass
            return f
    return ImageFont.load_default(sz)

# Área segura: miolo 4:5 (1080x1350, y 285..1635), com 90px de margem lateral.
SAFE_X0, SAFE_X1, SAFE_Y0, SAFE_Y1 = 90, 990, 285, 1635
text = a.frase.upper()
# quebra em até 3 linhas equilibradas e acha o maior tamanho que cabe
def layout(sz):
    f = font(sz); d = ImageDraw.Draw(img)
    best = None
    for n in range(1, min(3, len(words)) + 1):
        per = -(-len(words) // n)
        lines = [" ".join(words[i:i+per]).upper() for i in range(0, len(words), per)]
        w = max(d.textlength(l, font=f) for l in lines)
        if w <= SAFE_X1 - SAFE_X0 and (best is None or w < best[1]): best = (lines, w)
    return f, best
sz = 200
while sz > 60:
    f, best = layout(sz)
    if best: break
    sz -= 6
lines = best[0]
lh = int(sz * 1.05); total_h = lh * len(lines)
y0 = SAFE_Y0 + (SAFE_Y1 - SAFE_Y0) * 0.62 - total_h / 2   # centro-baixo da área segura, sem cobrir o rosto

shadow = Image.new("RGBA", img.size, (0, 0, 0, 0)); sd = ImageDraw.Draw(shadow)
for i, l in enumerate(lines):
    w = sd.textlength(l, font=f); x = (1080 - w) / 2; y = y0 + i * lh
    sd.text((x + 6, y + 8), l, font=f, fill=(0, 0, 0, 200))
shadow = shadow.filter(ImageFilter.GaussianBlur(10))
img = Image.alpha_composite(img.convert("RGBA"), shadow); d = ImageDraw.Draw(img)
for i, l in enumerate(lines):
    w = d.textlength(l, font=f); x = (1080 - w) / 2; y = y0 + i * lh
    d.text((x, y), l, font=f, fill="white", stroke_width=max(2, sz // 40), stroke_fill="black")
if a.tag:
    tf = font(40); tw = d.textlength(a.tag.upper(), font=tf)
    d.rounded_rectangle(((1080 - tw) / 2 - 24, SAFE_Y0 + 20, (1080 + tw) / 2 + 24, SAFE_Y0 + 84), 14, fill=(0, 0, 0, 170))
    d.text(((1080 - tw) / 2, SAFE_Y0 + 30), a.tag.upper(), font=tf, fill="white")
img = img.convert("RGB"); img.save(a.out, quality=92)
img.crop((0, 285, 1080, 1635)).resize((200, 250)).save(os.path.splitext(a.out)[0] + "_200px.jpg", quality=90)
print("OK", a.out, "fonte", sz, "linhas", lines)
~~~
