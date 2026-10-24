# Shop Directory (demo PWA)

Offline-first demo for the shop/owner/location database project. Data is stored on the device (localStorage) so it works with no server.

## Features
- Add, edit, delete (soft delete) shops with owner, type, address, hours, status
- Search, filter by shop type, "Sort by nearest" using GPS
- Export JSON backup / CSV, import JSON backup
- Installable, works offline
- Optional: send data to a Google Sheet (needs an Apps Script web app URL)

## Host on GitHub Pages
1. Create a repo and upload all files in this folder (keep them at the repo root).
2. Repo Settings > Pages > Deploy from branch > `main` / root.
3. Open `https://<username>.github.io/<repo>/` on your phone and choose Install / Add to Home screen.

## Run locally
`python3 -m http.server 8000` then open http://localhost:8000 (service workers need localhost or https).

## Updating
Change `CACHE` in `sw.js` (e.g. `shopdir-v2`) whenever you release a new version.

## Next steps
Replace localStorage with Supabase/PostgreSQL using the v2 schema, add logins and roles.
