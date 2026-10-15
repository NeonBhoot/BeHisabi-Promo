# BeHisabi Promo

HTML animation scenes for the BeHisabi Android app promo video. Each scene is a
self-contained HTML file rendered at a perfect 9:16 frame, timed to the
voiceover SRT.

## Scenes

| File | Voiceover | Status |
| ---- | --------- | ------ |
| `seg1-calendar-9x16.html` | ১ তারিখে বেতন এলো, আর ১৫ তারিখেই পকেট ফাঁকা। টাকাগুলো গেল কই? | Done |

## Preview

Open any scene file directly in a mobile browser. No build step, no dependencies
(apart from Google Fonts in some scenes).

## Rendering to video

Capture frames with headless Chromium at 30fps, then encode:

```bash
ffmpeg -framerate 30 -i frame_%04d.png -c:v libx264 -pix_fmt yuv420p out.mp4
```
