<p align="center"><img src="logo.png" width="96" alt="LuminaTrans"></p>

# LuminaTrans

Translation that sits on top of every window. Telegram, Discord, games, browsers: a small badge next to the clock, a panel that opens above it, and shortcuts that work from anywhere. Everything runs on your own computer: no subscription, no request limits, and nothing you translate leaves the machine.

## Install

1. Download the latest `LuminaTrans-Setup-x.y.z.exe` from [Releases](https://github.com/wonra16/LuminaTrans-releases/releases/latest) and run it. Windows may show a SmartScreen warning because the installer is not code-signed yet: choose More info, then Run anyway. Pick your language in the first dialog: the app opens in that language and uses it as "my language" (the other side defaults to English; English speakers get Turkish, change it in Settings).
2. On first launch a short setup runs: install **Ollama** (the local service that runs the model, official installer, one click) and download the translation model (**gemma4:e4b**, 9.6 GB, once). Speech recognition downloads its model (1.6 GB) the first time you use voice.
3. Done. The badge appears bottom right; click it to open the panel.

Requirements: Windows 10/11 64-bit, 16 GB RAM. An NVIDIA card with 6 GB+ VRAM makes everything fast (translation ~0.3 s, speech ~0.5 s); without a GPU it still works on the CPU, slower. About 15 GB of disk for the app and models.

## What it does

| Shortcut | |
|---|---|
| `Ctrl+Alt+Enter` | Translate what you typed in any input box and replace it in place, in the tone you chose. |
| `Ctrl+Alt+T` | Translate the selected text; the result lands in the Inbox tab while you stay in your app. |
| `Ctrl+Alt+V` | Speak (press, talk, press again): transcribed, translated, ready to paste. |
| `Ctrl+Alt+L` | Listen: whatever plays on your speakers (voice messages, videos, calls) becomes live subtitles at the bottom of the screen, translated. |
| `Ctrl+Alt+O` | Screen subtitles: draw a box over game dialogue or burned-in subtitles; they are read and translated as they change. |
| `Ctrl+Alt+R` | Translate a screen region once (things you cannot select). |
| `Ctrl+Alt+Space` | Show / hide the panel. |

Every translation comes in two stages: a quick plain translation first (~0.3 s), then three tones (formal, natural, emotional) with a short note on context and culture (~4 s).

Also: drop an audio, video or subtitle file on the panel to get a translated `.srt` and a text transcript; a watched folder (`Documents\LuminaTrans\Inbox`) that translates anything you put in it; a summary button after a listening session; read-aloud with natural neural voices; a glossary so names and terms stay fixed; optional clipboard watch.

## Privacy

Translation and speech recognition run locally through Ollama and Whisper. The only network use: downloading models, optional cloud providers you enable yourself (Gemini, Groq, Cerebras, Claude), and read-aloud voices. To translate a video you are watching, just press Ctrl+Alt+L while it plays.

Türkçe kılavuz: [README.tr.md](README.tr.md)

## Build from source

```
pip install -r requirements.txt
python app.py
```

`build_exe.bat` produces `dist\LuminaTrans`; `build_installer.bat` (Inno Setup 6) produces `Output\LuminaTrans-Setup-x.y.z.exe`.
