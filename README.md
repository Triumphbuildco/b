# Triumph Build Co — Website

A modern, dark-themed professional website for Triumph Build Co, a North Central Victoria–based **carpentry and construction** company.

## Overview

- **Stack:** HTML5, CSS3, vanilla JavaScript
- **Design:** Dark greyscale palette, Montserrat typography, minimalist grid layout, subtle scroll animations
- **SEO:** Meta titles/descriptions, semantic headings (H1–H3), keyword-focused content, mobile responsive

## Structure

| Page       | File         | Focus keywords |
|-----------|--------------|----------------|
| Home      | `index.html` | Carpentry & construction (local intent) |
| About     | `about.html` | Company story, approach, standards |
| Services  | `services.html` | Renovations, extensions, decks/pergolas, landscaping |
| Contact   | `contact.html` | Enquiries, North Central Victoria |

### Deep links

Services sections use fragment IDs for deep linking:

- `services.html#domestic-commercial`
- `services.html#renovations`
- `services.html#extensions`
- `services.html#decks-pergolas`
- `services.html#landscaping`

For path-based URLs (optional), use server rewrites:

**Apache (.htaccess):**
```apache
RewriteRule ^carpentry-construction$ /index.html [L]
RewriteRule ^renovations$ /services.html#renovations [R=301,L]
RewriteRule ^extensions$ /services.html#extensions [R=301,L]
```

**Netlify (_redirects):**
```
/carpentry-construction    /index.html   200
/renovations               /services.html#renovations   301
/extensions                /services.html#extensions   301
```

## Contact form

The contact form uses `action="#"`. To receive submissions:

1. **Backend:** Set `action` and `method` to your endpoint.
2. **Formspree / Netlify Forms / similar:** Replace `action="#"` with the provider’s URL and add any required fields (e.g. honeypot, redirect).

Update the placeholder phone number in `contact.html` with your real number before going live.

## Run locally

Open `index.html` in a browser, or use a local server:

```bash
# Python
python -m http.server 8000

# Node (npx)
npx serve .
```

Then visit `http://localhost:8000`.

## Brand positioning

- Language focuses on **premium carpentry and construction delivery**, clear communication, and structured execution.
