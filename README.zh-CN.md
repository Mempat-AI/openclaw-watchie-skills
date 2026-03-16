# Watchie OpenClaw Skills

**语言：** [English](./README.md) | 中文 | [Bahasa Melayu](./README.ms.md)

面向 Watchie 场景的 OpenClaw 可复用 skills 集合。

## 包含的 skills

- `gen-music`：通过 ACE-Step 兼容后端生成歌曲，保存稳定输出文件，并可选播放到 Watchie。
- `youtube-music`：实验性个人用途工具，把 YouTube / YouTube Music 音频下载为本地稳定文件，并可选播放到 Watchie。
- `story-teller`：以写作为核心的讲故事 skill，适合更生动、更适合语音播报的内容。

## 安装

```bash
git clone https://github.com/Mempat-AI/openclaw-watchie-skills.git
mkdir -p ~/.openclaw/skills
cp -R openclaw-watchie-skills/skills/gen-music ~/.openclaw/skills/
cp -R openclaw-watchie-skills/skills/youtube-music ~/.openclaw/skills/
cp -R openclaw-watchie-skills/skills/story-teller ~/.openclaw/skills/
```

复制完成后，重启 OpenClaw Gateway，或开启一个新的 OpenClaw 会话。

## 推荐的 Watchie 配置

1. 安装 Watchie 插件包：`@mempat-ai/watchie`。
2. 登录并配对手表：
   - `openclaw watchie login <国家区号> <手机号>`
   - `openclaw watchie pair <imei>`
3. 需要文字生成音乐时，安装 `gen-music`。
4. 需要 YouTube / YouTube Music 下载能力时，安装 `youtube-music`。
5. 把 `gen-music` 指向你的 ACE-Step 兼容后端（本地或远程）。

## 示例请求

- `生成一首活泼的一分钟海边流行歌并保存音频。`
- `生成一首开心的歌并播放到手表 860000019579324。`
- `把这个 YouTube Music 链接下载成 mp3。`
- `在 YouTube Music 找这首歌，保存到本地，然后发到我的手表。`
- `给我讲一个关于勇敢小兔子的睡前故事。`

## 依赖要求

- Python 3
- `youtube-music` 需要本地 `ffmpeg` 和 `yt-dlp`
- `gen-music` 需要 ACE-Step 兼容后端
- 如需手表播放，需要 Watchie 插件

## 说明

- `gen-music` 不包含 ACE-Step 模型权重或服务二进制。
- 你可以使用本地 ACE-Step 服务，也可以使用远程兼容端点。
