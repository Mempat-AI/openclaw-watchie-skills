# Watchie OpenClaw Skills

**Language:** English | [中文](./README.zh-CN.md) | [Bahasa Melayu](./README.ms.md)

Reusable OpenClaw skills for Watchie workflows.

## Included skills

- `gen-music`: generate songs through an ACE-Step-compatible API backend, save stable output files, and optionally play results on Watchie.
- `youtube-music`: experimental personal-use helper that downloads YouTube or YouTube Music audio into stable local files, with optional Watchie playback.
- `story-teller`: writing-focused storytelling skill for vivid, voice-friendly stories.

## Install

```bash
git clone https://github.com/Mempat-AI/openclaw-watchie-skills.git
mkdir -p ~/.openclaw/skills
cp -R openclaw-watchie-skills/skills/gen-music ~/.openclaw/skills/
cp -R openclaw-watchie-skills/skills/youtube-music ~/.openclaw/skills/
cp -R openclaw-watchie-skills/skills/story-teller ~/.openclaw/skills/
```

Restart OpenClaw Gateway or start a new OpenClaw session after copying skills.

## Recommended Watchie setup

1. Install the Watchie plugin package: `@mempat-ai/watchie`.
2. Sign in and pair your watch:
   - `openclaw watchie login <countryCode> <phoneNumber>`
   - `openclaw watchie pair <imei>`
3. Install `gen-music` if you want text-to-music flows.
4. Install `youtube-music` if you want best-effort YouTube/YouTube Music downloads.
5. Point `gen-music` to your ACE-Step-compatible backend (local or remote).

## Example requests

- `Generate a playful one-minute beach pop song and save the audio.`
- `Generate a happy song and play it on watch 860000019579324.`
- `Download this YouTube Music link as mp3.`
- `Find this song on YouTube Music, save it locally, then play it on my watch.`
- `Tell me a bedtime story about a brave rabbit.`

## Requirements

- Python 3
- `ffmpeg` and local `yt-dlp` for `youtube-music`
- An ACE-Step-compatible backend for `gen-music`
- Watchie plugin, if you want watch playback

## Notes

- `gen-music` does not bundle ACE-Step model weights or service binaries.
- You can use either a local ACE-Step server or a remote compatible endpoint.
