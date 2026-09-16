# content-assets

Public image host for the MedForm3D / LocalTranscript content pipeline.

Images are published here for one reason: the [Buffer API](https://developers.buffer.com)
attaches media **by public URL** and has no direct upload, so a generated post image has to be
fetchable without auth before it can be scheduled.

- `images/<slug>.jpg` — one file per content-pipeline slug. Regenerations are `<slug>-v2.jpg`,
  `-v3`, … and earlier versions are never deleted (a post already scheduled may still reference one).
- Raw URL: `https://raw.githubusercontent.com/diegoje/content-assets/main/images/<slug>.jpg`

Master copies live in the vault at `02-Personal/Projects/content-assets/`. This repo is a
publishing mirror, not the source of truth.

**Nothing confidential belongs here.** No client names, no patient data, no unreleased product
shots — the repo is world-readable by design. Images are metadata-stripped before they are
committed (fresh re-encode, verified free of `c2pa|jumbf|xmp|exif`).
