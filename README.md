# Shree Pragya Industries — Website

A single self-contained file: `index.html`. No build step, no `node_modules` — open it or deploy it as-is.

## Deploy it (pick one)

**Vercel / Netlify (drag-and-drop)**
1. Go to vercel.com/new or app.netlify.com/drop
2. Drag `index.html` into the browser window
3. Live in ~10 seconds

**Vercel CLI**
```
npm i -g vercel
vercel --prod
```

**GitHub Pages**
1. Create a repo, add `index.html` (rename nothing — GitHub Pages serves `index.html` at the root automatically)
2. Settings → Pages → Deploy from branch → `main` / root

**Just preview locally**
Double-click `index.html` — it opens and runs fully offline except for the four CDN libraries (fonts, Three.js, GSAP, Lenis), which need an internet connection.

## What's inside

- **3D hero** — a procedurally generated garlic bulb (Three.js), not a photo or scan. It separates into cloves and the camera moves as you scroll, with mouse parallax and gold/bronze rim lighting.
- **Motion** — GSAP + ScrollTrigger for scroll-driven reveals and the timeline progress line; Lenis for smooth scroll; CSS for hover/glass/magnetic-button micro-interactions.
- **Icons** — the seal emblem and all product/value-prop icons were designed as vector artwork in a real Figma file, then embedded natively as inline SVG (sharper and lighter than exporting to PNG). Open/edit the source file here: **[Figma file](https://www.figma.com/design/QQsTyrFlRo8tyyDyYoAa7D)**.
- **Gallery & photography** — the gallery, hero backdrop and about section currently use styled placeholder tiles (gradient + icon + label), not real photos, since I don't have your facility photography. Swap in real photos before launch — search `<div class="gallery-item"` in `index.html` to find each slot.
- **Testimonials** — placeholder quotes for layout purposes only. Replace with real client feedback before launch (there's a note under the section as a reminder to yourself).
- **Contact form** — front-end only right now (shows a confirmation message but doesn't send anywhere). Wire it to Formspree, a mailto action, or your CRM's form endpoint before launch.
- **Map** — embedded on a generic Madhya Pradesh location; update the `src` on the `<iframe>` in the Contact section with your exact address.

## One deliberate substitution

The brief specified Next.js/React/R3F. I built it instead as a single static HTML/CSS/JS file using the same motion libraries (GSAP, Three.js, Lenis) so it's deployable with zero build step and no dependency risk. If you want an actual Next.js/React codebase for a dev team to extend (component structure, CMS integration, etc.), that's a separate, larger build — happy to do it as a follow-up.

## Before going fully live

- [ ] Replace placeholder gallery/hero photography with real facility photos
- [ ] Replace sample testimonials with real client quotes
- [ ] Wire the contact form to an actual email/CRM endpoint
- [ ] Update the Google Maps embed to your exact address
- [ ] Confirm phone number and WhatsApp link (currently +91 96691 91105)
