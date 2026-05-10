# CSEC & CAPE Mathematics — brochure site

A single-page brochure site built with [Astro](https://astro.build) for advertising
CSEC and CAPE Mathematics tutoring services. No payments, no accounts — just a
clean, professional page that introduces you and tells visitors how to contact you.

## Sections

- **Hero** — name, tagline, CTA
- **About** — bio and teaching highlights
- **Subjects** — CSEC Math, CSEC Add Math, CAPE Pure Math, CAPE Applied Math
- **Credentials** — qualifications and experience
- **My Approach** — 3-step teaching method
- **Testimonials** — student/parent quotes
- **FAQ** — common parent/student questions
- **Contact** — WhatsApp, email, phone links + availability schedule

## Personalising the Site

All placeholder content is in **one place**: the `tutor` object at the top of
`src/pages/index.astro`. Update each value before publishing:

```js
const tutor = {
  name:           'Adrian Mungroo',
  tagline:        'PhD candidate, Mechanical Engineering · Georgia Tech',
  location:       'Atlanta, GA · online (Caribbean)',
  whatsapp:       '+1 (868) 000-0000',
  email:          'yourname@email.com',
  phone:          '+1 (868) 000-0000',
  experience:     '[X]',
};
```

After updating those values, search the file for any remaining `[PLACEHOLDER]`
comments (there are several inside the bio, credentials, FAQ, and testimonials
sections) and replace them with your real content.

## Running Locally

```sh
npm install      # first time only
npm run dev      # dev server at http://localhost:4321
npm run build    # production build → dist/
npm run preview  # preview the production build
```

## Deployment

The site is fully static. Deploy the `dist/` folder to any static host:

- [Netlify](https://www.netlify.com) — drag and drop `dist/`, free tier is fine
- [Vercel](https://vercel.com) — connect the repo, set build command to `npm run build`
- [Cloudflare Pages](https://pages.cloudflare.com) — same approach as Vercel
- Shared hosting — upload `dist/` via FTP

## Tech Stack

- [Astro](https://astro.build) 5.x — static site generator
- Plain CSS (no framework) in `src/styles/global.css`
- No JavaScript frameworks — vanilla JS only for mobile nav and FAQ accordion
- Google Fonts — Inter (loaded from CDN)
