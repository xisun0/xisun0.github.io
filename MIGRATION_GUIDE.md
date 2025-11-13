# Migration Guide: Layout and Style Templates

This guide explains how to customize the migrated layout and style templates for your personal GitHub Pages site.

## Overview

The layouts, styles, and components in this repository have been copied from [shirleyshu0503's GitHub Pages repository](https://github.com/shirleyshu0503/shirleyshu0503.github.io) to provide a professional academic website template. This migration includes:

- Layout templates for pages, posts, publications, talks, and teaching materials
- SCSS/CSS styling and design
- JavaScript for interactive UI elements
- Site navigation and configuration structure

## What Was Copied

### Directories and Files
- `_layouts/` - Page layout templates (HTML)
- `_includes/` - Reusable HTML components (header, footer, sidebar, etc.)
- `_sass/` - SCSS source files for styling
- `assets/` - CSS, JavaScript, fonts, and other frontend assets
- `_data/` - Configuration data (navigation, UI text)
- `Gemfile` - Ruby gem dependencies for Jekyll

### Placeholder Content
- `images/avatar-placeholder.png` - Replace with your avatar
- `images/cover-placeholder.jpg` - Replace with header/cover image
- `images/project-placeholder.png` - Replace with project images
- `_config.yml` - Contains TODO markers for personalization

## What Was NOT Copied

For privacy and security reasons, the following were intentionally not copied:
- Personal images from the source repository
- CNAME file (custom domain configuration)
- Third-party API keys, tokens, or credentials
- Personal email addresses
- Private or sensitive content

## Step-by-Step Customization

### 1. Replace Placeholder Images

**Avatar/Profile Picture:**
```bash
# Replace the placeholder with your actual avatar
# Recommended: 300x300 pixels or larger (square)
cp your-avatar.jpg images/avatar.jpg
```

Then update `_config.yml`:
```yaml
author:
  avatar: "images/avatar.jpg"  # Update this line
```

**Cover/Header Images:**
```bash
# Add your cover image (if needed)
# Recommended: 1200x400 pixels or similar wide format
cp your-cover.jpg images/cover.jpg
```

**Project Images:**
Add project-specific images to the `images/` directory as needed.

### 2. Update Site Configuration (_config.yml)

Open `_config.yml` and search for `TODO` comments. Update the following sections:

**Basic Information:**
```yaml
title: "Your Name"
name: "Your Name"
description: "Your professional tagline or research interests"
url: https://yourusername.github.io  # Or your custom domain
repository: "yourusername/yourusername.github.io"
```

**Author Profile:**
```yaml
author:
  avatar: "images/avatar.jpg"  # Your actual avatar path
  name: "Your Name"
  bio: "Your professional title and brief bio"
  location: "Your City, Country"
  employer: "Your Institution"
  email: "your.email@example.com"  # Uncomment to enable
```

**Social Media Links:**
Update these fields with your usernames/URLs:
```yaml
author:
  github: "yourusername"
  googlescholar: "https://scholar.google.com/citations?user=YOUR_ID"
  orcid: "https://orcid.org/YOUR-ORCID-ID"
  linkedin: "yourusername"
  twitter: "yourusername"
  # Add others as needed
```

**Analytics (Optional):**
```yaml
analytics:
  provider: "google"  # or "google-analytics-4"
  google:
    tracking_id: "UA-XXXXXXXXX-X"  # Your tracking ID
```

### 3. Customize Navigation

Edit `_data/navigation.yml` to set up your site menu:

```yaml
main:
  - title: "About"
    url: /
  
  - title: "Research"
    url: /research/
  
  - title: "Publications"
    url: /publications/
  
  - title: "Teaching"
    url: /teaching/
  
  - title: "CV"
    url: /cv/
```

### 4. Create Content Pages

Create pages in the `_pages/` directory (create this directory if it doesn't exist):

**Example: _pages/about.md**
```yaml
---
layout: single
title: "About"
permalink: /
author_profile: true
---

Your about content here...
```

**Example: _pages/research.md**
```yaml
---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

Your research description here...
```

### 5. Add Collections (Optional)

The template supports several content collections:

**Publications** (`_publications/` directory):
```yaml
---
title: "Paper Title"
collection: publications
permalink: /publication/paper-slug
date: 2023-01-01
venue: 'Journal Name'
paperurl: 'http://example.com/paper.pdf'
citation: 'Your citation format'
---

Paper abstract or description...
```

**Teaching** (`_teaching/` directory):
```yaml
---
title: "Course Name"
collection: teaching
type: "Course"
permalink: /teaching/course-slug
venue: "University Name, Department"
date: 2023-09-01
---

Course description...
```

**Talks** (`_talks/` directory):
```yaml
---
title: "Talk Title"
collection: talks
type: "Talk"
permalink: /talks/talk-slug
venue: "Conference Name"
date: 2023-06-01
location: "City, Country"
---

Talk abstract...
```

**Portfolio** (`_portfolio/` directory):
```yaml
---
title: "Project Name"
excerpt: "Short project description"
collection: portfolio
---

Project details...
```

### 6. Local Development and Testing

If you have Ruby and Jekyll installed, you can test locally:

```bash
# Install dependencies
bundle install

# Serve the site locally
bundle exec jekyll serve

# View at http://localhost:4000
```

### 7. Deploy to GitHub Pages

Once you're satisfied with your changes:

1. Commit all changes to your repository
2. Push to the `main` branch (or your default branch)
3. GitHub Pages will automatically build and deploy your site
4. Visit `https://yourusername.github.io` to see your site

### 8. Custom Domain (Optional)

To use a custom domain:

1. Create a `CNAME` file in the root directory with your domain:
   ```
   www.yoursite.com
   ```

2. Configure your domain's DNS settings (see [GitHub's documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site))

