# M Chateau — Website

The static website for Chef Marcus Lim's private dining experience, M Chateau.

- **Live site:** https://mchateau.com
- **Cloudflare preview URL:** https://m-chateau.pages.dev
- **GitHub repository:** https://github.com/gracegumala/m-chateau

---

## Tech Stack

- Single self-contained HTML page (`index.html`) — HTML, CSS, and JavaScript all live inside one file. No build step.
- Fonts loaded via Google Fonts: **Italiana**, **Cormorant Garamond**, **Inter**.
- Hosted on **Cloudflare Pages**, auto-deployed from the `main` branch of this repo.
- Domain registered at **Hostinger**; DNS is delegated to **Cloudflare**.

---

## Repository Structure

```
m-chateau/
├── index.html            # The entire website (HTML + CSS + JS)
├── images/               # All photography and brand assets
│   ├── logo.png          # M Chateau house mark (white background)
│   ├── logo-cutout.png   # Same logo, transparent background
│   ├── main-course.jpeg  # Hero image
│   ├── scallop-truffle.jpeg
│   ├── chef-portrait.jpeg
│   ├── chef-plating.jpeg
│   ├── tuile-detail.jpeg
│   ├── table-setting.jpeg
│   └── menu.jpeg         # Reference PDF-style menu (not shown on site)
├── .gitignore
└── README.md
```

---

## Deploy Pipeline

1. Push to `main` on GitHub.
2. Cloudflare Pages auto-detects the commit and rebuilds within ~30 seconds.
3. Site is live at both `mchateau.com` and `m-chateau.pages.dev`.

There is **no build step** — the `index.html` file is served as-is.

---

## Making Edits

1. Clone the repo:
   ```bash
   git clone https://github.com/gracegumala/m-chateau.git
   cd m-chateau
   ```

2. Open `index.html` in any code editor (VS Code recommended).

3. Preview locally by opening `index.html` directly in a browser (double-click, or drag into Chrome).

4. Commit and push:
   ```bash
   git add .
   git commit -m "Describe what changed"
   git push
   ```

5. Verify at https://mchateau.com in ~30 seconds.

---

## Finding Sections in `index.html`

Search for these HTML comments to jump to each section:

| Section | Comment marker |
|---|---|
| Top navigation | `<!-- NAVIGATION -->` |
| Hero image + M Chateau wordmark | `<!-- HERO -->` |
| Philosophy / logo opener | `<!-- INTRO -->` |
| Scrollable dish gallery | `<!-- DISH MARQUEE -->` |
| Chef Marcus's bio + lineage | `<!-- CHEF -->` |
| Five-course tasting menu | `<!-- MENU -->` |
| Instagram video / social section | `<!-- SOCIAL FEED -->` |
| Reserve panel (Instagram DM CTA) | `<!-- RESERVE -->` |
| Footer | `<!-- FOOTER -->` |

---

## Contact Points Wired into the Site

| Purpose | Value | Where |
|---|---|---|
| Reservation CTA | Instagram DM to `@real.mchateau` | Reserve section |
| Enquiry email (footer) | `marcuschateau25@gmail.com` | Footer |
| Instagram handle | `@real.mchateau` (URL: `https://www.instagram.com/real.mchateau/`) | Footer, Social section, Reserve CTA |

To change any of these, search-and-replace in `index.html` and push.

---

## Fonts

Loaded via a single Google Fonts `<link>` in `<head>`:

- **Italiana** — the M Chateau wordmark, section titles
- **Cormorant Garamond** — body copy, editorial paragraphs, italics
- **Inter** — small uppercase labels, nav links, form labels

All three are free under the SIL Open Font License and can be used in print collateral (menus, business cards).

---

## Domain & DNS

- Domain `mchateau.com` is registered at **Hostinger**.
- Nameservers point to Cloudflare: `piers.ns.cloudflare.com` and `irena.ns.cloudflare.com`.
- The custom domain is configured inside the **Cloudflare Pages project → Custom domains**.
- SSL certificates are auto-provisioned by Cloudflare.

---

## Common Tasks

**Change the menu:** Search for `<!-- MENU -->` in `index.html`. Each course is inside a `<div class="course reveal">`. Enhancements are inside `<div class="enh-row reveal">`.

**Change a photo:** Replace the file inside `images/` with the same filename, or upload a new file and update the `src="..."` reference in `index.html`. Keep aspect ratios similar (e.g. hero image needs to work at 16:9+).

**Change the Instagram handle:** Search for `real.mchateau` in `index.html` and replace with the new handle.

**Change the reservation email:** Search for `marcuschateau25@gmail.com` in `index.html` and replace.

**Update the chef bio:** Search for `<!-- CHEF -->`. Body copy is inside `<p class="reveal">` tags. The lineage table (Mentorship, Brigade, etc.) is a `<ul class="lineage">`.

---

## Support Handover Checklist

The following access is needed to fully manage the site:

- [ ] **GitHub** — collaborator or owner on `gracegumala/m-chateau`
- [ ] **Cloudflare** — member on the Cloudflare account with access to the `m-chateau` Pages project
- [ ] **Hostinger** — access to renew or transfer the `mchateau.com` domain
- [ ] **Google account** — access to `marcuschateau25@gmail.com` for enquiries
- [ ] **Instagram** — access to `@real.mchateau` for reservations
