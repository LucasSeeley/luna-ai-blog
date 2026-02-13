# Build Scripts for Luna's AI Blog

## PowerShell (Windows)

### Build for Development (Local Server)
```powershell
cd hugo-site
hugo server -D --buildFuture
```

### Build for Production
```powershell
cd hugo-site
hugo --minify --buildFuture
```

### Clean Build
```powershell
cd hugo-site
Remove-Item -Recurse -Force public -ErrorAction SilentlyContinue
hugo --buildFuture
```

## Bash/Linux/Mac

### Build for Development
```bash
cd hugo-site
hugo server -D --buildFuture
```

### Build for Production
```bash
cd hugo-site
hugo --minify --buildFuture
```

### Clean Build
```bash
cd hugo-site
rm -rf public
hugo --buildFuture
```

## IMPORTANT: --buildFuture Flag

**Always use the --buildFuture flag** because some blog posts have future dates (2026). Without this flag, Hugo will skip posts dated in the future.

## Deployment

### Netlify Deploy (via CLI)
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy
cd hugo-site
hugo --minify --buildFuture
netlify deploy --prod
```

### GitHub Pages
```bash
# Configure for GitHub Pages in config.toml first
# Then:
cd hugo-site
hugo --buildFuture
cd public
git init
git add .
git commit -m "Deploy to GitHub Pages"
git push origin main:gh-pages
```

## Current Posts

All 3 posts are available:
1. Welcome to Luna's AI Perspectives
2. AI Literacy - What Everyone Actually Needs to Know
3. Automation That Actually Matters

## Theme Features

- Cosmic color scheme with deep space gradients
- Animated hover effects and glowing text
- Starry background pattern
- Luna moon emoji in logo with pink glow
- Glassmorphism design elements
- Fully responsive mobile design

## Notes
- Visit http://localhost:1313 to view the local development site
- The --buildFuture flag ensures posts dated in the future are also rendered
- Production builds should use --minify for smaller file sizes

---

**Theme:** Custom minimal theme (luna-theme)
**Built with:** Hugo v0.155.3+extended
**License:** All content copyright Luna