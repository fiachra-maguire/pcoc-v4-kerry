# PCOC V4 Nursing Update — Kerry Specialist Palliative Care Unit

Static site bundling the in-service videos and reference handout for the PCOC Version 4 nursing update at Kerry SPCU.

## Files

```
pcoc-v4-kerry/
├── index.html                 ← landing page, videos at top, handout below
├── smileys.pdf                ← patient-facing ESAS scale (vector)
├── smileys_print.png          ← raster fallback for the scale
└── videos/
    ├── pcoc_v4_kerry_walkthrough.mp4   ← full slide walkthrough (~97 MB)
    ├── 4AT_explainer.mp4               ← 4AT primer (~6 MB)
    ├── delirium_awareness.mp4          ← delirium recognition (~15 MB)
    └── (PINCHES ME video, to be added)
```

Total size: ~120 MB. Within GitHub Pages limits.

## Deploying to GitHub Pages

1. Create a new public repository on github.com (e.g. `pcoc-v4-kerry`).
2. From this folder, push the contents:

   ```bash
   git init
   git add .
   git commit -m "Initial PCOC V4 nursing update site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/pcoc-v4-kerry.git
   git push -u origin main
   ```

3. On github.com → repository **Settings → Pages**, set source to `main` branch / root.
4. After a minute or two, the site is live at:

   ```
   https://<your-username>.github.io/pcoc-v4-kerry/
   ```

## Updating later

Drop a new MP4 into `videos/` and edit `index.html`:

- Replace the placeholder block in the third video card (the PINCHES ME one) with a `<video controls preload="metadata"><source src="videos/pinches_me.mp4" type="video/mp4"></video>` once that video is ready.
- Push the change.

## Privacy note

This is a public GitHub repository. Don't put anything containing patient information into the videos or page text. The current videos cover generic clinical teaching only.

If patient data ever needs to be included, switch to a private repo with GitHub Pages (requires a paid GitHub plan) or a different hosting model.
