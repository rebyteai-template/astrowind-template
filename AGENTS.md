# AstroWind Template

A production-ready website template built with Astro 5.0 and Tailwind CSS. The most starred & forked Astro theme.

## Tech Stack

- **Framework**: Astro 5.x with SSG/SSR support
- **Styling**: Tailwind CSS
- **Language**: TypeScript
- **Content**: MDX for blog posts
- **Icons**: Astro Icon with Tabler icons

## Features

- Production-ready PageSpeed Insights scores
- Dark mode with system preference detection
- RTL (Right-to-Left) support
- Built-in blog with categories, tags, and RSS feed
- Image optimization with Astro Assets and Unpic
- Automatic sitemap generation
- Open Graph metadata for social sharing
- Google Analytics integration ready
- Multiple landing page variants (SaaS, Startup, Mobile App, Personal)

## Project Structure

```
src/
├── assets/        # Images, styles, favicons
├── components/    # Reusable UI components
├── content/       # Blog posts (MDX/Markdown)
├── layouts/       # Page layouts
├── pages/         # Route pages
└── utils/         # Helper functions
```

## Available Skills

| Skill | Description |
|-------|-------------|
| `build-and-deploy` | Build and deploy this Astro website to Vercel or Netlify |

## Development

```bash
npm install
npm run dev
```

## Configuration

Edit `src/config.yaml` to customize site settings, navigation, and metadata.

## Page Variants

- `/` - Main landing page
- `/homes/saas` - SaaS product page
- `/homes/startup` - Startup landing page
- `/homes/mobile-app` - Mobile app showcase
- `/homes/personal` - Personal portfolio
- `/landing/*` - Various landing page templates
