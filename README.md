# Technsyntax — main site

Static site, deployed on Netlify via GitHub. No build step required.

## File structure
```
technsyntax/
├── index.html          # homepage
├── netlify.toml        # redirects, headers, caching
├── robots.txt
├── sitemap.xml
├── assets/
│   └── css/
│       └── tokens.css  # design tokens shared across the ecosystem
└── pages/
    └── about.html
```

## To push this to GitHub

From the folder containing these files:

```bash
git init
git remote add origin https://github.com/keertistaff/technsyntax.git
git add .
git commit -m "Rebuild: unified design system, new homepage"
git branch -M main
git push -u origin main --force
```

Use `--force` only because the repo was emptied — drop it on future pushes.

If the remote already has a `main` branch history you want to keep instead,
skip `--force` and resolve any conflicts normally.

## After pushing
1. Confirm Netlify is watching this repo/branch (Site settings → Build & deploy).
2. Trigger a deploy if it doesn't auto-fire.
3. Check `https://www.technsyntax.site/` loads with the new design.
4. Set `www.technsyntax.site` as the primary domain in Netlify's domain settings if not already.
