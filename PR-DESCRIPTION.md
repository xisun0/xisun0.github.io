# Pull Request: Add Layout and Style Templates + Preview Deployment

## 📋 Summary

This PR migrates comprehensive layout and style templates from [shirleyshu0503/shirleyshu0503.github.io](https://github.com/shirleyshu0503/shirleyshu0503.github.io) to create a modern, professional academic portfolio website. All personal content has been replaced with placeholders and clear TODO markers.

## 🎯 Objectives Achieved

1. ✅ Copied layout and style files (layouts, includes, sass, css, js)
2. ✅ Created placeholder images (SVG format with TODO text)
3. ✅ Added comprehensive TODO comments and documentation
4. ✅ Backed up original configuration files
5. ✅ Created sample pages demonstrating the layout system
6. ✅ Added GitHub Actions workflow for preview deployment

## 📁 Files Added/Modified

### Layout System (New)
- **`_layouts/`** (7 files)
  - `default.html` - Base layout template
  - `single.html` - Single page/post layout
  - `archive.html` - Archive listing layout
  - `talk.html` - Talks/presentations layout
  - `splash.html` - Full-width splash layout
  - `compress.html` - HTML compression wrapper
  - `archive-taxonomy.html` - Taxonomy archive layout

### Include Components (New)
- **`_includes/`** (40+ files)
  - `author-profile.html` - Sidebar bio and social links
  - `masthead.html` - Site header and navigation
  - `footer.html` - Site footer
  - `head.html` - HTML head section
  - `seo.html` - SEO meta tags
  - Various component includes (comments, analytics, breadcrumbs, etc.)

### Styles (New)
- **`_sass/`** (100+ files)
  - Complete SCSS/Sass source files
  - Vendor libraries (Font Awesome, Susy, Magnific Popup, Breakpoint)
  - Theme customization files
  - Layout-specific styles

### Assets (New)
- **`assets/css/`** - CSS files and main.scss entry point
- **`assets/js/`** - JavaScript for UI interactions
- **`assets/fonts/`** - Academicons font files
- **`assets/webfonts/`** - Font Awesome web fonts

### Placeholder Images (New)
- **`images/avatar-placeholder.svg`** - Avatar placeholder with TODO text
- **`images/cover-placeholder.svg`** - Cover image placeholder
- **`images/project-placeholder.svg`** - Project image placeholder

### Configuration (New/Modified)
- **`_config.yml`** - Comprehensive Jekyll config with placeholders (Modified)
- **`_config.yml.bak`** - Backup of original config (New)
- **`Gemfile`** - Ruby/Jekyll dependencies (New)
- **`_data/navigation.yml`** - Site navigation menu structure (New)
- **`.gitignore`** - Updated to exclude build artifacts (Modified)

### Documentation (New)
- **`assets/PLACEHOLDERS.md`** - Complete guide to all placeholders and replacements
- **`README-LAYOUTS.md`** - Feature branch documentation and usage guide
- **`PR-DESCRIPTION.md`** - This file

### Sample Content (New)
- **`_pages/about.md`** - Placeholder About page
- **`_pages/cv.md`** - Placeholder CV page
- **`index.md`** - Updated to use new layout (Modified)
- **`index.md.original`** - Backup of original homepage (New)
- **`index_cn.md.original`** - Backup of original Chinese homepage (New)

### Automation (New)
- **`.github/workflows/preview-deploy.yml`** - GitHub Actions workflow for preview deployment

## 🔄 GitHub Actions Workflow

The PR includes an automated workflow that:
- Triggers on push to `feature/borrow-shirley-layouts` branch
- Builds the Jekyll site using Ruby 3.1 and Bundler
- Deploys built static files to `preview/feature/borrow-shirley-layouts` branch
- **Does NOT modify** existing GitHub Pages settings

### How to Preview the Site

1. Wait for the GitHub Actions workflow to complete (check Actions tab)
2. Go to **Settings → Pages**
3. Change **Source** to branch: `preview/feature/borrow-shirley-layouts`
4. Set folder to: **`/ (root)`**
5. Click **Save**
6. Wait 1-2 minutes for GitHub Pages to deploy
7. Visit your GitHub Pages URL to see the preview

**Important:** The workflow does not automatically change your Pages settings. Your current live site remains unchanged until you manually update the Pages source.

## ✏️ TODO: Required Actions Before Going Live

### 1. Update Configuration (`_config.yml`)

Search for `TODO:` comments and update:
- **Site information:** title, description, url
- **Author information:** name, bio, location, employer, email
- **Social/academic links:** GitHub, ORCID, Google Scholar, etc.
- **SEO settings:** google_site_verification, og_image
- **Analytics:** Add tracking ID if desired

### 2. Replace Placeholder Images

- `images/avatar-placeholder.svg` → Replace with your avatar (e.g., `avatar.jpg`)
- `images/cover-placeholder.svg` → Replace with your cover image
- `images/project-placeholder.svg` → Replace with project images

Update image references in `_config.yml` (`author.avatar`, `og_image`)

### 3. Create Your Content

- **About page:** Edit `_pages/about.md` with your bio
- **CV page:** Edit `_pages/cv.md` with your CV
- **Publications:** Create `_pages/publications.md` or use `_publications/` collection
- **Research:** Create `_pages/research.md` or use `_portfolio/` collection
- **Blog posts:** Add to `_posts/` directory (optional)

### 4. Customize Navigation

Edit `_data/navigation.yml` to match your content structure

### 5. Review and Remove TODO Comments

Once you've updated content, remove or update TODO comments in:
- Layout files (`_layouts/`)
- Include files (`_includes/`)
- Your content pages

### 6. Test Locally

```bash
bundle install
bundle exec jekyll serve
```

Visit http://localhost:4000 to preview

### 7. Update Pages Settings

Once satisfied with the preview:
- Merge this PR to your main/master branch
- Update GitHub Pages settings to use your main branch
- Or continue using the preview branch if preferred

## 🔒 Security & Privacy

### What Was NOT Copied

To respect privacy and security:
- ❌ Personal images (photos, avatars)
- ❌ CNAME file (custom domain)
- ❌ Personal documents (PDFs, CVs)
- ❌ API tokens or credentials
- ❌ User-specific data files
- ❌ Blog posts and personal content

### What Was Added

- ✅ Placeholder images (SVG with clear labels)
- ✅ TODO markers for all personal fields
- ✅ Generic configuration values
- ✅ Sample pages as templates

### Dependencies

- Using `github-pages` gem for vetted versions
- Jekyll ~> 3.9 (stable, GitHub Pages compatible)
- kramdown-parser-gfm (secure markdown parser)
- Standard Jekyll plugins (sitemap, feed, etc.)

## 📄 Source Attribution

All layout and style files were borrowed from:
- **Repository:** https://github.com/shirleyshu0503/shirleyshu0503.github.io
- **Original Author:** Yunyu Shu (shirleyshu0503)
- **Based on:** Academic Pages template (fork of Minimal Mistakes Jekyll theme)

### License Compliance

- Original copyright notices retained where present
- Source repository referenced in documentation
- Academic Pages uses MIT License
- This migration is for personal academic portfolio use

## 📚 Documentation References

For detailed information, see:

1. **`assets/PLACEHOLDERS.md`** - Complete list of all placeholders and replacement instructions
2. **`README-LAYOUTS.md`** - Feature branch documentation and getting started guide
3. **Jekyll Documentation:** https://jekyllrb.com/docs/
4. **Academic Pages:** https://github.com/academicpages/academicpages.github.io
5. **Source Repository:** https://github.com/shirleyshu0503/shirleyshu0503.github.io

## 🧪 Testing Status

- ✅ All files copied successfully
- ✅ Placeholder documentation created
- ✅ TODO comments added to key files
- ✅ GitHub Actions workflow configured
- ⏳ Jekyll build will be tested by workflow on push to feature branch
- ⏳ Preview deployment will be tested automatically

## 🎉 Expected Outcome

After completing the TODO items:
- Modern, professional academic portfolio website
- Responsive design with mobile support
- Author profile sidebar with bio and social links
- Clean navigation menu
- SEO-optimized pages
- RSS feed support
- Google Analytics support (optional)

## ⚠️ Important Reminders

1. **This PR does not affect your current live site** until you:
   - Merge it to your main branch AND
   - Update GitHub Pages settings

2. **Preview branch is for testing only:**
   - Automatically updated on each push
   - Does not require manual git operations
   - Can be set as temporary Pages source for preview

3. **Original files are backed up:**
   - `_config.yml.bak`
   - `index.md.original`
   - `index_cn.md.original`

4. **All changes are reversible:**
   - Simply close this PR without merging
   - Or restore from backup files

## 📝 Checklist Before Merging

- [ ] Reviewed all TODO comments in `_config.yml`
- [ ] Replaced placeholder images with actual images
- [ ] Created/updated About page
- [ ] Created/updated CV page
- [ ] Added publications/research content
- [ ] Customized navigation menu
- [ ] Tested locally with `bundle exec jekyll serve`
- [ ] Previewed on preview branch via GitHub Pages
- [ ] Verified all links work
- [ ] Checked responsive design on mobile
- [ ] Removed unnecessary TODO comments
- [ ] Ready to make the site live

## 🤝 Questions or Issues?

If you have questions or encounter issues:
1. Check `assets/PLACEHOLDERS.md` for detailed instructions
2. Review `README-LAYOUTS.md` for usage guide
3. Consult Jekyll documentation
4. Review the source repository for examples

---

**Ready to proceed?** Review the changes, update the TODO items, test the preview, and merge when satisfied!
