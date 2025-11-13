# Placeholders and TODOs for Personalization

This document lists all placeholder images and content that need to be replaced with your personal information.

## Placeholder Images

The following placeholder images have been added and should be replaced with your actual images:

### 1. Avatar/Profile Picture
- **File**: `images/avatar-placeholder.png`
- **Description**: Used for your profile picture in the sidebar and author profile
- **TODO**: Replace with your actual avatar image at `images/avatar.jpg` or `images/avatar.png`
- **Recommended Size**: 300x300 pixels or larger (square)

### 2. Cover Image
- **File**: `images/cover-placeholder.jpg`
- **Description**: Used for header/banner images on pages
- **TODO**: Replace with your actual cover photo at `images/cover.jpg`
- **Recommended Size**: 1200x400 pixels or similar wide format

### 3. Project Placeholder
- **File**: `images/project-placeholder.png`
- **Description**: Used for project thumbnails or featured images
- **TODO**: Replace with actual project images as needed
- **Recommended Size**: 600x400 pixels or similar

## Configuration File (_config.yml)

The following fields in `_config.yml` contain placeholder values marked with TODO comments:

### Site Information
- `title`: Currently set to "Xi Sun" - update if needed
- `description`: Update with your site description
- `url`: Update with your actual domain (currently uses GitHub Pages URL)

### Author Information (in `author` section)
- `avatar`: **TODO** - Update to point to your actual avatar image (e.g., "images/avatar.jpg")
- `name`: Set to "Xi Sun" - update if needed
- `bio`: **TODO** - Add your professional bio/tagline
- `location`: **TODO** - Add your location
- `employer`: **TODO** - Add your institution/employer
- `email`: **TODO** - Add your email (commented out by default for privacy)

### Social Media Links (in `author` section)
- `github`: Set to "xisun0" - update if needed
- `googlescholar`: **TODO** - Add your Google Scholar profile URL
- `orcid`: **TODO** - Add your ORCID URL
- Other social links as needed (LinkedIn, Twitter, etc.)

## Layout and Include Files

The following files contain TODO comments marking areas that need personalization:

### _layouts/ files
- All layout files have been copied from the source template
- Check for any hardcoded text or references that need updating

### _includes/ files
- `_includes/author-profile.html` - Contains author sidebar information
- `_includes/masthead.html` - Contains site header/navigation
- `_includes/footer.html` - Contains footer information
- Check these files for any hardcoded personal references

## Content Files

### Homepage and About
- Review `index.md` and any about pages for personal content
- Update research interests, biography, and other personal information

### Navigation
- Update `_data/navigation.yml` if present to customize site navigation

## What NOT to Change

The following were intentionally not copied or should not be modified:
- **CNAME** - If you have a custom domain, keep your existing CNAME file
- **Personal images** - No personal photos from the source repository were copied
- **Third-party tokens** - No analytics tokens, comment system keys, etc. were copied
- **Email addresses** - Configure your own email in _config.yml

## Source Attribution

All layouts and styles are inspired by and adapted from:
**https://github.com/shirleyshu0503/shirleyshu0503.github.io**

Please ensure you comply with the original repository's license terms when using these templates.

## Next Steps

1. Replace all placeholder images with your actual images
2. Update _config.yml with your personal information
3. Review all layout and include files for any remaining hardcoded content
4. Test the site locally with `bundle exec jekyll serve` (if Jekyll is installed)
5. Update navigation and create content pages as needed
6. Ensure no sensitive information (emails, tokens) is committed to the repository
