# Staging workflow

This repo is the staging copy of `ShawCole/DentalSolutions`, the repo behind www.dentalcancun.com.

- **Edit here.** Every push to `main` builds and deploys automatically to
  https://dentalcancun-staging.netlify.app (usually within 2–3 minutes).
- **Production is separate.** Nothing here reaches www.dentalcancun.com until the change is
  reviewed and merged into `ShawCole/DentalSolutions`.
- **Where the site lives:** `apps/marketing` (Next.js 15). Shared code is in `packages/core`.
  The English US landing page is in `us-landing/`.
- **Run locally:** `npm ci --legacy-peer-deps && npx turbo dev --filter=marketing`
  (serves on http://localhost:3005).
- **Before pushing:** `npx turbo build --filter=marketing` must pass, or the staging deploy fails.
