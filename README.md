# DLSJBC Website — Redesigned Front-End

A from-scratch HTML/CSS/JS rebuild of dlsjbc.edu.ph's public pages (Home, Admissions,
About, Contact, Articles) with a new visual identity: forest green + Lasallian gold on a
warm parchment background, plus hover/scroll animations and an accordion, filterable
articles grid, and animated nav.

## Folder structure

```
dlsjbc-site/
├── index.html          Home
├── admissions.html      Admissions (requirements + enrollment steps accordion)
├── about.html            About (history timeline)
├── contact.html          Contact (form + info cards)
├── articles.html          Articles (search + filter)
├── css/
│   └── style.css        Design system, layout, animations
├── js/
│   └── main.js           Nav toggle, scroll reveal, accordion, form, filters
└── images/                All image assets
```

## About the images — please read

My sandbox can't reach `static.wixstatic.com` (the CDN hosting the real school photos and
logo), so I couldn't download the actual site images. Instead I generated **placeholder
graphics** in the same color palette, at the same filenames and roughly the same
dimensions the real assets would use, so the layout is fully "drop-in ready":

| File | Used for | Replace with |
|---|---|---|
| `images/logo.png` | Header + footer logo | The real DLSJBC seal/logo |
| `images/logo-small.png` | Favicon | Small square version of the logo |
| `images/icon-facebook.png` | Facebook icon | Keep or swap for your own icon |
| `images/hero-banner.jpg` | (available if you want a homepage hero photo) | A wide campus photo |
| `images/about-portrait.jpg` | About page portrait image | A tall building/campus photo |
| `images/admissions-banner.jpg` | (available for admissions banner) | Buildings & facilities photo |
| `images/contact-banner.jpg` | Contact page side image | Buildings & facilities photo |
| `images/news-*.jpg` (4 files) | Home + Articles news thumbnails | The 4 real news photos |

**To swap them in:** just save the real photos from the live site (right-click → Save
Image As) using the **same filenames** listed above, and drop them into `images/`,
overwriting the placeholders. No HTML/CSS changes needed.

## Notes

- All copy on About/Admissions was rewritten in my own words rather than copied verbatim
  from the original site, per standard copyright practice — feel free to refine the tone.
- The contact form is front-end only right now (shows a "Thanks for submitting!" message
  on submit) — wire it up to PHP/mail or an API endpoint whenever you're ready, similar to
  the backend pattern you're using for CVC Hire.
- Everything is vanilla HTML/CSS/JS, no build step — just open `index.html` in a browser,
  or serve the folder with XAMPP/any static server.
- Fonts (Fraunces, Manrope, Space Mono) load from Google Fonts via `<link>` tags in each
  page's `<head>` — swap for local font files if you need it to work offline.
