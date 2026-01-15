# AI Agent Instructions for AstroWind Template

This file provides guidance for AI coding agents customizing the AstroWind template.

## Quick Start

1. **Site Configuration**: Edit `src/config.yaml` for site name, description, and metadata
2. **Navigation**: Edit `src/navigation.ts` for header/footer links
3. **Homepage**: Edit `src/pages/index.astro` for main content
4. **Blog**: Add/edit posts in `src/data/post/` directory

---

## Files to MODIFY (Customize These)

### Core Configuration
| File | Purpose |
|------|---------|
| `src/config.yaml` | Site name, description, SEO metadata, social links |
| `src/navigation.ts` | Header navigation, footer links, social icons |

### Main Pages
| File | Purpose |
|------|---------|
| `src/pages/index.astro` | Homepage - hero, features, CTA sections |
| `src/pages/about.astro` | About page - team, values, stats |
| `src/pages/services.astro` | Services/features page |
| `src/pages/pricing.astro` | Pricing plans |
| `src/pages/contact.astro` | Contact form and info |
| `src/pages/terms.md` | Terms of service |
| `src/pages/privacy.md` | Privacy policy |

### Blog Posts
| Location | Purpose |
|----------|---------|
| `src/data/post/*.md` | Blog posts (Markdown) |
| `src/data/post/*.mdx` | Blog posts with components (MDX) |

### Branding
| File | Purpose |
|------|---------|
| `src/components/Logo.astro` | Site logo |
| `src/components/CustomStyles.astro` | Custom fonts and colors |
| `src/components/widgets/Announcement.astro` | Top banner announcement |

---

## Files to KEEP (Don't Modify Unless Necessary)

These are reusable components and utilities - modifying them may break the site:

```
src/components/widgets/     # Reusable page sections (Hero, Features, etc.)
src/components/ui/          # UI primitives (Button, Card, etc.)
src/components/common/      # Shared components
src/components/blog/        # Blog-specific components
src/layouts/               # Page layouts
src/utils/                 # Utility functions
src/content/config.ts      # Content collection schema
```

---

## Files You Can DELETE (Demo Content)

These are demo pages that most sites don't need:

```
src/pages/homes/           # Alternative homepage demos (saas, startup, mobile-app, personal)
src/pages/landing/         # Landing page demos (lead-generation, sales, click-through, etc.)
```

Also consider replacing the demo blog posts in `src/data/post/` with real content.

---

## Valid Tabler Icons

**CRITICAL**: Only use icons from this verified list. Invalid icons cause build failures.

### Safe Icons (Use These)
```
Navigation:  tabler:home, tabler:menu, tabler:arrow-right, tabler:chevron-down
Actions:     tabler:download, tabler:upload, tabler:search, tabler:check, tabler:x
Social:      tabler:brand-github, tabler:brand-twitter, tabler:brand-x, tabler:brand-facebook
Content:     tabler:file, tabler:folder, tabler:image, tabler:mail, tabler:phone
Status:      tabler:alert-circle, tabler:info-circle, tabler:check-circle
Objects:     tabler:sun, tabler:moon, tabler:star, tabler:rocket, tabler:bulb
             tabler:user, tabler:users, tabler:building, tabler:calendar
             tabler:code, tabler:terminal, tabler:database, tabler:server
             tabler:tool, tabler:bolt, tabler:shield, tabler:lock
Layout:      tabler:layout-grid, tabler:template, tabler:components, tabler:list-check
```

### Icons to AVOID (Will Break Build)
```
tabler:layers          -> Use tabler:layout-grid
tabler:vacuum-cleaner  -> Not in icon set
tabler:tools           -> Use tabler:tool
```

### Verify Before Deploying
Always run `npm run build` after changing icons to catch errors.

---

## config.yaml Structure

```yaml
site:
  name: 'Your Site Name'                    # CHANGE THIS
  site: 'https://your-domain.com'           # CHANGE THIS
  base: '/'
  trailingSlash: false
  googleSiteVerificationId: false

metadata:
  title:
    default: 'Your Site Title'              # CHANGE THIS
    template: '%s - Your Site'              # CHANGE THIS
  description: 'Your site description'      # CHANGE THIS
  robots:
    index: true
    follow: true
  openGraph:
    site_name: 'Your Site'                  # CHANGE THIS
    type: website
  twitter:
    handle: '@your_handle'                  # CHANGE THIS
    site: '@your_handle'                    # CHANGE THIS
    cardType: summary_large_image

apps:
  blog:
    isEnabled: true
    postsPerPage: 6
```

---

## Common Customization Tasks

### 1. Change Site Name and Branding
```bash
# Edit these files:
src/config.yaml          # Site name, description, social handles
src/navigation.ts        # Update footer copyright, social links
src/components/Logo.astro # Update logo text/image
```

### 2. Update Homepage Content
```bash
# Edit src/pages/index.astro
# Key sections to update:
# - Hero: Main headline, tagline, CTA buttons
# - Features: Feature cards with icons and descriptions
# - Content: Image + text sections
# - Stats: Numbers and metrics
# - FAQs: Frequently asked questions
# - CallToAction: Final CTA section
```

### 3. Replace Blog Posts
```bash
# Delete demo posts:
rm src/data/post/astrowind-template-in-depth.mdx
rm src/data/post/get-started-website-with-astro-tailwind-css.md
# ... etc

# Create new posts with frontmatter:
# ---
# publishDate: 2024-01-15T00:00:00Z
# title: 'Your Post Title'
# excerpt: 'Brief description'
# image: '~/assets/images/your-image.png'
# tags: [tag1, tag2]
# ---
# Your content here...
```

### 4. Update Legal Pages
```bash
# Edit these files and replace placeholder company name:
src/pages/terms.md
src/pages/privacy.md
```

---

## Build and Test

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production (catches icon errors!)
npm run build

# Preview production build
npm run preview
```

---

## Deployment Notes

This template is optimized for static deployment. Output goes to `dist/` folder.

For Astro sites, you do NOT need `_redirects` file - Astro generates static HTML pages.

Remember to update `src/config.yaml` with your actual deployed URL before final deployment.
