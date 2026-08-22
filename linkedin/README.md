# GK LinkedIn banner

A cohort banner for Guanghua–Kellogg EMBA students to use as their LinkedIn
cover image, built to match the Kellogg–WHU banner other cohorts use.

| file | use |
| --- | --- |
| `gk-linkedin-banner-1584x396.png` | LinkedIn's own recommended size — upload this one |
| `gk-linkedin-banner-1399x349.png` | same 4:1 crop at the WHU example's exact size |
| `banner.html` | the source; edit and re-render to change text or photos |

## Regenerating

Rendered at 2× through headless Chrome, then downsampled — that keeps the type
crisp at both output sizes.

```
chrome --headless=new --disable-gpu --hide-scrollbars \
       --window-size=3168,792 --screenshot=_raw2x.png banner.html
```

then resize `_raw2x.png` to 1584×396 and 1399×349 with LANCZOS.

## Design notes

The Kellogg–WHU banner was sampled before rebuilding it: its field is a
**vertical** gradient, essentially constant across the width, held at L 32–36 /
S 43–63. This one keeps that construction and swaps the hues to GK — Guanghua
crimson at the top, Kellogg purple at the bottom — so the lavender accent, which
sits low in the frame, lands on purple and stays legible.

Left slab is the Kellogg Global Hub in Evanston; the right slab is reserved for
a Guanghua / PKU campus photo, mirroring how the WHU banner pairs one campus
from each school.
