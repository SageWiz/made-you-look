# Made You Look

A deep dive into the UX and UI that grabs people's attention. Each experiment rebuilds one effect, then asks whether it's worth shipping.

Live at https://hellasage.com/made-you-look/

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | The series index |
| `head-tracked-window/` | 01, the screen as a window you look through |
| `assets/site.css` | Styles shared by every page |

Plain HTML, CSS and JS. No build step. GitHub Pages serves the `main` branch as is.

## Adding an experiment

1. Copy `head-tracked-window/` to a new folder and rename it. The folder name is the URL.
2. Build the page. Keep the experiment's script inside its own `index.html`.
3. In the root `index.html`, update that experiment's row (status, link).
4. Fill in "What it costs" with things you measured, and give it a verdict.

## Running it locally

Camera and tilt need a secure page, so open it through a local server, not as a file:

    python3 -m http.server 8000

Then visit http://localhost:8000/
