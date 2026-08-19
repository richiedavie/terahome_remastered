# Terahome Landing Page Project Context

## What We Are Building

Terahome is a fictional Indonesian home internet provider.

This repository is for a single professional landing page.

The goal is to transform the existing Terahome visual concept into a clean, production-quality Astro website.

This is a design and frontend implementation project.

It is not currently a full customer-management platform.

---

## Primary Stack

Use:

- Astro
- TypeScript
- Tailwind CSS

Astro should control the page structure and rendering.

Use interactive JavaScript only where necessary.

Do not introduce React, Svelte, Vue, or another frontend framework unless explicitly requested.

---

## Current Landing Page Structure

The page should remain a single page with these sections:

```text
Home
│
├── Hero
│
├── Benefits / Quick Stats
│
├── Paket Internet
│
├── Keunggulan
│
├── Tentang Kami
│
├── Kontak
│
└── Footer
```

Navigation:

```text
Home          → #hero
Paket Internet → #paket
Keunggulan    → #keunggulan
Tentang Kami  → #tentang
Kontak        → #kontak
```

---

## Required File Structure

```text
src/
├── components/
│   ├── Navbar.astro
│   ├── Hero.astro
│   ├── Benefits.astro
│   ├── Pricing.astro
│   ├── PricingCard.astro
│   ├── Advantages.astro
│   ├── About.astro
│   ├── Contact.astro
│   └── Footer.astro
│
├── layouts/
│   └── Layout.astro
│
├── styles/
│   └── global.css
│
└── pages/
    └── index.astro
```

Do not expand this architecture unnecessarily.

---

## Design Direction

The design must be:

- Professional
- Clean
- Modern
- Trustworthy
- Minimal
- Telecommunications-oriented

Do not imitate a flashy startup landing page.

Do not use excessive visual effects.

Do not use excessive animation.

Do not use glassmorphism as a default styling method.

---

## Gradient Restriction

This is extremely important:

**Do not use mixed-color gradients.**

No:

- Green-to-blue gradients
- Blue-to-purple gradients
- Purple-to-pink gradients
- Rainbow gradients
- Gradient text
- Neon gradients
- Multi-color glowing backgrounds

Use solid colors and controlled contrast.

The website should have a flat professional visual language.

Use subtle shadows, borders, spacing, and surface colors to create hierarchy.

---

## Brand Colors

```text
Primary Navy     #24384D
Secondary Green  #4D795F
Secondary Blue   #3E5F86
Dark Green       #315C48
Light Green      #75A56A
Accent Yellow    #D9A33A
Off White        #F4F3EC
White            #FFFFFF
Dark Text        #17212B
```

Navy and green should dominate.

Yellow/orange is only a supporting promotional accent.

---

## Typography

Use:

```text
Headings → Hanken Grotesk
Body     → Work Sans
```

Keep typography restrained and readable.

---

## Package Information

Use the following package information:

```text
5 Mbps   → Rp 155.000 / bulan
10 Mbps  → Rp 195.000 / bulan
20 Mbps  → Rp 220.000 / bulan
30 Mbps  → Rp 250.000 / bulan
50 Mbps  → Rp 350.000 / bulan
100 Mbps → Rp 400.000 / bulan
```

All packages communicate:

- Kecepatan Stabil
- Koneksi Unlimited

100 Mbps is the highlighted package:

`Paling Populer`

---

## Contact Information

Use the following fictional contact details:

```text
WhatsApp: +62 838-2543-0327
Website: terahome.id
Support: 24/7 Support
```

Do not invent additional real company information.

---

## Visual Philosophy

The flyer/source material is an inspiration for:

- Brand colors
- House + Wi-Fi identity
- Internet package concept
- Green and navy visual language
- Free-installation/promotion concept

However, the website should not look like a printed flyer.

Convert the information into a spacious web layout.

Use whitespace.

Use clear section separation.

Use consistent card proportions.

Use modern responsive layout.

---

## Implementation Philosophy

Build the page as reusable components.

`index.astro` should mostly compose the page.

Target composition:

```astro
<Layout>
  <Navbar />

  <main>
    <Hero />
    <Benefits />
    <Pricing />
    <Advantages />
    <About />
    <Contact />
  </main>

  <Footer />
</Layout>
```

Do not put every section into one massive `index.astro` file.

---

## Important

Do not overengineer the project.

This is a landing page.

No database is currently required.

No real backend is currently required.

A simulated form interaction is acceptable.

Focus on:

1. Visual fidelity
2. Responsive layout
3. Clean Astro architecture
4. Accessibility
5. Performance
6. Professional appearance

When making implementation decisions, prioritize the landing page experience above architectural complexity.

The final product should look like a polished ISP website that could realistically be deployed publicly.