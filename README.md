# Runable Videos landing-page prototype

Copy variant of https://github.com/xendezzz/runable-websites-hero-prototype at `339109858c91a749105f44d81ebe49002eb3a647`.

The original layout, typography, section order, responsive rules and motion are retained. Copy is tailored to video generation. The hero uses five supplied videos and extracted still frames. Other showcase artwork and demo clips remain grey placeholders with the original media dimensions. Brand marks, icons and fonts are retained. Usage metrics are unverified placeholders (—); pricing is inherited from the source and should be confirmed before launch.

## Preview

```sh
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000. No build step or dependency installation is required.

## Integration

This remains a marketing prototype. Generation, authentication, checkout and downloads are not connected. The source keeps a separate, unwired `hero-builder.js` integration helper. Its legacy event and selector IDs are retained for compatibility; the landing page CTAs remain prototype controls. The demo player is disabled until media is supplied. Replace media files under `dist/assets`, restore video sources and remove `dist/placeholders.css` when real assets are ready.

The original hosting project ID and canonical URL are deliberately omitted so this repository cannot overwrite the source site. Configure a separate deployment when ready.

## Feature copy source

The 5 feature cards under “Total control, remarkably simple” use the headings and descriptions from https://runable.com/videos. Updated September 25, 2026; grey media placeholders and the existing card presentation are retained.

## Hero videos

Five supplied clips rotate in the center card. Each is retimed to exactly 6 seconds (180 frames at 30 fps), muted, and optimized to at most 1280 pixels wide. Side cards show two distinct frames from that same original clip. Prompts and the dithered gradient change with each clip. Playback pauses offscreen, in background tabs, and via the video button; reduced-motion preferences disable autoplay.

| Scene | Original file | Original duration | Playback speed | Side-frame timestamps |
| --- | --- | --- | --- | --- |
| Product | final_combined_10s.mp4 | 10.02 s | 1.67× | 1.5 s / 8.1 s |
| Fashion | final_walk_showcase_v2.mp4 | 24.25 s | 4.04× | 11.8 s / 20.5 s |
| Animation | pixar animation.mp4 | 29.79 s | 4.97× | 4.5 s / 24 s |
| Motion control | side_by_side_16x9.mp4 | 9.87 s | 1.64× | 2 s / 7 s |
| UGC | video-9i9aucebe6.mp4 | 15.09 s | 2.52× | 1.6 s / 12 s |

Media lives in `dist/assets/hero-videos`; scene prompts and colors are configured in `dist/index.html`. Original source videos are unchanged.
