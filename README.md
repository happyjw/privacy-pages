# Privacy Pages

Public privacy policies for HappyJW apps, hosted via [GitHub Pages](https://docs.github.com/pages).

**Site (after Pages is enabled):** https://happyjw.github.io/privacy-pages/

## Layout

```text
privacy-pages/
├── index.html                 # Hub — list of all product policies
├── shared/
│   └── policy.css             # Shared page chrome
└── apps/
    └── <app-slug>/
        └── index.html         # That product’s Privacy Policy
```

| App slug | Product | Canonical URL |
|----------|---------|-----------------|
| `amazon-review-analyzer` | Amazon Review Analyzer (Chrome Extension) | https://happyjw.github.io/privacy-pages/apps/amazon-review-analyzer/ |

## Add a new product

1. Create `apps/<app-slug>/index.html` (copy an existing app page; keep the same CSS link).
2. Add a row to the table in root `index.html`.
3. Push to `main`.
4. Point the product’s `VITE_PRIVACY_POLICY_URL` (or equivalent) at the new URL.

## Enable GitHub Pages

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / folder: `/ (root)`
4. Save — wait ~1 minute, then open the hub URL above.

This repository is **public on purpose**: store privacy policies must be reachable without login. Keep source code in private app repos.
