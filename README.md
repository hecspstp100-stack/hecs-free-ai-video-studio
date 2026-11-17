# HECS Free AI Video Studio

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hecspstp100-stack/hecs-free-ai-video-studio/blob/main/HECS_Free_AI_Video_Studio.ipynb)

This notebook makes AI video clips for free on Google Colab's free T4 GPU. It uses an open-source model and needs no paid APIs, tokens or subscriptions.

| | |
|---|---|
| **Model** | [Wan 2.2 TI2V-5B](https://github.com/Wan-Video/Wan2.2) (Apache-2.0, commercial use allowed) |
| **Engine** | [ComfyUI](https://github.com/comfyanonymous/ComfyUI) v0.45.4, run headless inside the notebook (no web UI or tunnels) |
| **Modes** | Text → video, image → video, continue the last clip |
| **Formats** | 16:9 (1280×704) and 9:16 (704×1280), 24 fps, 1–5 s per clip |
| **Finishing** | FFmpeg joins clips (cut or crossfade) and adds music, `.srt` captions and a logo, then exports a 1080p MP4 (upscaled) |

## How to use

1. Click **Open in Colab** above.
2. Go to **Runtime ▸ Change runtime type ▸ T4 GPU**.
3. Run cells ① → ④: GPU check, install, ~17 GB model download, start the engine. This takes about 4 minutes.
4. Fill in the form in cell ⑤ and run it. Each run makes one clip.
5. Use ⑥ to download clips, and ⑦ to edit and export the final video.

## Measured on a free Colab T4 (16 Nov 2026)

- Setup (① → ④) takes about 4 minutes. The model download runs at 130–175 MB/s.
- A 3-second 1280×704 clip at 20 steps takes about 17 minutes end to end (~37 s per step).
- Free GPU time is rationed by Google, and the limits aren't published. If you see "Cannot connect to GPU backend … usage limits", try again later.

## Licences

- Wan 2.2 model weights: Apache-2.0
- ComfyUI: GPL-3.0. It is downloaded at run time, not redistributed here.
- Use only music, logos, faces and brand assets you have the rights to.
