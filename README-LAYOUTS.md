# Layout and Style Migration

This branch contains layouts and styles borrowed from [shirleyshu0503/shirleyshu0503.github.io](https://github.com/shirleyshu0503/shirleyshu0503.github.io) for the purpose of creating a modern academic portfolio website.

## What's Included

### Layouts (`_layouts/`)
- `default.html` - Base layout with header, footer, and content area
- `single.html` - Single page/post layout with sidebar
- `archive.html` - Archive listing pages
- `talk.html` - Talks/presentations layout
- `splash.html` - Full-width splash page layout
- `compress.html` - HTML compression wrapper

### Includes (`_includes/`)
- `author-profile.html` - Sidebar author profile with bio and social links
- `masthead.html` - Site header and navigation
- `footer.html` - Site footer
- `head.html` - HTML head section with meta tags
- `seo.html` - SEO meta tags
- Various other component includes for features like comments, analytics, breadcrumbs, etc.

### Styles (`_sass/`)
- Complete SCSS/Sass source files for styling
- Includes vendor libraries (Font Awesome, Susy grid, Magnific Popup, etc.)
- Theme customization files

### Assets
- `assets/css/` - Compiled CSS and main.scss entry point
- `assets/js/` - JavaScript for UI interactions
- `assets/fonts/` and `assets/webfonts/` - Icon fonts (Academicons, Font Awesome)

### Configuration
- `_config.yml` - Comprehensive Jekyll configuration with placeholder values
- `Gemfile` - Ruby/Jekyll dependencies
- `_data/navigation.yml` - Site navigation menu structure

### Documentation
- `assets/PLACEHOLDERS.md` - Complete guide to all placeholders and required replacements
- `README-LAYOUTS.md` - This file

## Placeholder Content

All personal content has been replaced with placeholders:

### Images
- `images/avatar-placeholder.svg` - Replace with your avatar
- `images/cover-placeholder.svg` - Replace with your cover/header image
- `images/project-placeholder.svg` - Replace with your project images

### Configuration (`_config.yml`)
Search for `TODO:` comments throughout the file. Key items to update:
- Site title and description
- Author name, bio, location, employer
- Email address
- Social media/academic profile links (GitHub, ORCID, Google Scholar, etc.)

### Content Directories (to be created)
- `_pages/` - Create your static pages (about, CV, etc.)
- `_posts/` - Blog posts or news (optional)
- `_publications/` - Your publications
- `_portfolio/` - Your projects/portfolio items
- `_talks/` - Your talks and presentations

## Getting Started

### 1. Update Configuration
Edit `_config.yml` and replace all `TODO:` items with your actual information.

### 2. Replace Placeholder Images
Replace the SVG placeholders in `images/` with your actual images.

### 3. Create Content
Create your pages in `_pages/` and populate collections as needed.

### 4. Customize Navigation
Edit `_data/navigation.yml` to define your site's navigation menu.

### 5. Local Testing
```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000` to preview your site.

## Preview Deployment

This branch has a GitHub Actions workflow (`.github/workflows/preview-deploy.yml`) that automatically builds and deploys the site to a preview branch `preview/feature/borrow-shirley-layouts`.

### How to Preview Online
1. Push changes to this branch
2. Wait for the GitHub Actions workflow to complete
3. Go to your repository Settings → Pages
4. Change Source to branch: `preview/feature/borrow-shirley-layouts`
5. Set folder to: `/ (root)`
6. Save and wait for GitHub Pages to deploy (1-2 minutes)
7. Visit your GitHub Pages URL to see the preview

**Important:** This preview deployment does not affect your current live site until you manually change the Pages source in settings.

## Source Attribution

All layout and style files were borrowed from:
- Repository: https://github.com/shirleyshu0503/shirleyshu0503.github.io
- Original author: Yunyu Shu (shirleyshu0503)

The original work is based on the Academic Pages template, which is a fork of Minimal Mistakes Jekyll theme.

## License

Please refer to the LICENSE file in the source repository for licensing information. When using these layouts:
- Retain copyright notices where present
- Provide attribution to the original authors
- Follow the terms of the original license

## What Was NOT Copied

To respect privacy and security:
- Personal images (photos, avatars)
- CNAME file (custom domain configuration)
- Personal documents (PDFs, CVs)
- API tokens or credentials
- User-specific data files
- Blog posts and personal content

## Next Steps

1. ✅ Review `assets/PLACEHOLDERS.md` for complete replacement checklist
2. ✅ Update `_config.yml` with your information
3. ✅ Replace placeholder images
4. ✅ Create your content pages
5. ✅ Test locally with `bundle exec jekyll serve`
6. ✅ Preview online using the preview branch
7. ✅ Once satisfied, merge to main branch
8. ✅ Update GitHub Pages settings to use your main branch

## Support

For issues with the layouts:
- Check the original repository: https://github.com/shirleyshu0503/shirleyshu0503.github.io
- Jekyll documentation: https://jekyllrb.com/docs/
- Academic Pages documentation: https://github.com/academicpages/academicpages.github.io

## Checklist for Going Live

- [ ] All TODO items in `_config.yml` completed
- [ ] Placeholder images replaced with real images
- [ ] About page created with your bio
- [ ] CV/Resume page created
- [ ] Publications added
- [ ] Navigation menu customized
- [ ] Tested locally
- [ ] Previewed on preview branch
- [ ] Removed TODO comments from files
- [ ] Updated GitHub Pages settings to point to main branch
