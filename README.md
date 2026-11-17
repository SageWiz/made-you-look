# Made You Look

A deep dive into the UX and UI that grabs people's attention. Each experiment rebuilds one effect, then asks whether it's worth shipping.

Live at https://hellasage.com/made-you-look/

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | The series index |
| `head-tracked-window/` | 01, the screen as a window you look through |
| `scroll-through-places/` | 02, scrolling pushes you through a chain of places |
| `portrait-reveal/` | 03, a portrait drawn in characters with a drag-to-reveal handle |
| `search-builds-the-page/` | 04, a search box that assembles the page from your question |
| `assets/site.css` | Styles shared by every page |

Plain HTML, CSS and JS. No build step. GitHub Pages serves the `main` branch as is.

## Adding an experiment

1. Copy one of the experiment folders and rename it. The folder name is the URL.
2. Build the page. Keep the experiment's script inside its own `index.html`.
3. In the root `index.html`, add a row for it under "Also up".
4. Fill in "What it costs" with things you measured, and give it a verdict.

## Running it locally

Camera and tilt need a secure page, so open it through a local server, not as a file:

    python3 -m http.server 8000

Then visit http://localhost:8000/

## Things you'll want to edit

- **02 photos.** Each stop in `scroll-through-places/index.html` is one picture with a wide file and a tall file (`room-1-wide.webp`, `room-1-tall.webp`, and so on). Replace those files with your photos, fill in the `alt`, and rewrite the caption. The comment above the section has the details.
- **03 photo.** Replace `portrait-reveal/portrait.jpg` with any square photo and update the `alt` text on the `<img>`.
- **04 facts.** Everything the search box knows is the `TOPICS` list at the top of the script in `search-builds-the-page/index.html`.
- **Verdicts and measurements.** Each page has a "What it costs" table and a "Would I ship it?" section waiting for real numbers.
