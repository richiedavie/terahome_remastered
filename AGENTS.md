# Terahome Landing Page Development Guidelines

## Project Purpose

This repository contains a single-page marketing website for **Terahome**, a fictional Indonesian home internet service provider.

The primary goal is to build a polished, production-quality **landing page**, not a full SaaS application, dashboard, customer portal, or complex full-stack system.

The website should communicate:

- Fast and stable home internet
- Simple and transparent internet packages
- Reliable customer support
- Professional telecommunications branding
- A trustworthy and modern digital experience

The design should feel like a legitimate ISP website that could realistically be shown to customers.

The project is intentionally limited in scope.

Do not introduce unnecessary backend architecture, authentication systems, database systems, CMS infrastructure, admin dashboards, payment systems, or other features that are not required for the landing page.

---

## Primary Technology

Use:

- Astro
- TypeScript
- Tailwind CSS
- Astro components
- Minimal client-side JavaScript only when interaction actually requires it

Astro is the primary framework and should remain the architectural foundation of the project.

Prefer Astro components for static and presentational sections.

Do not convert the entire website into React, Svelte, Vue, or another client-rendered application.

Interactive components may use a small amount of client-side JavaScript when appropriate, but avoid unnecessary JavaScript.

The website is primarily a content-driven marketing page and should remain lightweight.

---

## Project Scope

This project is a **single landing page**.

The primary route is:

`/`

The page should contain the following sections:

1. Home / Hero
2. Benefits / Quick Stats
3. Paket Internet
4. Keunggulan
5. Tentang Kami
6. Kontak
7. Footer

These sections should exist on the same page.

Do not create separate routes for:

- `/paket`
- `/keunggulan`
- `/tentang`
- `/kontak`

unless explicitly requested later.

The navbar should use anchor navigation to the corresponding sections.

---

## Required Navigation

The main navigation must contain:

- Home
- Paket Internet
- Keunggulan
- Tentang Kami
- Kontak

Navigation targets:

- Home → `#hero`
- Paket Internet → `#paket`
- Keunggulan → `#keunggulan`
- Tentang Kami → `#tentang`
- Kontak → `#kontak`

The primary navbar CTA:

`Berlangganan`

should lead to the package or contact area rather than an external page.

Use smooth scrolling behavior for section navigation.

Do not create fake navigation items that point nowhere.

---

## Required File Structure

Maintain this project structure:

```text
terahome-rework/
├── .vscode/
│   ├── extensions.json
│   └── launch.json
│
├── public/
│   ├── favicon.ico
│   ├── favicon.svg
│   └── images/
│       └── router/
│
├── src/
│   ├── components/
│   │   ├── Navbar.astro
│   │   ├── Hero.astro
│   │   ├── Benefits.astro
│   │   ├── Pricing.astro
│   │   ├── PricingCard.astro
│   │   ├── Advantages.astro
│   │   ├── About.astro
│   │   ├── Contact.astro
│   │   └── Footer.astro
│   │
│   ├── layouts/
│   │   └── Layout.astro
│   │
│   ├── styles/
│   │   └── global.css
│   │
│   └── pages/
│       └── index.astro
│
├── astro.config.mjs
├── package.json
├── package-lock.json
├── tsconfig.json
├── AGENTS.md
├── CLAUDE.md
└── README.md
```

Do not create additional directories unless there is a concrete implementation requirement.

Do not create backend folders, API folders, database folders, authentication folders, or server architecture for this landing page unless explicitly requested.

---

## Component Responsibilities

### Navbar.astro

Responsible only for the top navigation.

Contains:

- Terahome logo/brand
- Home
- Paket Internet
- Keunggulan
- Tentang Kami
- Kontak
- Berlangganan CTA

The navbar should remain clean and responsive.

Desktop navigation should remain horizontal.

Mobile navigation should collapse into an appropriate mobile menu.

Do not make the navbar visually excessive.

---

### Hero.astro

The hero is the primary introduction.

Use:

Headline:

`Internet Cepat.`
`Hidup Tanpa Batas.`

Supporting copy:

`Internet rumah cepat, stabil, dan terpercaya untuk kebutuhan sehari-hari. Nikmati koneksi tanpa hambatan bersama Terahome.`

Primary CTA:

`Lihat Paket Internet`

Secondary CTA:

`Hubungi Kami`

Trust indicators:

- Cepat & Stabil
- Unlimited
- Support 24/7

The right-side visual should represent a home internet/router concept using a clean and minimal visual language.

Do not overload the hero with decorative effects.

---

### Benefits.astro

This is the compact benefits / quick-stat section immediately below the hero.

