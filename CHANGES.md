# What changed in this build

New SVG assets (all validated as well-formed XML):

- `assets/divider.svg` — animated section divider (data packet travels the wire). Replaces the plain `---` before each section heading.
- `assets/footer.svg` — terminal `exit` footer with animated top bar + status chips. **Fixes the previously broken footer** that pointed at a nonexistent `output/footer.svg`.
- `assets/glyph.svg` — animated 3-block marker now sits beside every section heading.
- `assets/cards/*.svg` — five clickable project cards with baked-in real repo data (stars, language, tags). Each is wrapped in a markdown link so it stays clickable.

README wiring:

- Featured-builds table → animated card grid. Cards link to their repos; heading text stays real markdown so it remains crawlable.
- All 8 section headings now carry the animated glyph but remain `##` markdown (anchors + SEO intact).
- Footer now points to the committed `./assets/footer.svg`.

Card stats are **static** (baked in July 2026). To refresh them, edit the values in `gen_cards.js` and re-run `node gen_cards.js`.

## Still on you (from earlier)

1. Verify the email `rajatkudash.2004@gmail.com` — looks like it may be a typo for `kumardash`.
2. Deploy your own `github-readme-stats` + `github-profile-trophy` forks to Vercel and update the `qmrajat-stats` / `qmrajat-trophies` URLs, or the telemetry section stays 503.
3. Add `METRICS_TOKEN` secret and run each workflow once to populate `metrics/` and the `output` branch (snake + metrics 404 until then).
4. Optional: swap the plain-text default credentials in the Dash_Poultry and TableServe READMEs for "see setup.sql".
