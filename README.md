# Soichiro Inatani - Personal Website

Personal website and CV hosted on GitHub Pages.

## Local Development

### Prerequisites
- Ruby (3.2.2 or later)
- Bundler

### Setup
```bash
bundle install
```

### Running locally
```bash
LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8 bundle exec jekyll serve
```

Then open http://127.0.0.1:4000/ in your browser.

## Deployment

This site is automatically deployed to GitHub Pages when you push to the `master` branch.

### Deploy Steps

1. **Commit your changes**
   ```bash
   git add .
   git commit -m "Update CV and site content"
   ```

2. **Push to GitHub**
   ```bash
   git push origin master
   ```

3. **Verify deployment**
   - Visit https://inai17ibar.github.io
   - GitHub Pages will automatically build and deploy your site (usually takes 1-2 minutes)

### Quick Deploy Command
```bash
git add . && git commit -m "Update site" && git push origin master
```

## Site Structure

- `/` - Home page (hero, now, contact, recent posts)
- `/about/` - Profile page (自己紹介)
- `/cv/` - English CV
- `/cv-ja/` - Japanese CV (日本語版)
- `/404.html` - Not-found page

## Files

- `index.markdown` - Home page content
- `_pages/about.md` - About page content (processed via `include: [_pages]` in `_config.yml`)
- `cv.md` - English CV content
- `cv-ja.md` - Japanese CV content
- `_posts/` - Blog posts
- `_layouts/` - HTML layouts (default / home / page / post)
- `assets/css/main.css` - Site-wide stylesheet (design tokens: paper / ink / blue-ink / rule / marker)
- `_config.yml` - Site configuration

## Design Notes

「研究ノート」(researcher's field notebook) concept:
serif display (Shippori Mincho B1) + gothic body (Zen Kaku Gothic New) + mono labels (IBM Plex Mono),
a notebook margin rail with blue section tabs, and a single highlighter accent on the home hero.
Note: kramdown treats lines containing `|` as tables — use `・` or `／` as separators in Markdown body text.

## Maintenance

### Update dependencies
To update gem dependencies and fix security vulnerabilities:

```bash
bundle update
```

Or update specific gems:
```bash
bundle update nokogiri rexml
```

After updating, commit and push the changes:
```bash
git add Gemfile Gemfile.lock
git commit -m "Update dependencies to fix security vulnerabilities"
git push origin master
```

### Check for security vulnerabilities
GitHub Dependabot will automatically create alerts for security vulnerabilities.
Visit https://github.com/inai17ibar/inai17ibar.github.io/security/dependabot to view alerts.

## Troubleshooting

### Encoding errors when running Jekyll
If you encounter encoding errors, make sure to set the environment variables:
```bash
export LANG=en_US.UTF-8
export LC_ALL=en_US.UTF-8
```

Or use the command with environment variables as shown above.

### Network timeout when updating gems
If `bundle update` times out, try again later or check your internet connection.