Required benefits:

- Kecepatan Stabil
- Unlimited
- Coverage Luas
- Support 24/7

Use simple icons.

This section should be concise and visually lighter than the hero.

---

### Pricing.astro

Responsible for the full internet package section.

Heading:

`Pilih Paket Internet Terbaik Untuk Anda`

Supporting copy:

`Temukan paket internet yang sesuai dengan kebutuhan rumah Anda.`

Required packages:

| Speed | Price |
|---|---:|
| 5 Mbps | Rp 155k / bln |
| 10 Mbps | Rp 195k / bln |
| 20 Mbps | Rp 220k / bln |
| 30 Mbps | Rp 250k / bln |
| 50 Mbps | Rp 350k / bln |
| 100 Mbps | Rp 400k / bln |

Every package includes:

- Kecepatan Stabil
- Koneksi Unlimited
- Berlangganan CTA

The 100 Mbps package should be highlighted as:

`Paling Populer`

Do not make the highlight excessively flashy.

---

### PricingCard.astro

This should be a reusable component.

Do not manually duplicate six completely separate card implementations when a reusable component can render all package variants.

Accept package-specific data through Astro props.

The component should support:

- Name
- Speed
- Price
- Popular state
- CTA state

Cards should remain visually consistent.

---

### Advantages.astro

Required heading:

`Keunggulan Terahome`

Required features:

### Gaming & Streaming

`Nikmati pengalaman bermain game dan streaming video tanpa lag.`

### Low Latency

`Ping rendah untuk respons yang cepat dalam setiap aktivitas online.`

### Coverage Luas

`Jangkauan sinyal yang kuat dan luas ke seluruh area rumah Anda.`

### Support 24/7

`Tim bantuan siap melayani Anda kapan saja dibutuhkan.`

Use simple, consistent icons.

Do not use giant decorative illustrations.

---

### About.astro

Required heading:

`Terhubung Lebih Baik Bersama Terahome`

Supporting idea:

Terahome provides home internet services intended to support everyday digital activities for families.

Value statements:

- Stabil
- Terjangkau
- Terpercaya

Supporting metrics:

- 100% → Fokus Kualitas
- 24/7 → Support

Keep claims believable and avoid inventing unsupported corporate statistics.

Do not invent real-world company history, customer counts, certifications, coverage percentages, or awards.

Terahome is a fictional project.

---

### Contact.astro

Required heading:

`Butuh Bantuan?`

Supporting copy should encourage visitors to contact Terahome for package and service information.

Contact information currently represented in the source design:

WhatsApp:

`+62 838-2543-0327`

Website:

`terahome.id`

Support:

`24/7 Support`

Contact form fields:

- Nama
- WhatsApp
- Pilih Paket
- Pesan

Button:

`Kirim Pesan`

The form is a simulated/demo interaction.

Do not build a real customer database.

Do not implement real payment processing.

Do not imply that form submissions are being permanently stored.

If form interaction is implemented, it may show a local or simulated success state.

---

### Footer.astro

Keep the footer dark and professional.

Include:

- Terahome branding
- Company links
- Service links
- Legal links
- Copyright

Relevant navigation links should point to the actual landing-page sections.

Avoid dead links wherever possible.

---

## Visual Design Rules

The visual identity must remain professional, restrained, and telecommunications-oriented.

The website should look modern without becoming futuristic or gimmicky.

### Absolutely no mixed gradients

Do not use:

- Multicolor gradients
- Rainbow gradients
- Purple-to-blue gradients
- Green-to-blue gradients
- Orange-to-purple gradients
- Neon gradient backgrounds
- Gradient text
- Excessive glow effects

Do not use gradients simply because a section looks empty.

Use solid surfaces instead.

If depth is needed, achieve it through:

- Solid color contrast
- Borders
- Subtle shadows
- Whitespace
- Typography hierarchy
- Spacing
- Card elevation

A very subtle single-tone visual treatment may be acceptable if it is explicitly necessary, but the default should be **flat solid colors**.

The original landing-page concept is intentionally professional and should not resemble a generic AI-generated SaaS template.

---

## Color System

Use the existing Terahome visual language.

Primary Navy:

`#24384D`

Secondary Green:

`#4D795F`

Secondary Blue:

`#3E5F86`

Dark Green:

`#315C48`

Light Green:

`#75A56A`

Warm Promotional Accent:

`#D9A33A`

Off White:

`#F4F3EC`

White:

`#FFFFFF`

Dark Text:

`#17212B`

Use navy and green as the dominant brand colors.

Use yellow/orange only as a small promotional accent.

Do not introduce unrelated colors without a strong reason.

