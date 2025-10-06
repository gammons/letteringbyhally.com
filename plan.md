You are to design and implement a complete static website for Lettering by Hally — a modern, romantic calligraphy studio.
Your goal is to produce a fast, elegant, production-ready static site that highlights Hally’s artistry and converts visitors into leads.

The user will provide nine portfolio images (p1.jpg–p9.jpg) to include.

## Project Overview

Business name: Lettering by Hally
Mission: Elegant, hand-crafted calligraphy for weddings, events, and keepsakes.
Aesthetic: Modern, airy, romantic, timeless — similar to Lettering by Hally.
Primary goal: Drive inquiries for wedding and event calligraphy services.
Secondary goals: Display portfolio, establish trust, and capture leads.

## Technical Requirements

- Framework: Astro
- No CMS; content lives in /content/ as YAML/JSON
- Include README.md with setup and deploy steps (Netlify or Vercel)
- Lighthouse scores ≥95 for Performance and Accessibility
- CSS budget <100 KB, mobile-first, semantic HTML5, WCAG AA contrast
- Images served as WebP/AVIF via <picture>, lazy-loaded, and responsive
- Provide sitemap.xml and robots.txt
- Add Plausible or GA4 analytics

## Visual Design System

### Palette

| Role | Hex |
|------|-----|
| Ink Black | #1A1A1A |
| Warm White | #FAF9F7 |
| Soft Blush | #F2E9E4 |
| Sage Grey | #C8CEC7 |
| Gold Accent | #BDA06A |

### Typography

- **Headlines**: Playfair Display or Fraunces
- **Body**: Inter or Source Sans 3
- **Optional accent**: SVG signature wordmark

### Layout & Mood

- Max width 1160 px, generous white space
- Light, natural photography, shallow depth of field
- Subtle animations (fade 50–100 ms)
- Feels calm, premium, trustworthy

### Portfolio Assets

Include 9 images: `images/p1.jpg–p9.jpg`

Use across the site:

- **Home**: 3–4 featured images in carousel
- **Portfolio**: all 9 images in masonry or 3-column grid
- Each image opens in a lightbox with title, category, caption, and materials

## Sitemap & Pages

### Home

- Hero: headline, subcopy, CTA "Request a Quote", secondary "View Portfolio"
- Services overview (Weddings, Day-Of, Commissions)
- Featured portfolio carousel (p1–p4)
- Process (Discovery → Design → Delivery)
- Testimonials slider
- Contact mini-form

### Services

- Invitation Calligraphy (from $800)
- Envelope Addressing (from $2.50 per envelope)
- Day-Of Signage & Place Cards (from $150)
- Custom Commissions & Gifts (from $95)
- On-Site Brand Events (day rate)

CTA "Request a Quote"

### Portfolio

Grid showing all 9 images with category filters and lightbox captions.

### Pricing

Transparent price ranges and sample bundles ($1.5k / $2k / $3k).

- Include rush-fee and timeline notes.
- CTA "Share Your Details".

### About

Photo + short story about Hally and her values (craftsmanship, communication, reliability).

CTA "Say Hello".

### FAQ

~12 FAQs (timelines, materials, rush, shipping, deposits, care).

### Contact

Full inquiry form: name, email, phone, event date, venue, services, quantities, inspiration URL, message.

- Integrate with Formspree or Netlify Forms; add confirmation page.

### Optional

- **Workshops** – sessions + waitlist
- **Shop** – Etsy integration
- **Privacy / Terms**

## Copy Guidelines

**Tone**: Warm, confident, approachable, professional.

**Highlight**: clarity, timelines, and artistry.

### Hero Example

> Modern calligraphy for weddings & meaningful moments.
>
> Hand-crafted invitations, envelopes, and day-of details — thoughtfully designed and delivered on time.
>
> [Request a Quote]

### Service Blurbs

- **Invitation Calligraphy** — "Set the tone from the very first envelope."
- **Envelope Addressing** — "Consistent, legible, and beautiful — at scale."
- **Day-Of Signage** — "Place cards, menus, and seating charts that bring the room together."
- **Commissions** — "Keepsake quotes and heirloom gifts, written by hand."

### Process

Every project begins with your story. We confirm details, explore materials, provide proofs, and deliver carefully packaged finished work.

### Trust Microcopy

Clear communication, careful packaging, and reliable timelines.

## Content Files

### /content/services.yml

```yaml
- id: invitations
  name: Wedding Invitation Calligraphy
  starts_at: 800
  includes:
    - Headers & names
    - Spot calligraphy
    - Two proof rounds

- id: envelopes
  name: Envelope Addressing
  starts_at_each: 2.5

- id: dayof
  name: Day-Of Signage & Place Cards
  starts_at: 150

- id: commissions
  name: Custom Commissions & Gifts
  starts_at: 95
```

### /content/faq.yml

```yaml
- q: How far in advance should I book?
  a: For weddings, 6–12 weeks notice ensures availability.

- q: Do you ship nationwide?
  a: Yes, via insured USPS Priority and UPS.

- q: Do you accept rush projects?
  a: Often possible with a 20–40% rush fee.
```

## SEO & Metadata

- Meta title + description per page
- OG/Twitter images in `/public/og/`
- JSON-LD LocalBusiness schema

**Natural keywords**: wedding calligraphy, envelope addressing, day-of signage, custom calligraphy, Philadelphia calligrapher (adjust location)

## Components

- Header (transparent → solid)
- Buttons: primary, outline, text
- Card component for services
- Testimonial slider
- Steps timeline with icons
- Portfolio grid + filters + lightbox
- Multi-step quote form
- Footer with Instagram feed + email signup

## Deliverables

- Full static-site repo with pages and assets
- `/content` directory with example data
- `README.md` for setup, content editing, and deployment
- OG images and favicons
- "Getting Started" checklist for owner (update email, replace text, confirm forms)

## Stretch Features

- Multi-step "Estimate Builder" on Pricing
- Print-friendly project brief from form submission
- Light / Dark mode toggle

## Footer Example

> © Lettering by Hally — Modern calligraphy for weddings, events, and keepsakes. Based in [City, State].
