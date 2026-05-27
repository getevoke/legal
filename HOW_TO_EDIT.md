# How the Evoke legal site works (privacy policy + ToS)

**Live URL:** https://getevoke.github.io/legal/
- Privacy Policy: https://getevoke.github.io/legal/privacy-policy
- Terms of Service: https://getevoke.github.io/legal/terms-of-service

## Where it's hosted
- GitHub repo: **`getevoke/legal`** (public)
- GitHub Pages, Jekyll `jekyll-theme-minimal`, served from `main` branch root (`build_type: legacy`)
- Plain markdown files render directly — `privacy-policy.md`, `terms-of-service.md`, `index.md` (only `index.md` has Jekyll front matter; the policy/ToS files are bare markdown and render fine)

## This local clone
`/Users/faresnabil/faresdev/getevoke-legal` — clone of `getevoke/legal`. Edit here.

## To update the privacy policy or ToS
1. Edit the `.md` file here (or copy from the app repo's mirror at `/Users/faresnabil/faresdev/Evoke/legal/`)
2. `git add <file> && git commit -m "..." && git push origin main`
3. Wait ~1-2 min for Pages to rebuild. Check build: `gh api repos/getevoke/legal/pages/builds/latest --jq .status` (want `"built"`)
4. Verify live (cache-bust): `curl -s "https://getevoke.github.io/legal/privacy-policy?cb=$(date +%s)" | grep -i "<marker>"`

## Source-of-truth note
The app repo (`Evoke/legal/*.md`) holds mirror copies. The **canonical published source is THIS repo** (`getevoke/legal`). When editing, sync both or treat this repo as authoritative. As of 2026-05-27 the privacy policy here is current (discloses PostHog + Luciq + opt-out); the ToS still needs v1 subscription terms (Evoke bead Evoke-ajd8).