Do not gradually shift between brand colors through gradients.

---

## Typography

The existing source design uses:

- Hanken Grotesk for headings
- Work Sans for body and labels

Preserve this pairing where practical.

Headings should be:

- Strong
- Clean
- Modern
- Easy to scan

Body text should be:

- Readable
- Neutral
- Compact
- Professional

Do not use novelty fonts.

Do not use oversized typography merely to create visual drama.

---

## Layout

Use a consistent centered content container.

Desktop maximum width:

`1280px`

Maintain a consistent horizontal gutter.

Existing design tokens suggest:

- 8px base unit
- 16px small stack spacing
- 24px gutter
- 32px large stack spacing
- 80px section spacing
- 40px desktop margins
- 16px mobile margins

Maintain consistent spacing rather than improvising spacing values randomly throughout components.

Major sections should have generous whitespace.

---

## Cards

Cards should use:

- Solid backgrounds
- White or light surfaces
- Subtle border
- Small to moderate radius
- Very subtle shadow
- Clear internal spacing

Avoid:

- Heavy glassmorphism
- Neon borders
- Giant shadows
- Gradient backgrounds
- Excessive blur

Cards should feel like components from one coherent design system.

---

## Buttons

Primary buttons:

- Terahome green
- White text
- Medium rounded corners
- Clear hover state

Secondary buttons:

- Navy outline or neutral outline
- Clear contrast
- Clean hover state

Buttons should not look oversized.

Do not introduce animated gradient buttons.

Do not make every button visually identical in importance.

---

## Icons

Use a consistent icon style.

Material Symbols may be used because the original source design already uses them.

Keep icon sizing and stroke/weight visually consistent.

Do not mix many unrelated icon libraries without a reason.

---

## Responsive Behavior

The page must work well on:

- Desktop
- Tablet
- Mobile

Desktop:

- Hero uses a balanced two-column layout
- Pricing uses a multi-column grid
- Advantages use four columns when width permits
- Contact uses a two-column layout

Mobile:

- Hero stacks vertically
- Pricing cards stack naturally
- Advantages become a single or two-column layout depending on available width
- About section stacks vertically
- Contact section stacks vertically
- Navigation becomes mobile-friendly
- Buttons remain accessible and readable
- No horizontal overflow

Do not simply shrink the desktop design.

Recompose sections where necessary.

---

## Accessibility

Use semantic HTML.

Use:

- `nav`
- `main`
- `section`
- `footer`
- `header`
- appropriate heading levels

Every meaningful form input must have a label.

Interactive elements must be keyboard accessible.

Maintain sufficient text contrast.

Do not use color alone to communicate essential information.

Decorative images should use appropriate empty alt text when needed.

---

## SEO

The landing page should include:

- Appropriate `<title>`
- Meta description
- Viewport metadata
- Semantic heading structure
- Relevant Open Graph metadata where practical

The page title should remain related to Terahome and home internet.

Do not stuff keywords unnaturally.

---

## Code Quality

Prefer:

- Small focused components
- Reusable components
- Typed props
- Semantic markup
- Clear naming
- Minimal duplication
- Minimal client-side JavaScript

Avoid:

- Giant monolithic `index.astro`
- Repeating the same markup unnecessarily
- Inline styles everywhere
- Unused dependencies
- Arbitrary libraries
- Premature abstractions

The code should be understandable to a developer learning Astro.

---

## Important Source-of-Truth Rule

The provided HTML structure is the source reference for this project's content and section organization.

The current page structure contains:

- Navbar
- Hero
- Benefits / Quick Stats
- Paket Internet
- Keunggulan
- Tentang Kami
- Kontak
- Footer

Preserve the intended content and navigation relationships when converting it into Astro components.

Do not silently replace the existing content with unrelated copy.

Improve implementation quality and component organization, but do not change the project's core business concept.

---

## Scope Control

This project is a landing page.

Do not implement:

- Database
- Authentication
- Admin panel
- User dashboard
- Payment gateway
- Subscription billing
- CMS
- Customer account system
- Real CRM integration
- Complex backend
- Websocket infrastructure
- Unnecessary API architecture

A simulated contact/subscription interaction is acceptable.

Keep the project simple until a real requirement demands more complexity.

---

## Final Quality Standard

The final website should feel like a professional ISP landing page rather than:

- A student demo
- A generic template
- A flashy AI-generated page
- A brochure pasted directly into a browser
- A dashboard disguised as a landing page

The design should communicate:

**Stable. Professional. Modern. Trustworthy.**

When uncertain between a more decorative implementation and a cleaner implementation, choose the cleaner implementation.