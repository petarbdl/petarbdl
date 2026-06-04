# Personal Portfolio — Petar Badaloski

Senior Qt/C++ Engineer · Skopje, North Macedonia

This is the source of my personal portfolio page, hosted via GitHub Pages.

## Folder structure

```
.
├── index.html
├── README.md
└── images/
    ├── xylem/
    │   └── all/                  # 23-shot gallery behind the "All screenshots" toggle
    ├── relimetrics/
    │   └── all/                  # 36-shot gallery behind the "All screenshots" toggle
    └── cms-aero/
        └── cabin-control.png
```

## Image filenames (must match exactly)

The `index.html` looks for these specific files. Either name your screenshots to match, or edit the `<img src="...">` paths in `index.html`.

| Project       | Path                                       |
|---------------|--------------------------------------------|
| Xylem         | `images/xylem/all/` (23-image gallery behind the "All screenshots" toggle) |
| Relimetrics   | `images/relimetrics/all/` (36-image gallery behind the "All screenshots" toggle) |
| CMS AERO      | `images/cms-aero/cabin-control.png`        |

## Recommended image specs

- **Width:** ~1600px (will scale down responsively)
- **Aspect ratio:** roughly 16:10 (the slot is 16:10; other ratios get cropped via `object-fit: cover`)
- **Format:** PNG for screenshots with text, JPG for photos
- **File size:** keep under 500KB each — compress with tinypng.com or squoosh.app

## Fallback behavior

If an image is missing or fails to load, the page automatically falls back to the placeholder grid — the page never looks broken, even mid-upload. Once you upload an image with the correct filename, it replaces the placeholder on the next page refresh.

## Adding additional screenshots per project

Each project currently has one screenshot. To add more, duplicate the `<div class="project-screenshot">` block inside the same `<article class="project">`:

```html
<div class="project-screenshot">
    <img src="images/xylem/measurement-ui.png" alt="..." onerror="this.style.display='none'">
    <div class="placeholder">...</div>
</div>

<div class="project-screenshot">
    <img src="images/xylem/calibration-view.png" alt="..." onerror="this.style.display='none'">
    <div class="placeholder">...</div>
</div>
```

## Updating the site

GitHub Pages rebuilds automatically. After committing a change, allow ~30–60 seconds, then refresh.

## Updating contact links

In the "Get in touch" section near the bottom of `index.html`, replace the `#` placeholders with your real LinkedIn and GitHub URLs.
