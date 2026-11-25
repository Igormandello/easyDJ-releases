# easyDJ

**English** · [Português](#português)

easyDJ is a desktop app for DJs that turns "I found some tracks online" into "they're on my USB stick, sorted". It:

- **downloads** whole YouTube channels, SoundCloud artists and Spotify links (track, album, playlist or artist) as 320 kbps MP3s, or as WAV when SoundCloud offers the lossless original;
- lets you **review** each song quickly: listen to a few parts, then 👍 or 👎, and tag it with your own labels (genres, moods, anything);
- detects **BPM and key** (Camelot) and shows which songs mix with the one you're playing;
- builds **playlists** in the order you want;
- **exports** the liked songs to a USB stick or a folder, one folder per label, ready for your DJ software or CDJs.

It runs on your computer, needs no account, and speaks English or Portuguese (it follows your computer's language; switch it in the PT/EN menu at the top).

## Download

| System | File |
|---|---|
| **Mac** with Apple Silicon (M1, M2, M3, M4…) | [easyDJ.dmg](https://github.com/Igormandello/easyDJ-releases/releases/latest/download/easyDJ.dmg) |
| **Windows** 10 or 11, 64-bit | [easyDJ-Setup.exe](https://github.com/Igormandello/easyDJ-releases/releases/latest/download/easyDJ-Setup.exe) |

All versions: [Releases](https://github.com/Igormandello/easyDJ-releases/releases). Intel Macs aren't supported.

## Install

### Mac

1. Open `easyDJ.dmg`.
2. Drag **easyDJ** to the **Applications** folder.
3. Eject the "easyDJ" disk in Finder.

**The first time you open it:** the app isn't from the App Store, so the Mac says it can't verify it. Click **OK** / **Done**, then go to **System Settings > Privacy & Security**, scroll to the bottom and click **Open Anyway** next to easyDJ. Confirm with your Mac password. You only do this once. (Right-click > Open no longer works on macOS 15 and newer.)

**The first time you download something,** the Mac may ask for access to **"Chrome Safe Storage"** in Keychain. Type your Mac password and click **Always Allow**. easyDJ reads Google Chrome's cookies so YouTube doesn't ask you to "confirm you're not a bot". The prompt may come back after an update; just allow it again.

### Windows

1. Open `easyDJ-Setup.exe`.
2. If **"Windows protected your PC"** appears, click **More info**, then **Run anyway**. (It shows up because the app has no paid signature; that's normal.)
3. Follow the installer. You don't need to be an administrator. Tick "Create a desktop shortcut" if you like.

easyDJ uses Microsoft Edge WebView2 for its window; it already comes with Windows 10 and 11.

## First run

1. easyDJ asks for a **library folder**. Pick (or create) a folder just for this, e.g. `Documents/easyDJ Music`. Every artist/channel you download becomes a subfolder in it. To change it later: **easyDJ menu > Change library folder…**
2. Sign in to YouTube in **Google Chrome** on the same computer. This avoids YouTube's "not a bot" check. (On Windows, Firefox is used instead when it's installed, since Chrome blocks access to its cookies there.)
3. Optional: sign in to SoundCloud in Chrome too. Some artists only allow downloading the original (WAV) to logged-in users.

## How to use

### 1. Download songs (⬇ Download)

1. Click **⬇ Download** at the top left.
2. Under **New links**, paste a link and press Enter. It becomes a chip; add as many as you want. Accepted links:
   - a YouTube channel (`https://www.youtube.com/@name`), video or playlist;
   - a SoundCloud artist (`https://soundcloud.com/name`), track or playlist;
   - a Spotify track, album, playlist or artist. The audio comes from YouTube Music (Spotify's own audio is protected), and a Spotify playlist also becomes an easyDJ playlist.
3. Set the filters if you want:
   - **From**: skip songs older than this date;
   - **Max. length**: skip anything longer (default 5 min, so full sets and mixes are skipped);
   - **Only the N newest per source**: leave it empty for all of them.
4. Click **⬇ Download**. You can close the dialog and keep reviewing while it runs; **■ Stop** stops it, and the next run picks up where it left off.

Songs you already have are skipped, including re-uploads with a slightly different title, and songs you deleted never come back.

Every link you download is remembered under **Sources**. Later, **↻ Check all** counts how many new songs each source has (nothing is downloaded), and **⬇ Download new** fetches only those. **Last download** lists the songs that failed, if any.

### 2. Review (👍 / 👎 and labels)

The left side lists your songs. The tabs filter them: **To review**, **👍 Liked**, **👎**, **All**, **🔁** (songs downloaded more than once) and **🔤** (songs with the same name). Use the search box (`/`), the label menu and the sort menu (**By artist**, **By source**, newest, oldest, most or least viewed) to narrow it down.

Open a song and:

- **Parts preview** plays a few short parts spread through the song, so you hear the intro, the drop and the end in seconds. Set how many **Parts** and how many **Seconds each**, or untick it to play the whole song. Click the waveform to jump anywhere.
- Press **👍 Like** (`L`) or **👎 Dislike** (`D`). With **Go to the next one after 👍/👎** ticked, the next unreviewed song opens by itself; otherwise press **Next to review →** (`Enter`).
- Click a label chip, or press `1`–`9`, to tag the song. Type in **+ new label** to create one. A song can have several labels.
- **✎** edits the song's name; **🗑 Delete song** removes the file for good (it asks first).
- In **🔁**, the copies of a repeated song are listed together so you can keep the best one (e.g. the WAV) and delete the rest.

Everything is saved as you go. There is no Save button.

### 3. BPM, key and compatible songs

easyDJ works out each song's **BPM** and **key** (Camelot notation, like `8A`) in the background; the top of the list shows the progress. Click **🎚 Compatible** on a song to show only the songs that mix with it: a matching key (same, ±1 on the wheel, or its relative) and a close BPM (or half/double). Click the chip again to show everything.

### 4. Playlists

- Type a name in **+ new playlist** under a song, or pick one in the playlist menu on the left.
- In playlist mode, the playlist sits at the top in order, with the other songs below as candidates.
- `P` adds the open song to the playlist (right after the last one you added) or removes it if it's already in.
- `Shift`+`↑`/`↓` moves the open song up or down in the playlist.

### 5. Export to a USB stick (💾 Export)

1. Plug in the USB stick.
2. Click **💾 Export**, choose the stick under **Destination** (or **📁 A folder…** to export anywhere else), and click **💾 Export**.

easyDJ creates an `easyDJ` folder on the stick with:

```
easyDJ/
  All liked/          every 👍 song
  <Label>/            one folder per label, with its 👍 songs
  Playlists/<name>/   each playlist, numbered in order (01 - …, 02 - …)
```

Export again whenever you like: it only copies what changed and removes what you no longer like. It only ever touches its own `easyDJ` folder, never the rest of the stick.

## Keyboard shortcuts

| Key | Action |
|---|---|
| `Space` | play / pause |
| `←` `→` | previous / next part |
| `Shift` + `←` `→` | back / forward 10 seconds |
| `↑` `↓` | previous / next song in the list |
| `L` | like 👍 |
| `D` | dislike 👎 |
| `1`–`9` | toggle label 1–9 |
| `Enter` or `N` | next song to review |
| `/` | search |
| `P` | add to / remove from the playlist |
| `Shift` + `↑` `↓` | move the song in the playlist |

## Updates

easyDJ checks for new versions on its own. When one is ready, a "New version available" banner shows up: click **Install and restart**. Your library, likes, labels and playlists are kept.

## Where are my files?

- **Music:** in the library folder you picked, one subfolder per artist or channel, named `<song> - <DJs>.mp3` (or `.wav`). Each subfolder also has a `report.csv` with your likes and labels; you can open it in Excel.
- **App settings and log:**
  - Mac: `~/Library/Application Support/easyDJ/` (in Finder: **Go > Go to Folder…** and paste it)
  - Windows: `%APPDATA%\easyDJ\` (press **Windows + R**, paste it, press Enter)

## Troubleshooting

- **YouTube says "confirm you're not a bot" / downloads fail:** sign in to YouTube in Google Chrome on the same computer and, on a Mac, allow "Chrome Safe Storage" when asked. Downloading a lot at once can also trigger it; wait a while and try again.
- **A SoundCloud song came as MP3, not WAV:** the artist only allows the original to logged-in users (sign in to SoundCloud in Chrome) or doesn't allow downloads at all.
- **A song is missing after a download:** see **Last download** in the ⬇ Download dialog. It may have been skipped as a repeat, longer than the max. length, or older than the date filter.
- **The Mac won't open the app:** see [Install > Mac](#mac) (Open Anyway).
- **Something else went wrong:** send the `app.log` file from the folder above to whoever gave you the app.

---

# Português

[English](#easydj) · **Português**

O easyDJ é um app para DJs que transforma "achei umas faixas na internet" em "já estão no pendrive, organizadas". Ele:

- **baixa** canais inteiros do YouTube, artistas do SoundCloud e links do Spotify (música, álbum, playlist ou artista) em MP3 320 kbps, ou em WAV quando o SoundCloud tem o original sem perda;
- deixa você **revisar** cada música rapidinho: ouve algumas partes, dá 👍 ou 👎 e marca com as suas etiquetas (subgênero, clima, o que quiser);
- detecta **BPM e tom** (Camelot) e mostra quais músicas combinam com a que está tocando;
- monta **playlists** na ordem que você quiser;
- **exporta** as curtidas para o pendrive ou uma pasta, uma pasta por etiqueta, prontas para o seu software de DJ ou CDJ.

Roda no seu computador, não precisa de conta e fica em português ou inglês (segue o idioma do computador; troque no menu PT/EN no topo).

## Baixar

| Sistema | Arquivo |
|---|---|
| **Mac** com Apple Silicon (M1, M2, M3, M4…) | [easyDJ.dmg](https://github.com/Igormandello/easyDJ-releases/releases/latest/download/easyDJ.dmg) |
| **Windows** 10 ou 11, 64 bits | [easyDJ-Setup.exe](https://github.com/Igormandello/easyDJ-releases/releases/latest/download/easyDJ-Setup.exe) |

Todas as versões: [Releases](https://github.com/Igormandello/easyDJ-releases/releases). Macs com Intel não são suportados.

## Instalar

### Mac

1. Abra o `easyDJ.dmg`.
2. Arraste o **easyDJ** para a pasta **Aplicativos**.
3. Ejete o disco "easyDJ" no Finder.

**Na primeira vez que abrir:** o app não é da App Store, então o Mac diz que não pode verificá-lo. Clique em **OK** / **Concluído**, vá em **Ajustes do Sistema > Privacidade e Segurança**, desça até o fim e clique em **Abrir Mesmo Assim** ao lado do easyDJ. Confirme com a senha do Mac. Só precisa fazer isso uma vez. (Botão direito > Abrir não funciona mais no macOS 15 ou mais novo.)

**Na primeira vez que baixar algo,** o Mac pode pedir acesso a **"Chrome Safe Storage"** nas Chaves. Digite a senha do Mac e clique em **Sempre Permitir**. O easyDJ usa os cookies do Google Chrome para o YouTube não pedir "confirme que você não é um robô". O pedido pode voltar depois de uma atualização; é só permitir de novo.

### Windows

1. Abra o `easyDJ-Setup.exe`.
2. Se aparecer **"O Windows protegeu o computador"**, clique em **Mais informações** e depois em **Executar assim mesmo**. (Aparece porque o app não tem assinatura paga; é normal.)
3. Siga o instalador. Não precisa ser administrador. Marque "Criar um atalho na Área de Trabalho" se quiser.

O easyDJ usa o Microsoft Edge WebView2 para mostrar a janela; ele já vem no Windows 10 e 11.

## Na primeira vez

1. O easyDJ pede uma **pasta para a biblioteca**. Escolha (ou crie) uma pasta só para isso, por exemplo `Documentos/Músicas easyDJ`. Cada artista/canal baixado vira uma subpasta dela. Para trocar depois: **menu easyDJ > Trocar pasta da biblioteca…**
2. Entre na sua conta do YouTube no **Google Chrome**, no mesmo computador. Isso evita o aviso de robô do YouTube. (No Windows, se o Firefox estiver instalado, ele é usado no lugar, porque lá o Chrome bloqueia os cookies.)
3. Opcional: entre no SoundCloud pelo Chrome também. Alguns artistas só liberam o original (WAV) para quem está logado.

## Como usar

### 1. Baixar músicas (⬇ Baixar)

1. Clique em **⬇ Baixar**, no canto de cima à esquerda.
2. Em **Links novos**, cole um link e tecle Enter. Ele vira uma etiqueta; adicione quantos quiser. Links aceitos:
   - canal do YouTube (`https://www.youtube.com/@nome`), vídeo ou playlist;
   - artista do SoundCloud (`https://soundcloud.com/nome`), faixa ou playlist;
   - música, álbum, playlist ou artista do Spotify. O áudio vem do YouTube Music (o do Spotify é protegido), e uma playlist do Spotify também vira uma playlist no easyDJ.
3. Ajuste os filtros se quiser:
   - **A partir de**: pula músicas mais antigas que essa data;
   - **Duração máx.**: pula o que for mais longo (5 min por padrão, então sets e mixagens ficam de fora);
   - **Só as N mais novas por origem**: deixe vazio para baixar todas.
4. Clique em **⬇ Baixar**. Pode fechar a janela e continuar revisando enquanto baixa; **■ Parar** interrompe, e a próxima vez continua de onde parou.

Músicas que você já tem são puladas, inclusive reenvios com título um pouco diferente, e as que você apagou não voltam.

Todo link baixado fica guardado em **Origens**. Depois, **↻ Verificar todos** conta quantas músicas novas cada origem tem (sem baixar nada), e **⬇ Baixar novas** baixa só essas. **Último download** mostra as músicas que falharam, se houver.

### 2. Revisar (👍 / 👎 e etiquetas)

À esquerda fica a lista de músicas. As abas filtram: **A revisar**, **👍 Curtidas**, **👎**, **Todas**, **🔁** (músicas baixadas mais de uma vez) e **🔤** (músicas com o mesmo nome). Use a busca (`/`), o menu de etiquetas e o de ordem (**Por artista**, **Por origem**, mais novas, mais antigas, mais ou menos vistas) para filtrar.

Abra uma música e:

- **Prévia em partes** toca alguns trechos curtos espalhados pela música, para ouvir o começo, o meio e o fim em segundos. Escolha quantas **Partes** e quantos **Segundos cada**, ou desmarque para tocar a música inteira. Clique na onda para pular para qualquer ponto.
- Aperte **👍 Curtir** (`L`) ou **👎 Não curti** (`D`). Com **Ir para a próxima depois de 👍/👎** marcado, a próxima música a revisar abre sozinha; senão, aperte **Próxima a revisar →** (`Enter`).
- Clique numa etiqueta, ou aperte `1`–`9`, para marcar a música. Digite em **+ nova etiqueta** para criar uma. Uma música pode ter várias.
- **✎** edita o nome da música; **🗑 Apagar música** apaga o arquivo de vez (pergunta antes).
- Em **🔁**, as cópias de uma música repetida aparecem juntas, para você ficar com a melhor (por exemplo, o WAV) e apagar as outras.

Tudo é salvo na hora. Não tem botão de salvar.

### 3. BPM, tom e músicas compatíveis

O easyDJ calcula o **BPM** e o **tom** (notação Camelot, tipo `8A`) de cada música em segundo plano; o topo da lista mostra o progresso. Clique em **🎚 Compatíveis** numa música para ver só as que combinam com ela: tom compatível (igual, ±1 na roda ou o relativo) e BPM próximo (ou metade/dobro). Clique de novo na etiqueta para ver todas.

### 4. Playlists

- Digite um nome em **+ nova playlist** embaixo de uma música, ou escolha uma no menu de playlists à esquerda.
- No modo playlist, a playlist fica no topo, na ordem, e as outras músicas embaixo como candidatas.
- `P` põe a música aberta na playlist (logo depois da última que você adicionou), ou tira se ela já estiver lá.
- `Shift`+`↑`/`↓` sobe ou desce a música aberta na playlist.

### 5. Exportar para o pendrive (💾 Exportar)

1. Conecte o pendrive.
2. Clique em **💾 Exportar**, escolha o pendrive em **Destino** (ou **📁 Uma pasta…** para exportar para outro lugar) e clique em **💾 Exportar**.

O easyDJ cria uma pasta `easyDJ` no pendrive com:

```
easyDJ/
  Todas curtidas/     todas as 👍
  <Etiqueta>/         uma pasta por etiqueta, com as 👍 dela
  Playlists/<nome>/   cada playlist, numerada na ordem (01 - …, 02 - …)
```

Exporte de novo quando quiser: ele só copia o que mudou e tira o que você não curte mais. Ele só mexe na própria pasta `easyDJ`, nunca no resto do pendrive.

## Atalhos de teclado

| Tecla | Ação |
|---|---|
| `Espaço` | tocar / pausar |
| `←` `→` | parte anterior / próxima |
| `Shift` + `←` `→` | voltar / avançar 10 segundos |
| `↑` `↓` | música anterior / próxima da lista |
| `L` | curtir 👍 |
| `D` | não curti 👎 |
| `1`–`9` | liga/desliga a etiqueta 1–9 |
| `Enter` ou `N` | próxima a revisar |
| `/` | buscar |
| `P` | pôr na playlist / tirar dela |
| `Shift` + `↑` `↓` | mover a música na playlist |

## Atualizações

O easyDJ procura versões novas sozinho. Quando uma estiver pronta, aparece o aviso "Nova versão disponível": clique em **Instalar e reiniciar**. Sua biblioteca, curtidas, etiquetas e playlists continuam lá.

## Onde ficam os meus arquivos?

- **Músicas:** na pasta da biblioteca que você escolheu, uma subpasta por artista ou canal, com nomes `<música> - <DJs>.mp3` (ou `.wav`). Cada subpasta tem também um `report.csv` com as suas curtidas e etiquetas; dá para abrir no Excel.
- **Configurações e log do app:**
  - Mac: `~/Library/Application Support/easyDJ/` (no Finder: **Ir > Ir para a Pasta…** e cole o caminho)
  - Windows: `%APPDATA%\easyDJ\` (aperte **Windows + R**, cole o caminho e tecle Enter)

## Problemas

- **O YouTube pede "confirme que você não é um robô" / os downloads falham:** entre no YouTube pelo Google Chrome no mesmo computador e, no Mac, permita o "Chrome Safe Storage" quando pedir. Baixar muita coisa de uma vez também pode causar isso; espere um pouco e tente de novo.
- **Uma música do SoundCloud veio em MP3, não WAV:** o artista só libera o original para quem está logado (entre no SoundCloud pelo Chrome) ou não libera download.
- **Faltou uma música depois do download:** veja **Último download** na janela ⬇ Baixar. Ela pode ter sido pulada por ser repetida, mais longa que a duração máxima ou mais antiga que a data do filtro.
- **O Mac não abre o app:** veja [Instalar > Mac](#mac-1) (Abrir Mesmo Assim).
- **Outro problema:** mande o arquivo `app.log` da pasta acima para quem te passou o app.
