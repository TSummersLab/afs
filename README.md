# Autonomous Fleet Systems — Lab Website

Public website for the Autonomous Fleet Systems project, Summers Lab,
University of Texas at Dallas.

**Live site:** https://tsummerslab.github.io

---

## Structure

```
index.html        # Main site (single-file, no build step required)
_config.yml       # GitHub Pages metadata
.nojekyll         # Tells GitHub Pages to serve HTML directly
assets/
  images/         # Lab photos, robot photos, diagrams
  videos/         # Demo clips (keep small; link to YouTube for large files)
docs/             # External-facing versions of project documents (PDF)
CONTRIBUTING.md   # How to make edits (for co-directors and students)
```

## Making edits

See `CONTRIBUTING.md` for step-by-step instructions tailored for
co-directors and students who may not be regular GitHub users.

The short version: edit `index.html`, commit to `main`, and GitHub
Pages will update the live site automatically within ~60 seconds.

## Adding photos and videos

1. Place image files in `assets/images/`
2. In `index.html`, replace any `<div class="media-placeholder">` block
   with a standard `<img>` or `<video>` tag referencing the file
3. For videos larger than ~10MB, upload to YouTube and embed with
   an `<iframe>` instead

## Replacing placeholders

Search `index.html` for the comment `<!-- placeholder -->` or look for
`media-placeholder` CSS class to find all sections awaiting real content.

Co-director bios and photos are clearly marked with `[Co-Director 1]`
and `[Co-Director 2]` — replace those strings with real information.

---

*Maintained by the AFS project team. Questions → tyler.summers@utdallas.edu*
