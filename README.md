# Art Agenda

A New York City exhibition directory, monthly watchlist, and gallery map.

**Website:** https://jpcortinab.github.io/art-agenda/

## Publish

In GitHub, open **Settings → Pages** for this repository. Under **Build and deployment**, select **Deploy from a branch**, choose **main**, choose **/(root)**, and save. GitHub Pages then serves `index.html` from the root.

## Structure

- `index.html` — Art Agenda page, watchlist, and interactive map
- `exhibitions.json` — curated exhibition catalog (update this to add new shows)
- `cloud.js` — optional sign-in and private cloud sync
- `cloud-config.js` — *public* Supabase project URL and publishable key
- `supabase/setup.sql` — database table and row-level security policies
- `SYNC_SETUP.md` — cloud account setup instructions

## Sign-in configuration

In the connected Supabase project, go to **Authentication → URL Configuration** and add
`https://jpcortinab.github.io/art-agenda/` to allowed redirect URLs. Keep any existing site URL and redirects used by the restaurant website.

Existing saved browser watchlists use `localStorage` under `jpcortinab.github.io`, which is shared by the old and new paths **in the same browser**. For other devices, sign in to sync or use the one-time transfer link.

## Privacy

This repository is public; it contains no service-role keys. Cloud data is protected by per-user row-level security. Only publishable browser keys belong in `cloud-config.js`.
