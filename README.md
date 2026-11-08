# robertgeraldsenasin.github.io

Portfolio site for Robert Gerald Senasin (RGS): software, applied AI and games.

Plain HTML, CSS and a little JavaScript in one `index.html`. No build step, no framework. The fonts (Anton, Barlow, DM Serif Display) are self-hosted, so the site makes no outside requests.

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | The whole site. Views are switched by the URL hash (`#work`, `#minerva`, `#text-to-sql`, `#hasik`, `#about`, `#credentials`, `#resume`, `#contact`) |
| `assets/fonts/` | The three typefaces, latin subset, WOFF2 |
| `assets/` | Event photos and certificates (WebP), plus `og.png`, the link-preview image |
| `resumes/` | The four resume PDFs linked from the Resume page |
| `.github/workflows/pages.yml` | Deploys the site on every push to `main` |

## Deploy

1. Create a public repo named exactly `robertgeraldsenasin.github.io`.
2. Push these files to the `main` branch.
3. In the repo's Settings, open Pages and set the source to **GitHub Actions**.
4. The site goes live at https://robertgeraldsenasin.github.io after the workflow finishes.

## Updating

- The "Right now" block on the home view and the footer date are the two places that go stale. Update both together.
- **Hasik goes public:** in the Hasik view, change "Not public yet" to "Public" and paste in the commented-out button row right below the facts box.
- **Shipping a planned project (Byahe, Bantay):** copy the Hasik view's structure into a new `<article class="view" data-view="...">`, add its name to `VIEWS`, `TITLES` and `NAV_FOR` in the script, link it from the Work list, and on the Work page's lane map change its dot from `planned` to a link.
- New resume versions: replace the PDFs in `resumes/` and keep the same filenames.

## Motion

Besides the hero letters and the page sweep, these graphics play once, when they scroll into view:

- Section title tabs slide in, and their gold block drops behind them.
- Featured cases wipe in one after another, and each stamp lands.
- Case pages: the award burst spins in, pipeline steps slide in one by one, charts grow, result numbers count up, and the Text-to-SQL repair loop runs five turns before stamping "0 of 48" on Pass.
- The Work page's lane map draws its three circles, then places each project.

To add motion to a new element, give it `data-anim` and style its start state under `.motion` and its end state under `.motion ... .in`. People with "reduce motion" turned on see the finished state with no animation.
