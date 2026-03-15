# Paperkite Reader — Landing Page & Privacy Policy

Public website for the Paperkite Reader app, hosted on GitHub Pages with a custom domain.

## Live URLs

- **Landing page**: https://paperkitereader.com
- **Privacy policy**: https://paperkitereader.com/privacy.html

## Files

| File | Purpose |
|------|---------|
| `index.html` | App landing page (hero, features, store links, footer) |
| `privacy.html` | Privacy policy (linked from Play Store and landing page) |
| `icon.png` | App icon used on the landing page |
| `CNAME` | Custom domain config for GitHub Pages (auto-generated, do not edit) |

## Hosting

- Hosted via **GitHub Pages** from the `main` branch, root `/`.
- Custom domain `paperkitereader.com` is configured via **Cloudflare DNS**.
- DNS records (managed in Cloudflare dashboard):
  - `A` records for apex domain → GitHub Pages IPs (`185.199.108.153` – `185.199.111.153`)
  - `CNAME` for `www` → `parsolomeo.github.io`

## How to Update

1. Edit the relevant HTML file in this repo.
2. Commit and push to `main`.
3. Changes go live automatically within 1–2 minutes (GitHub Pages rebuilds on push).

```bash
cd paperkite-site
# make edits...
git add . && git commit -m "Describe your change" && git push
```

## Design System

The site matches the Flutter app's theme defined in `PDF-Project/lib/theme/app_theme.dart`:

| Token | Value | Usage |
|-------|-------|-------|
| `--bg` | `#F4EFE6` | Page background (warm parchment) |
| `--surface` | `#FFFBF4` | Card/section backgrounds (light cream) |
| `--text-primary` | `#3B2F23` | Headings, body text (dark brown) |
| `--text-secondary` | `#6B5A46` | Secondary text, descriptions |
| `--accent` | `#B1783C` | Buttons, links (amber/copper) |
| `--divider` | `#E3D6C4` | Borders, separators |

- **Fonts**: EB Garamond (headings/body), Inter (UI text, descriptions)
- **Border radius**: 18px for cards, 14px for buttons
- **Shadows**: subtle, using `rgba(59, 47, 35, 0.06)`

## Store Links

The Google Play and App Store buttons in `index.html` currently link to `#`. Update the `href` values once the store listings are live:

```html
<!-- Find these lines in index.html and replace href="#" -->
<a href="#" class="store-btn primary" ...>Google Play</a>
<a href="#" class="store-btn secondary" ...>App Store</a>
```

## Contact Email

Both `index.html` and `privacy.html` reference `paperkitereader@gmail.com`. Update in both files if the contact email changes.
