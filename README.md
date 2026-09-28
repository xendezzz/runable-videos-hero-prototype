# Runable Videos landing-page prototype

Copy variant of https://github.com/xendezzz/runable-websites-hero-prototype at `339109858c91a749105f44d81ebe49002eb3a647`.

The original layout, typography, section order, responsive rules and motion are retained. Copy is tailored to video generation. The hero uses five supplied videos and extracted still frames. Other showcase artwork and demo clips remain grey placeholders with the original media dimensions. Brand marks, icons and fonts are retained. Usage metrics are sample placeholders (25,000+ creators and teams, 150,000+ videos, 120+ countries); pricing is inherited from the source and should be confirmed before launch.

## Preview

```sh
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000. No build step or dependency installation is required.

## Integration

This remains a marketing prototype. Generation, authentication, checkout and downloads are not connected. The source keeps a separate, unwired `hero-builder.js` integration helper. Its legacy event and selector IDs are retained for compatibility; the landing page CTAs remain prototype controls. The tutorial player uses the supplied AI Video Making Tutorial with its original audio and duration. Replace media files under `dist/assets`, restore video sources and remove `dist/placeholders.css` when real assets are ready.

The original hosting project ID and canonical URL are deliberately omitted so this repository cannot overwrite the source site. Configure a separate deployment when ready.

## Feature copy source

The 5 feature cards under “Total control, remarkably simple” use the headings and descriptions from https://runable.com/videos. Updated September 25, 2026; grey media placeholders and the existing card presentation are retained.

## Hero videos

Five supplied clips rotate in the center card. Each is retimed to exactly 10 seconds (300 frames at 30 fps), muted, and optimized to at most 1280 pixels wide. Side cards show two distinct frames from that same original clip. Prompts and the dithered gradient change with each clip. Playback pauses offscreen, in background tabs; reduced-motion preferences disable autoplay.

| Scene | Original file | Original duration | Playback speed | Side-frame timestamps |
| --- | --- | --- | --- | --- |
| Product | final_combined_10s.mp4 | 10.02 s | 1.00× | 1.5 s / 8.1 s |
| Fashion | final_walk_showcase_v2.mp4 | 24.25 s | 2.43× | 9 s / 20.5 s |
| Animation | pixar animation.mp4 | 29.79 s | 2.98× | 4.5 s / 24 s |
| Motion control | side_by_side_16x9.mp4 | 9.87 s | 0.99× | 2 s / 7 s |
| UGC | video-9i9aucebe6.mp4 | 15.09 s | 1.51× | 1.6 s / 12 s |

Media lives in `dist/assets/hero-videos`; scene prompts and colors are configured in `dist/index.html`. Original source videos are unchanged.

## Starting-point showcase

The five category previews use the supplied Product ads, Brand stories, Explainers, Social clips, and 3D animation clips in `dist/assets/showcase-videos`. Original clip durations are preserved. Desktop and mobile previews loop silently while selected and visible, pause in background tabs, and show extracted posters when reduced motion is enabled.

## Feature card videos

The five cards under Total control use the supplied eight-second Text to Video, Image to Video, Video Remix, Multi-Model, and AI Audio clips in `dist/assets/feature-videos`. Original dimensions and duration are preserved. Only the selected visible card plays, muted and looping. Inactive cards and background tabs pause; reduced-motion users see a still poster.
