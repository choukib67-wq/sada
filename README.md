
# EstateNext — Static Real Estate Site (Next.js + Tailwind + Decap CMS)

A modern, lightning-fast real estate site you can deploy to Vercel or Netlify and edit through a Git-based CMS (Decap CMS).

FEATURES
- Static export (SEO-friendly, fast)
- Listings with filters (location, type, max price, keywords)
- Property detail pages with image gallery, map embed, and contact form
- Contact & booking forms powered by Formspree (replace with your own)
- CMS editing via Decap CMS (/admin) using GitHub backend
- Tailwind CSS styling

QUICK START
1) npm install
2) npm run dev (local dev)
3) npm run build (builds & exports to out/)

DEPLOY
- Vercel: Import the repository. Build command: npm run build. Output directory: out
- Netlify: New site from Git. Build command: npm run build. Publish directory: out

CMS (Decap)
- Edit public/admin/config.yml and set:
  - repo: YOUR_GITHUB_USERNAME/YOUR_REPO_NAME
  - branch: main (or your default branch)
- You need a GitHub OAuth App for the CMS backend (or host on Netlify and use Git Gateway).
  - Docs: https://decapcms.org/docs/github-backend/
- After deploying, visit /admin to log in and manage properties.

DOMAIN (GoDaddy)
- After deployment, point your GoDaddy domain to your hosting provider:
  - Vercel: Add domain in Vercel Project Settings > Domains, then in GoDaddy set the provided CNAME/ALIAS records.
  - Netlify: Add domain in Netlify Domain settings, then in GoDaddy update nameservers or add provided DNS records.

CUSTOMIZE
- Listings live in content/properties/*.md as Markdown with frontmatter.
- Images go to public/uploads (CMS will place them there).
- Styles tweak: app/globals.css and tailwind config.
