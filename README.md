# Commerce On Tap - Website

Professional website for Commerce On Tap, a Shopify consulting and e-commerce solutions business.

## Tech Stack

- **Framework:** Eleventy (11ty) - Static site generator
- **Templating:** Nunjucks
- **Styling:** CSS (no frameworks)
- **Hosting:** Cloudflare Pages
- **Domain:** commerceontap.com

## Local Development

### Prerequisites

- Node.js (v16 or higher)
- npm

### Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

### Development Commands

- **Start dev server:** `npm run dev`
  - Opens local server at http://localhost:8080
  - Watches for changes and auto-reloads

- **Build site:** `npm run build`
  - Generates production-ready files in `_site/` directory

## Project Structure

```
commerceontap-site/
├── src/
│   ├── index.njk           # Home page
│   ├── services.njk        # Services page
│   ├── contact.njk         # Contact page
│   ├── blog/
│   │   ├── blog.njk        # Blog listing page
│   │   └── posts/          # Blog posts (markdown files)
│   ├── _includes/
│   │   ├── base.njk        # Base layout template
│   │   ├── header.njk      # Site header
│   │   ├── footer.njk      # Site footer
│   │   └── post.njk        # Blog post layout
│   └── css/
│       └── style.css       # Main stylesheet
├── .eleventy.js            # Eleventy configuration
├── package.json
└── README.md
```

## Adding Blog Posts

1. Create a new markdown file in `src/blog/posts/`
2. Add frontmatter with required fields:
   ```markdown
   ---
   layout: post.njk
   title: "Your Post Title"
   date: 2026-01-25
   excerpt: "Brief description for the blog listing page"
   tags: ["post", "topic1", "topic2"]
   ---

   Your content here...
   ```

3. Run `npm run build` or `npm run dev` to see your post

## Contact Form Setup

The contact form uses Formspree. To activate:

1. Sign up at https://formspree.io
2. Create a new form for ben@commerceontap.com
3. Copy your form ID
4. Update the form action in `src/contact.njk`:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

## Deployment

### Cloudflare Pages

The site is configured to deploy automatically via Cloudflare Pages:

1. **Build Command:** `npm run build`
2. **Build Output Directory:** `_site`
3. **Branch:** `main`

Push to the `main` branch to trigger automatic deployment.

## Color Palette

- **Primary background:** `#133D38` (deep teal)
- **Content backgrounds:** `#FAF8F5` (cream), `#FFFFFF` (white)
- **Accent:** `#E8B86D` (gold)
- **Text:** `#1a1a1a` (primary), `#4a4a4a` (secondary)

## License

All rights reserved - Commerce On Tap
