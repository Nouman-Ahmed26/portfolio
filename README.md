# Mohammed Nouman Ahmed — Portfolio

A dark, editorial-style portfolio site built for data analytics and web development roles.

## Stack

- Pure HTML + CSS + Vanilla JavaScript
- No build step required — just open `index.html`
- Zero external JS dependencies
- Google Fonts (Instrument Serif + DM Sans)

## Features

- **Hero section** with animated scroll hint and stats card
- **About section** with grouped skill pills
- **Projects section** with tab filtering (Web / Data & AI)
- **Project detail overlay** with full write-up, highlights, tech stack, and links
- **Contact section** with social links and a message form
- **Responsive** — works on all screen sizes
- **Dark theme** with subtle grid background and accent gradients
- **Smooth scroll** and fade-in animations via IntersectionObserver

## Personalise

Edit the `projects` array in the `<script>` tag inside `index.html`:

```js
{
  id: "your-project-id",       // used for detail overlay key
  category: "web" | "data",   // controls tab filter
  title: "Project Title",
  subtitle: "Short descriptor",
  description: "One-liner for the card",
  longDescription: "Full write-up shown in the detail panel. Use \\n\\n for paragraphs.",
  tech: ["Python", "SQL"],
  icon: "📊",                  // emoji shown on card thumbnail
  color: "#00d4ff",            // accent colour for this card
  github: "https://...",
  demo: "https://..." | null,  // null hides the Live button
  highlights: ["Point 1", "Point 2", "Point 3", "Point 4"],
  status: "Live" | "Notebook" | "GitHub",
}
```

Also update the personal info at the top of the `<body>` (name, bio, email, links).

## Deploy to Vercel

### Option 1: Vercel CLI

```bash
npm i -g vercel
cd portfolio
vercel --prod
```

### Option 2: GitHub + Vercel Dashboard

1. Push this folder to a GitHub repo
2. Go to [vercel.com](https://vercel.com) → New Project → Import your repo
3. Framework: **Other** (no build command needed)
4. Output directory: `.` (root)
5. Click Deploy

### Custom Domain

In Vercel dashboard → your project → Settings → Domains:
1. Add your domain (e.g. `noumanahmed.dev`)
2. Add the DNS records Vercel provides to your domain registrar
3. Vercel handles SSL automatically

## Project Structure

```
portfolio/
├── index.html        ← entire site (single file, self-contained)
├── vercel.json       ← Vercel routing config
├── README.md
└── src/
    └── data/
        └── portfolio.js   ← reference data file (not used at runtime)
```

## Customisation Tips

- **Colors**: Edit CSS variables in `:root` at the top of the `<style>` block
- **Fonts**: Replace the Google Fonts `<link>` and update `--serif` / `--sans` variables
- **Add sections**: Copy the section HTML pattern, give it an `id`, and add it to the nav links
- **Real images**: Replace `.card-thumbnail` background with `<img>` tags pointing to `/assets/` screenshots
