# Placeholder Files and Required Replacements

This document lists all placeholder files and content that need to be replaced with your actual content.

## Source Attribution
All layout and style files were borrowed from: https://github.com/shirleyshu0503/shirleyshu0503.github.io
Please retain author/copyright notices where present in the original files.

## Placeholder Images

The following placeholder images have been created and need to be replaced with your actual images:

### 1. Avatar Image
- **Placeholder Path:** `images/avatar-placeholder.svg`
- **Suggested Replacement Path:** `images/avatar.jpg` or `images/avatar.png`
- **Usage:** Referenced in `_config.yml` under `author.avatar`
- **TODO:** Replace with your actual profile photo (recommended size: 400x400px)

### 2. Cover/Header Image
- **Placeholder Path:** `images/cover-placeholder.svg`
- **Suggested Replacement Path:** `images/cover.jpg` or `images/header.jpg`
- **Usage:** Can be used in page headers via `page.header.overlay_image` or `page.header.image`
- **TODO:** Replace with your desired cover/header image (recommended size: 1200x400px or larger)

### 3. Project/Portfolio Image
- **Placeholder Path:** `images/project-placeholder.svg`
- **Suggested Replacement Path:** Various project-specific paths in `_portfolio/` or `images/projects/`
- **Usage:** Used for portfolio/project thumbnails
- **TODO:** Replace with actual project screenshots or representative images (recommended size: 800x600px)

## Configuration File (_config.yml)

The `_config.yml` file contains numerous fields that need to be customized with your information:

### Site Information
- `title`: "Your Name" - TODO: Update with your name
- `description`: "Your tagline or research interests" - TODO: Update with your description
- `url`: Update with your actual site URL
- `repository`: Update with your GitHub repository path

### Author Information (author section)
- `avatar`: TODO: Update to point to your actual avatar image path (e.g., "avatar.jpg")
- `name`: TODO: Update with your full name
- `pronouns`: Optional - add if desired
- `bio`: TODO: Update with your professional bio
- `location`: TODO: Update with your location
- `employer`: TODO: Update with your institution/employer
- `email`: TODO: Update with your email address

### Social/Academic Links (author section)
All of the following should be updated with your actual profiles or removed if not applicable:
- `googlescholar`: TODO: Add your Google Scholar profile URL
- `orcid`: TODO: Add your ORCID URL
- `github`: TODO: Add your GitHub username
- `linkedin`: TODO: Add your LinkedIn username
- `twitter`: TODO: Add your Twitter/X handle (if applicable)
- Other academic/social profiles as needed

## Layout and Include Files

The following files have been copied and contain TODO comments in their headers:

### Layouts
- `_layouts/default.html` - Main layout template
- `_layouts/single.html` - Single page/post layout
- `_layouts/archive.html` - Archive pages layout
- `_layouts/talk.html` - Talk/presentation layout
- `_layouts/splash.html` - Splash page layout

### Includes
- `_includes/author-profile.html` - Sidebar author profile (contains detailed TODO comments)
- `_includes/masthead.html` - Site header/navigation
- `_includes/footer.html` - Site footer
- `_includes/head.html` - HTML head section
- Other include files for various components

**Action Required:** Review each file for inline HTML comments starting with `TODO:` and update accordingly.

## Content Directories

The following directories may need to be created and populated with your content:

### Pages (`_pages/`)
- About page
- CV/Resume page
- Publications page
- Research/Projects page

### Posts (`_posts/`)
- Blog posts or news items (if applicable)

### Portfolio (`_portfolio/`)
- Project descriptions and images

### Data (`_data/`)
- Navigation menu configuration
- UI text translations (if multilingual)

## Additional Notes

### Do NOT Copy from Source
The following were intentionally NOT copied from the source repository:
- Personal images (avatars, photos)
- CNAME file (custom domain configuration)
- Personal PDFs or documents
- API tokens or credentials
- User-specific email addresses

### Privacy and Security
- Never commit real API tokens, credentials, or sensitive data to the repository
- Review all configuration before making the site public
- Consider using environment variables for any sensitive configuration

### Next Steps
1. Update `_config.yml` with all your personal information
2. Replace placeholder images with your actual images
3. Review and customize layout files as needed
4. Add your content (pages, posts, portfolio items)
5. Test locally using `bundle exec jekyll serve`
6. Review the preview branch deployment before going live

## Preview Deployment

This feature branch has an automated GitHub Actions workflow that deploys to `preview/feature/borrow-shirley-layouts` branch.
- The preview branch is automatically updated on each push to this feature branch
- To preview the site, you can temporarily set GitHub Pages source to the preview branch in repository settings
- The workflow does not automatically change your Pages configuration - this must be done manually

## Questions or Issues?

If you encounter any issues or have questions about replacing placeholders:
1. Review the original source repository for examples: https://github.com/shirleyshu0503/shirleyshu0503.github.io
2. Consult Jekyll documentation: https://jekyllrb.com/docs/
3. Check the theme documentation (if using a Jekyll theme)
