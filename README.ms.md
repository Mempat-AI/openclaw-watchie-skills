# Watchie OpenClaw Skills

**Bahasa:** [English](./README.md) | [中文](./README.zh-CN.md) | Bahasa Melayu

Koleksi skill OpenClaw yang boleh diguna semula untuk aliran kerja Watchie.

## Skill yang disediakan

- `gen-music`: jana lagu melalui backend serasi ACE-Step, simpan fail output yang stabil, dan pilihan untuk main pada Watchie.
- `youtube-music`: pembantu eksperimen untuk kegunaan peribadi, muat turun audio YouTube / YouTube Music ke fail tempatan yang stabil, dengan pilihan main pada Watchie.
- `story-teller`: skill penceritaan berfokus penulisan untuk cerita yang lebih hidup dan sesuai dibacakan.

## Pasang

```bash
git clone https://github.com/Mempat-AI/openclaw-watchie-skills.git
mkdir -p ~/.openclaw/skills
cp -R openclaw-watchie-skills/skills/gen-music ~/.openclaw/skills/
cp -R openclaw-watchie-skills/skills/youtube-music ~/.openclaw/skills/
cp -R openclaw-watchie-skills/skills/story-teller ~/.openclaw/skills/
```

Selepas menyalin skill, mulakan semula OpenClaw Gateway atau buka sesi OpenClaw baharu.

## Setup Watchie yang disyorkan

1. Pasang pakej plugin Watchie: `@mempat-ai/watchie`.
2. Log masuk dan padankan jam:
   - `openclaw watchie login <kodNegara> <nomborTelefon>`
   - `openclaw watchie pair <imei>`
3. Pasang `gen-music` jika anda mahu aliran teks-ke-muzik.
4. Pasang `youtube-music` jika anda mahu muat turun YouTube / YouTube Music secara best-effort.
5. Tetapkan `gen-music` kepada backend serasi ACE-Step anda (tempatan atau jauh).

## Contoh permintaan

- `Generate a playful one-minute beach pop song and save the audio.`
- `Generate a happy song and play it on watch 860000019579324.`
- `Download this YouTube Music link as mp3.`
- `Find this song on YouTube Music, save it locally, then play it on my watch.`
- `Tell me a bedtime story about a brave rabbit.`

## Keperluan

- Python 3
- `youtube-music` memerlukan `ffmpeg` dan `yt-dlp` secara tempatan
- `gen-music` memerlukan backend serasi ACE-Step
- Plugin Watchie jika anda mahu main balik pada jam

## Nota

- `gen-music` tidak membungkus berat model atau binari servis ACE-Step.
- Anda boleh gunakan pelayan ACE-Step tempatan atau endpoint serasi jauh.
