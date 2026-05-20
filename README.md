# Ty K. Beats — Redesigned site

A unified four-page redesign sharing one stylesheet. All image paths are relative — drop these files into your `TyKBeats_Website` folder alongside the existing `images/` directory and everything will resolve.

## File structure

```
TyKBeats_Website/
├── index.html       (Home)
├── albums.html      (Albums — Broken Promises)
├── singles.html     (Singles — Whisper, One Day, Renegade, Free Man)
├── featured.html    (Featured — latest video + past release)
├── styles.css       (Shared design system — edit once, applies everywhere)
└── images/          (your existing folder, unchanged)
    ├── logo.jpg
    ├── tyson_photo.jpg
    ├── bp_album_cover.jpg
    ├── whisper_cover.jpeg
    ├── one_day_cover.jpg
    ├── renegade_cover.jpg
    ├── free_man_cover.jpg
    ├── youtube_icon.png
    └── soundcloud_icon.png
```

## What to drop in

Copy the four `.html` files and `styles.css` into your project root. Leave your existing `images/` folder where it is. The redesigned pages don't use `logo.jpg`, `youtube_icon.png`, or `soundcloud_icon.png` (replaced with inline SVG for sharpness at any size), but those files don't need to be removed — they just stop being referenced.

## Things you'll want to update

These are placeholder values I chose because I didn't have the real ones:

- **Track durations** in `albums.html` (3:24, 3:12, etc.) — swap in your actual run times
- **Album year** (2025) and **total runtime** (34 min) in the albums hero
- **Single release years** (all set to 2025) in `singles.html`
- **SoundCloud track URLs** — every track-row and single-card currently links to the artist profile (`soundcloud.com/tykbeats`). Once you have individual track URLs, replace the `href` on each link
- **SoundCloud album set URL** — the embed under each hero points to your profile. If "Broken Promises" exists as a SoundCloud set, swap in that set URL for a more focused player
- **Spotify / Apple Music links** — currently `#` placeholders with "Coming soon" labels. Update when you publish there

## Things to know about the design

- The site is dark by default — designed for late-night listening, which suits the lo-fi/emotional register
- Typography is Fraunces (display serif) + DM Sans (body), loaded from Google Fonts. No system fonts
- Single accent color (`#e08259`, sunset coral) — defined as `--accent` in `styles.css` if you ever want to shift the brand color
- The film grain and warm vignette are CSS-only (no extra image files)
- Fully responsive — collapses to single column at 900px, hides nav on small screens (replace with a hamburger if you want)
- Respects `prefers-reduced-motion` — animations disable for users who've set that preference

## Deploying

Same as before — drag the whole folder into your Netlify project, or push to your git repo if you have one connected. No build step required, it's all static HTML/CSS.
