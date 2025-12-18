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

- `/` - Home page
- `/cv/` - English CV
- `/cv-ja/` - Japanese CV (日本語版)

## Files

- `index.md` - Home page content
- `cv.md` - English CV content
- `cv-ja.md` - Japanese CV content
- `_layouts/` - HTML layouts
- `_config.yml` - Site configuration

## Troubleshooting

### Encoding errors when running Jekyll
If you encounter encoding errors, make sure to set the environment variables:
```bash
export LANG=en_US.UTF-8
export LC_ALL=en_US.UTF-8
```

Or use the command with environment variables as shown above.
