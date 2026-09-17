# Sipho's Plumbing & Maintenance — Website Project

## Student Information
- **Module:** Web Development (Introduction) — WEDE5020
- **Student Name:** Mokolobetsi Johannes Mangena
- **Student Number:** [insert student number]

## Project Overview
Sipho's Plumbing & Maintenance is a sole-proprietor plumbing business operating in
Johannesburg since 2016, offering residential and small-commercial plumbing, geyser
repairs, and general maintenance. This project builds a professional website for the
business to replace its current reliance on a Facebook page and word-of-mouth referrals.

The site is being built in three parts:
- **Part 1 — Building the Foundation:** planning, content research, HTML structure
- **Part 2 — Designing the Visuals:** CSS styling and responsive design
- **Part 3 — Adding Functionality and SEO:** JavaScript, forms, SEO, deployment

## Website Goals and Objectives
1. Generate qualified enquiry leads (quote requests) directly from the website.
2. Build trust and credibility ahead of a phone call or site visit.
3. Improve local search visibility for "plumber near me"-type searches.

**KPIs:** quote-form submissions per month, phone-click conversions, local search
ranking for target keywords.

## Key Features and Functionality
- Homepage with hero banner and service overview
- About Us page with company history, mission, vision and team
- Services page detailing plumbing, geyser, and maintenance offerings
- Enquiry page with a quote-request form
- Contact page with two service locations, a map, and a general contact form

## Timeline and Milestones
| Phase | Weeks | Focus |
|---|---|---|
| Part 1 | 1 – 4 | Planning, content gathering, HTML structure |
| Part 2 | 5 – 8 | CSS styling and responsive design |
| Part 3 | 9 – 12 | JavaScript functionality, forms, SEO, deployment |

## Part 1 Details

### File and Folder Structure
```
sipho-plumbing/
├── index.html
├── about.html
├── services.html
├── enquiry.html
├── contact.html
├── css/
│   └── style.css        (placeholder — styled in Part 2)
├── js/
│   └── script.js         (placeholder — built out in Part 3)
├── images/               (original SVG graphics: logo, hero, icons, avatar)
├── screenshots/           (Part 2 responsive testing evidence)
└── README.md
```

### Sitemap
```
Home (index.html)
├── About Us (about.html)
├── Services (services.html)
│   ├── Plumbing Repairs (#plumbing)
│   ├── Geyser Services (#geysers)
│   └── General Maintenance (#maintenance)
├── Get a Quote (enquiry.html)
└── Contact (contact.html)
```
All five pages share a common header (logo, navigation, "Call Now" button) and
footer (contact details, secondary navigation), as required by the module brief.

### Changelog
| Date | Change |
|---|---|
| 2026-08-14 | Initial project structure and Part 1 HTML pages created (index, about, services, enquiry, contact) |
| 2026-08-14 | Placeholder css/style.css and js/script.js added ahead of Parts 2 & 3 |
| 2026-08-14 | README.md created with project overview, sitemap and references |
| 2026-08-17 | Added original SVG images (logo, hero illustration, service icons, team avatar) and embedded Google Map on contact.html |
| 2026-08-17 | Part 2: replaced placeholder stylesheet with full CSS — base styles, typography scale, Grid/Flexbox layout, colour/shadow/pseudo-class styling, and responsive breakpoints (tablet ≤900px, mobile ≤600px) |
| 2026-08-17 | Part 2: captured desktop/tablet/mobile screenshots of all five pages as responsive-testing evidence |
| 2026-09-14 | Replaced the SVG icon + text logo with a supplied logo graphic (`images/logo-full.png`) in the header on all five pages; added responsive sizing rules for the new logo |
| 2026-09-16 | Part 2: increased `.logo-img` size so the logo's tagline is legible; screenshots regenerated |
| 2026-09-16 | Part 2: recoloured the entire site to a blue/white/black palette (updated CSS custom properties; "Call Now" button changed to black with blue hover state) |
| 2026-09-16 | Part 2: replaced the abstract hero illustration and added real, freely-licensed plumbing photographs (Pexels) to the homepage hero, a new "Our Work" gallery, each services.html section, and the about.html history section — see References for credits |
| 2026-09-16 | Part 2: added further content — "How It Works" process steps and "Where We Work" service-area list (index.html); "Our Values" and "Qualifications & Compliance" (about.html); response-time notes and an FAQ section (services.html); "What Happens Next" steps (enquiry.html); opening-hours table (contact.html) |
| 2026-09-16 | Part 2: regenerated desktop/tablet/mobile screenshots for all five pages to reflect the new palette, photos and content |

## Part 2 Details

### CSS Styling Approach
- **External stylesheet:** `css/style.css`, linked from every page.
- **Base style:** CSS reset (`* { margin:0; padding:0; box-sizing:border-box }`), CSS
  custom properties (`:root`) for the colour scheme, typography scale and shadows so
  values are defined once and reused everywhere.
