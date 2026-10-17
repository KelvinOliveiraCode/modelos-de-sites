# Website Templates · 20 showcase landing pages, one per niche

![HTML5](https://img.shields.io/badge/HTML5-e34f26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572b6?style=flat-square&logo=css3&logoColor=white)

Showcase of 20 landing pages, one per business niche. Each template is a single HTML file, no build, no npm, no framework: open in the browser and see how the client's website looks before ordering your own.

## Problem / Why it exists

The business owner needs to see what they will receive before paying for a website. A gray wireframe does not show that. This showcase brings together 20 ready-made templates by niche — medical clinic, gym, law firm, fashion, online courses, real estate, aesthetics, SaaS technology, restaurant, pet shop, finance, children's education, wedding, dentistry, digital marketing, solar energy, insurance, travel, civil construction, and cryptocurrencies — so the client can choose the one most similar to their business and order their own in the same standard. Texts, prices, and images are placeholders for each client's real data.

## What it does

The hub (index.html) is the only index: there are no links between landings. It gathers the 20 models in a grid filterable by segment and text search. Each card shows the niche name, a line of what the model does, and the color palette used. Clicking opens the niche landing: a complete self-contained page with navigation, niche-specific sections, form validation, and real interactions (tabbed menu, financing simulator, solar energy calculator, scheduling, etc.), plus a link back to the hub. All pages open directly in the browser, with no installation.

## Stack

- HTML5 — semantics, visible focus, keyboard navigation, prefers-reduced-motion
- CSS3 — CSS variables, grid, flexbox, transform and opacity animations, mobile-first responsiveness
- JavaScript — IntersectionObserver for scroll reveal, filters and search in the hub, form validation, and per-niche interactions
- No external dependencies besides Google Fonts

## How it works

The visitor filters by segment, searches by term, chooses a model, and opens the file `<slug>/index.html`. Each landing is a single file with inline CSS and JS. The menu works on mobile, the form validates fields and shows a success state without sending anything anywhere, and all models respect WCAG AA contrast and motion reduction.

## How to run

There is no build. Open `index.html` in the browser, or serve the folder with any static server:

```
python -m http.server
npx serve .
```

To open a specific model, navigate to its folder, for example `restaurante-delivery/index.html`.

## Project structure

```
index.html           hub: segment filter, search, 20 model cards, process, contact
<slug>/index.html    complete self-contained landing of a niche (20 folders)
spec/nichos.md       dossier of the 20 models: colors, fonts, sections, and animation of each niche
spec/regras-landing.md execution rules valid for all landings (accessibility, mobile, animation, prohibited)
spec/revisao-layout.md layout review
spec/revisao-visual.md visual review
DESIGN.md            hub design direction and landing contract
.nojekyll            direct publishing on GitHub Pages
```

## Trade-offs and decisions

- One landing per niche, each one a single file. Advantage: the client opens and sees the real result in the browser without installing anything. Cost: CSS repetition between pages; no global change propagates by itself.
- Inline CSS and JS. No build, no npm, no framework — zero tool dependency. The only external link is Google Fonts.
- No links between landings; the hub is the only index. The client enters through the hub, chooses the niche, and returns. Simplifies navigation, but requires returning via the browser back button or the return link on each landing.
- The niche color appears only as a band on the hub card, never as a hub interface color, avoiding a rainbow effect of 20 palettes.
- Texts, prices, images, and testimonials are explicit placeholders (`Your Brand`, `[LOGO]`, `[real testimonial]`). Never present invented data as real.

## Known limitations

- No backend: forms do not send anything; they only show a success state on screen.
- The hub search searches the model name and segment; there is no search for content inside landings.
- Each model loads Google Fonts; without internet connection, the page uses the system fallback font.
- All content is in Brazilian Portuguese; there is no English version.
- Not a website ready to publish as is: it is a demonstration showcase with placeholder data.

## License

Distributed under the MIT license. See the repository's license file for details.

## Author

Kelvin Oliveira

- GitHub: https://github.com/KelvinOliveiraCode
- LinkedIn: https://www.linkedin.com/in/kelvin-oliveira-code/
- Portfolio: https://kelvinoliveiracode.github.io/portfolio/
- WhatsApp: (91) 98613-4599
