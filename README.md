# BECM BODY90 — GitHub Pages

This folder contains the single-file BODY90 web app prepared for GitHub Pages.

## Publish

1. Create a GitHub repository named `BECOM_BODY90`.
2. Upload `index.html` and `.nojekyll` to the repository root.
3. In repository **Settings → Pages**, select the `main` branch and `/ (root)` as the source.
4. When GitHub provides the final HTTPS site URL, open Supabase **Authentication → URL Configuration**. Set **Site URL** to the exact site URL and add that same URL as an allowed redirect URL. Do not leave `http://localhost:3000` as the production destination.
5. The signup flow now requests the page's current HTTPS URL as the confirmation redirect.

## Privacy and visibility

GitHub Pages is a public website. With GitHub Free, Pages requires a public repository; even when the source repository is private on eligible plans, the published Pages site is still public by default. The app contains only the Supabase publishable key (safe for browser use under the included RLS policies), no service-role key, and no personal BODY90 records. User health and training records are not included in these files.

The site URL is not known yet, so Supabase redirect allow-list configuration must be finalized after the repository owner and URL are confirmed.
