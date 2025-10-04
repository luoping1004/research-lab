# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-based research lab website built using the [Lab Website Template](https://greene-lab.gitbook.io/lab-website-template-docs). The site showcases research, publications, team members, and blog posts for Luo Lab at Algoma University.

## Development Commands

### Local Development
```bash
bundle exec jekyll serve
# Site will be available at http://localhost:4000/research-lab
```

### Build Site
```bash
JEKYLL_ENV=production bundle exec jekyll build --baseurl "/research-lab"
```

### Update Citations
```bash
python _cite/cite.py
```

## Site Architecture

### Content Structure

- **`_members/`**: Team member profiles (markdown files with YAML front matter)
  - Files prefixed with `aaa-`, `ab-`, etc. control display order
  - Each member has `name`, `image`, `role`, `affiliation`, `aliases`, and `links`
  - Roles include `principal-investigator` and other team positions

- **`_posts/`**: Blog posts with date-prefixed filenames (`YYYY-MM-DD-title.md`)
  - Front matter includes `title`, `author`, and `tags`

- **`_data/`**: Site data files (YAML format)
  - `sources.yaml`: Publication sources (DOI, URLs)
  - `citations.yaml`: Auto-generated from sources via citation workflow
  - `projects.yaml`, `orcid.yaml`, `types.yaml`: Additional structured data

- **`_layouts/`**: Page templates (`default.html`, `member.html`, `post.html`)

- **`_includes/`**: Reusable HTML components (button, card, citation, feature, grid, etc.)

### Citation System

The citation system uses Manubot to automatically generate formatted citations from DOIs and other identifiers:

1. Add publication identifiers to `_data/sources.yaml` (or `orcid.yaml`, `pubmed.yaml`, `google-scholar.yaml`)
2. Run `python _cite/cite.py` to generate `_data/citations.yaml`
3. The system supports plugins in `_cite/plugins/` for different citation sources
4. Environment variable `GOOGLE_SCHOLAR_API_KEY` can be set for Google Scholar plugin

### Custom Plugins

Ruby plugins in `_plugins/` extend Jekyll functionality:
- `misc.rb`: Liquid filters for data manipulation, Google Fonts URL generation, and HTML proofer integration
- `array.rb`, `hash.rb`, `file.rb`, `regex.rb`: Additional utility filters

### Styling

- Styles defined in `_styles/` directory using Sass
- Dark mode support via `_scripts/dark-mode.js`
- Custom fonts loaded via Google Fonts (configured in `_config.yaml`)

## GitHub Actions Workflows

- **`on-push.yaml`**: Runs on push to main; updates citations then builds/deploys site
- **`update-citations.yaml`**: Updates citations using `_cite/cite.py` script
- **`build-site.yaml`**: Builds Jekyll site and deploys to GitHub Pages
- **`on-pull-request.yaml`**: Runs checks on pull requests
- **`on-schedule.yaml`**: Periodic scheduled updates
- **`build-preview.yaml`**: Generates preview deployments for PRs

## Configuration

- **`_config.yaml`**: Main Jekyll configuration
  - Site metadata (title, description, links)
  - Jekyll plugins: jekyll-spaceship, jekyll-sitemap, jekyll-redirect-from, jekyll-feed, jekyll-last-modified-at
  - Collections: members, posts
  - HTML proofer setting: `proofer: false` (disabled)

## Key Technologies

- Jekyll 4.3 (static site generator)
- Ruby 3.4.5
- Python 3.11 (for citation system)
- Manubot (citation generation)
- Liquid templating engine
