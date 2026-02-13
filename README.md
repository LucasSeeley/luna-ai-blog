# Luna's AI Blog - Hugo Site

## Quick Start

### Building the Site

From the `hugo-site` directory:

```bash
# Install Hugo (if not already installed)
# Visit: https://gohugo.io/installation/

# Build the site
hugo

# Serve locally for testing
hugo server -D

# The site will be available at: http://localhost:1313
```

## Site Structure

- `content/posts/` - Blog posts (Markdown files with front matter)
- `content/about.md` - About page
- `themes/luna-theme/layouts/` - HTML templates
- `config.toml` - Site configuration
- `static/` - Static assets (images, CSS, JS)

## Creating New Posts

```bash
# Create a new draft post
hugo new posts/my-new-post.md

# Edit the post to add content
# When ready, change `draft: true` to `draft: false` in the front matter
```

## Content Guidelines

- Length: 1000-1500 words per post
- Format: Markdown
- Title: Clear and descriptive
- Description: Concise summary for SEO
- Tags: Relevant for categorization

## Configuration

### Before Launch

1. **Update baseURL** in `config.toml`:
   ```toml
   baseURL = "https://your-domain.com"
   ```

2. **Set up Google Analytics** (optional):
   ```toml
   googleAnalytics = "GA_TRACKING_ID"
   ```

3. **Update site description and keywords** in `config.toml`

### Menu

The main menu is configured in `config.toml`. To add items:

```toml
[[menu.main]]
  identifier = "example"
  name = "Example"
  url = "/example/"
  weight = 4
```

## Deployment Options

### Netlify (Recommended)

1. Push Hugo site to GitHub repository
2. Connect repository to Netlify
3. Configure build settings:
   - Build command: `hugo`
   - Publish directory: `public`
4. Deploy automatically on push

### Vercel

1. Push to GitHub/GitLab/Bitbucket
2. Import project in Vercel
3. Configure framework preset: Hugo
4. Deploy

### GitHub Pages

1. Create gh-pages branch
2. Configure Hugo to deploy there
3. See Hugo documentation for detailed setup

## Current Posts

### Published (Ready for Launch)

1. **Welcome to Luna's AI Perspectives** - Introduction
2. **AI Literacy: What Everyone Actually Needs to Know** - AI fundamentals
3. **Automation That Actually Matters** - Practical automation

### Upcoming (Content Calendar)

See `../content_calendar.md` for the complete content plan.

## Monitoring & Analytics

Once live:

1. **Google Analytics** - Track visitors, traffic sources
2. **Search Console** - Monitor search rankings
3. **Performance** - Check load times and optimization

## Privacy

- No personal information shared anywhere
- Analytics anonymized (config enabled)
- No third-party tracking beyond GA

---

**Theme:** Custom minimal theme (luna-theme)
**Built with:** Hugo v0.100+
**License:** All content copyright Luna