3. Update `_config.yml`:
   ```yaml
   url: https://www.yoursite.com
   ```

## File Structure Reference

```
.
├── _config.yml           # Main configuration file
├── _data/                # Data files
│   ├── navigation.yml    # Site navigation menu
│   └── ui-text.yml       # UI text strings
├── _includes/            # Reusable HTML components
│   ├── author-profile.html
│   ├── footer.html
│   ├── masthead.html
│   └── ...
├── _layouts/             # Page layout templates
│   ├── default.html
│   ├── single.html
│   └── ...
├── _sass/                # SCSS source files
├── assets/               # Frontend assets (CSS, JS, fonts)
├── images/               # Image files
├── _pages/               # Site pages (create this)
├── _posts/               # Blog posts (create if needed)
├── _publications/        # Publications (create if needed)
├── _teaching/            # Teaching materials (create if needed)
├── _talks/               # Talks/presentations (create if needed)
└── _portfolio/           # Portfolio items (create if needed)
```

## Troubleshooting

### Site Not Building
- Check that `_config.yml` syntax is valid (YAML is sensitive to indentation)
- Ensure all required plugins are listed in `_config.yml` and `Gemfile`
- Check GitHub Actions logs for build errors

### Styles Not Appearing
- Verify `_sass/` and `assets/css/` directories are present
- Check that `main.scss` imports are correct
- Clear browser cache

### Images Not Showing
- Verify image paths in `_config.yml` are correct
- Ensure images exist in the specified locations
- Use forward slashes (`/`) in paths, not backslashes

### Navigation Not Working
- Check `_data/navigation.yml` syntax
- Ensure page permalinks match navigation URLs
- Create missing pages referenced in navigation

## Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Academic Pages Documentation](https://github.com/academicpages/academicpages.github.io)
- [Original Template Source](https://github.com/shirleyshu0503/shirleyshu0503.github.io)

## Attribution

This template is based on the Academic Pages theme, which is itself a fork of Minimal Mistakes. The specific implementation was adapted from:

**Source Repository:** https://github.com/shirleyshu0503/shirleyshu0503.github.io

Please respect the licenses of these projects when using this template.

## License

Make sure to review and comply with the license terms of:
- The original Minimal Mistakes theme
- The Academic Pages fork
- The source repository you adapted from

Typically, these projects use MIT or similar permissive licenses, but always verify.

## Questions?

For questions about:
- **Jekyll and GitHub Pages:** See official documentation
- **This specific template:** Check the source repository or create an issue
- **Customization:** Refer to Jekyll documentation and this guide

## Checklist for Going Live

Before deploying your site, make sure you've:

- [ ] Replaced all placeholder images with your actual images
- [ ] Updated `_config.yml` with your personal information
- [ ] Removed all TODO comments after addressing them
- [ ] Created your main content pages (about, research, etc.)
- [ ] Customized the navigation menu
- [ ] Added your publications/teaching/talks (if applicable)
- [ ] Tested the site locally (if possible)
- [ ] Verified no sensitive information (emails, tokens) is committed
- [ ] Checked all links work correctly
- [ ] Reviewed the site on mobile devices (responsive design)
- [ ] Set up custom domain (if desired)
- [ ] Configured analytics (if desired)

Good luck with your new website!
