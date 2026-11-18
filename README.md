# VIC1 interactive surface relighting viewer

This is a lightweight WebGL normal-map relighting viewer generated from the supplied files:
- RTI_5_albedo.tif → assets/albedo.webp (2560px wide)
- RTI_5_normals_wood.tif → assets/normal.webp (2560px wide)
- Confidence TIFF was inspected but not used to mask pixels; edge artifacts may remain.

The original source TIFF files are not included because they total hundreds of MB.
This is a *photometric-stereo normal-map relighting approximation* rather than original RTI polynomial/PTM/RBF fitting or OpenLIME rendering.

## Deploy
1. Create new public GitHub repo `vic1-rti-viewer`.
2. Upload `index.html` and **assets** folder, preserving paths.
3. Import repository into Vercel, Framework Preset `Other`, no build command.
4. Open its public URL and test pointer-driven illumination and controls.
5. To embed in another site, use iframe src pointing to the deployed URL, e.g.:

<iframe src="https://YOUR-RI-VERCEL-URL/" width="100%" height="650" loading="lazy" title="Interactive wood surface RTI viewer"></iframe>

You can use this as your existing OBJ hotspot site's `rtiViewerUrl`, if it supports iframe URLs.

## Scientific notes
- The shader assumes normal RGB channels encode XYZ in [0,255] => [-1,1] and may need Y inversion.
- Exposure defaults to 5x because the supplied albedo values are dark.
- The normal map and albedo are web-sized versions; preserve originals for research.
- The image background/edge shows processing artifacts; interpret only valid timber pixels.
- The supplied RTI_5_command indicates the `rti_shadow_aware.py` workflow.
