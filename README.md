# Lettering by Hally

A modern, elegant static website for Lettering by Hally — a calligraphy studio specializing in wedding invitations, envelope addressing, and event stationery.

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd letteringbyhally.com
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser to `http://localhost:4321`

## 📁 Project Structure

```
/
├── public/
│   ├── images/          # Portfolio images (p1.jpg - p9.jpg)
│   ├── og/              # Open Graph images for social sharing
│   ├── favicon.svg      # Site favicon
│   └── robots.txt       # SEO robots file
├── src/
│   ├── components/      # Reusable Astro components
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── Button.astro
│   │   ├── Card.astro
│   │   ├── TestimonialSlider.astro
│   │   └── PortfolioGrid.astro
│   ├── layouts/         # Page layouts
│   │   └── BaseLayout.astro
│   ├── pages/           # Site pages (auto-routed)
│   │   ├── index.astro       # Home page
│   │   ├── services.astro    # Services page
│   │   ├── portfolio.astro   # Portfolio gallery
│   │   ├── pricing.astro     # Pricing & packages
│   │   ├── about.astro       # About page
│   │   ├── faq.astro         # FAQ page
│   │   ├── contact.astro     # Contact form
│   │   └── thank-you.astro   # Form confirmation
│   └── styles/          # Global styles
│       └── global.css
├── content/             # Content as YAML files
│   ├── services.yml     # Services data
│   ├── faq.yml          # FAQ items
│   ├── testimonials.yml # Client testimonials
│   └── portfolio.yml    # Portfolio items
├── astro.config.mjs     # Astro configuration
├── package.json
└── tsconfig.json
```

## ✏️ Editing Content

All content is managed through YAML files in the `/content` directory. This makes it easy to update without touching code.

### Services (`content/services.yml`)

Add or modify services:

```yaml
- id: service-id
  name: Service Name
  description: Brief description
  starts_at: 800           # Starting price
  # OR
  starts_at_each: 2.5     # Per-item price
  includes:
    - Feature 1
    - Feature 2
```

### Portfolio (`content/portfolio.yml`)

Add portfolio items:

```yaml
- id: p10
  image: /images/p10.jpg
  title: Project Title
  category: invitations    # invitations, envelopes, dayof, commissions, events
  materials: Description of materials
  description: Project description
```

### FAQ (`content/faq.yml`)

Add FAQ items:

```yaml
- q: Question here?
  a: Answer here.
```

### Testimonials (`content/testimonials.yml`)

Add testimonials:

```yaml
- author: Client Name
  text: Testimonial text
  role: Wedding Clients
```

## 🖼️ Adding Images

1. Place images in `/public/images/`
2. Reference them in content files as `/images/filename.jpg`
3. For best performance:
   - Use WebP or AVIF format when possible
   - Optimize images before uploading
   - Recommended max width: 2000px

## 🎨 Customizing Styles

### Color Palette

Edit colors in `/src/styles/global.css`:

```css
:root {
  --color-ink-black: #1A1A1A;
  --color-warm-white: #FAF9F7;
  --color-soft-blush: #F2E9E4;
  --color-sage-grey: #C8CEC7;
  --color-gold-accent: #BDA06A;
}
```

### Typography

Current fonts (loaded from Google Fonts):
- **Display**: Playfair Display
- **Body**: Inter

To change fonts, update the Google Fonts link in `/src/layouts/BaseLayout.astro` and the CSS variables in `/src/styles/global.css`.

## 📧 Contact Form Setup

The contact form is configured for **Netlify Forms**. If deploying to Netlify:

1. Forms will work automatically (no additional setup needed)
2. Access form submissions in Netlify dashboard under "Forms"
3. Configure email notifications in Netlify settings

### Using a Different Form Service

To use Formspree or another service:

1. Open `/src/pages/contact.astro`
2. Replace the form attributes:

```astro
<form
  action="https://formspree.io/f/YOUR_FORM_ID"
  method="POST"
>
```

## 🚀 Deployment

### Deploy to Netlify

1. Push your code to GitHub
2. Log in to [Netlify](https://netlify.com)
3. Click "Add new site" → "Import an existing project"
4. Connect to your GitHub repository
5. Build settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Click "Deploy"

Your site will be live at a Netlify URL (e.g., `yoursite.netlify.app`). Add a custom domain in Netlify settings.

### Deploy to Vercel

1. Push your code to GitHub
2. Log in to [Vercel](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Vercel auto-detects Astro settings
6. Click "Deploy"

### Deploy to Other Platforms

Build the static site:

```bash
npm run build
```

Upload the `dist/` folder to any static hosting service (Cloudflare Pages, GitHub Pages, etc.).

## 🔍 SEO & Analytics

### SEO

- **Sitemap**: Automatically generated at `/sitemap-index.xml`
- **Robots.txt**: Located at `/public/robots.txt`
- **Meta tags**: Configured per-page in BaseLayout
- **JSON-LD Schema**: Included for LocalBusiness

Update the site URL in `astro.config.mjs`:

```js
export default defineConfig({
  site: 'https://yourdomain.com',
  // ...
});
```

### Analytics

The site is configured for **Plausible Analytics**. To use:

1. Sign up at [plausible.io](https://plausible.io)
2. Add your domain
3. Update the script in `/src/layouts/BaseLayout.astro`:

```astro
<script defer data-domain="yourdomain.com" src="https://plausible.io/js/script.js"></script>
```

To use **Google Analytics** instead:

```astro
<!-- Replace Plausible script with: -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 📝 Commands

| Command | Action |
|---------|--------|
| `npm install` | Install dependencies |
| `npm run dev` | Start dev server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview build locally before deploying |
| `npm run astro` | Run Astro CLI commands |

## ✅ Pre-Launch Checklist

- [ ] Update all content in `/content` YAML files
- [ ] Replace placeholder portfolio images
- [ ] Update contact email address
- [ ] Configure form submission service
- [ ] Add custom domain
- [ ] Update analytics tracking code
- [ ] Replace OG image in `/public/og/default.jpg` (1200x630px)
- [ ] Update site URL in `astro.config.mjs`
- [ ] Test contact form submission
- [ ] Run Lighthouse audit (target: 95+ performance & accessibility)
- [ ] Test on mobile devices

## 🎯 Performance

This site is optimized for:
- **Lighthouse Performance**: 95+
- **Lighthouse Accessibility**: 95+
- **CSS Budget**: <100 KB
- **Mobile-first design**
- **Fast loading with lazy-loaded images**
- **Semantic HTML5**
- **WCAG AA contrast compliance**

## 🆘 Support

For issues or questions:
- Check [Astro documentation](https://docs.astro.build)
- Review this README
- Check `/content` YAML files for data structure

## 📄 License

© Lettering by Hally. All rights reserved.