- **Colour scheme:** blue, white and black, matching the brand logo — navy (`--color-navy`)
  for headings and primary buttons, a mid-blue (`--color-blue`) for links and accents,
  and black (`--color-black`) for the "Call Now" button, the header's top border, and
  the FAQ/service checkmarks, giving the CTA the strongest visual weight on the page.
- **Typography:** system sans-serif stack, a 1.25 modular type scale (`--fs-sm` through
  `--fs-xxl`), consistent `line-height` and `letter-spacing` on headings.
- **Layout:** CSS Grid for the services overview, "How It Works" steps, the "Our Work"
  photo gallery, "Our Values" cards, and the contact-page locations; Flexbox for the
  header/nav, hero, service-detail rows, and buttons; both used to keep selector count
  low by relying on the cascade rather than styling every element individually.
- **Visual styling:** colour, background-color, border, and box-shadow on cards, photo
  frames and buttons; `:hover`, `:focus`, and `:active` pseudo-classes on all links,
  buttons and form fields (including a visible focus ring for keyboard accessibility).
- **Responsive design:** two breakpoints — tablet (`≤900px`) and mobile (`≤600px`).
  The 3-column grids (services, "How It Works", "Our Work" gallery) become 2 columns
  on tablet and 1 on mobile; the 2-column contact/locations grid becomes 1 column on
  tablet; the header stacks and the "Call Now" button becomes a full-width sticky bar
  on mobile, per the original proposal's UX requirement. Spacing and font sizes use
  `rem`/`em` units throughout so the whole layout scales with the user's browser font
  settings.
- **Images:** the logo, hero-icon set and team avatar are original SVGs (vector,
  resolution-independent). The homepage hero, "Our Work" gallery, services.html
  section photos, and the about.html history photo are real, freely-licensed
  photographs hotlinked from Pexels (see References) — chosen because a plumbing
  business's own before/after job photos aren't available for a coursework project.
  All images are capped with `max-width: 100%`, and photo containers use a fixed CSS
  `height` with `object-fit: cover` so the layout doesn't shift while images load.

### Responsive Testing Evidence
Screenshots of every page at desktop (1280px), tablet (800px) and mobile (390px)
widths are in the `screenshots/` folder, e.g. `index_desktop.png`,
`index_tablet.png`, `index_mobile.png` (and the same pattern for about, services,
enquiry and contact).


## References
- Google Search Central. *SEO starter guide.* Available at: https://developers.google.com/search [Accessed 2026].
- GitHub Docs. *GitHub Pages.* Available at: https://docs.github.com/pages [Accessed 2026].
- Nielsen Norman Group. *Mobile UX for local service websites.* Available at: https://www.nngroup.com [Accessed 2026].
- MDN Web Docs. *HTML: A good basis for accessibility.* Available at: https://developer.mozilla.org [Accessed 2026].
- Logo (`images/logo-full.png`): AI-generated image (Google Gemini), supplied by the student. Requires an AI-disclosure entry (in-text citation, full reference, and screengrab annexe) per the module's AI usage guidelines, as it was not hand-drawn or photographed by the student.
- Karakaya, A. (2021) *Plumber Installs Pipe Fittings* [Photograph]. Pexels. Available at: https://www.pexels.com/photo/plumber-installs-pipe-fittings-6419128/ [Accessed 2026]. Used on index.html (hero) and services.html (Plumbing Repairs).
- AR Abnoy (2024) *Close-up of Man Using a Spanner* [Photograph]. Pexels. Available at: https://www.pexels.com/photo/close-up-of-man-using-a-spanner-16509869/ [Accessed 2026]. Used on index.html ("Our Work") and services.html (Plumbing Repairs).
- sejio402 (2024) *Professional Plumber Installing a Radiator Pipe* [Photograph]. Pexels. Available at: https://www.pexels.com/photo/professional-plumber-installing-a-radiator-pipe-29226620/ [Accessed 2026]. Used on index.html ("Our Work") and services.html (Geyser Services).
- Danilyuk, P. (2021) *Steel Pipes with Pressure Gauge* [Photograph]. Pexels. Available at: https://www.pexels.com/photo/steel-pipes-with-pressure-gauge-7937300/ [Accessed 2026]. Used on index.html ("Our Work") and services.html (General Maintenance).
- Ruth, H. (2021) *Plumber Repairing Power Source* [Photograph]. Pexels. Available at: https://www.pexels.com/photo/plumber-repairing-power-source-7859953/ [Accessed 2026]. Used on about.html (Our History).
- Pexels (2026) *License.* Available at: https://www.pexels.com/license/ [Accessed 2026]. All photographs above are used under the Pexels License (free for commercial and personal use, no attribution legally required; credited here regardless as good academic practice, and to satisfy the module's "cite the source of images" requirement).
