# Contributing to the AFS Website

This guide is written for co-directors and students who need to make
edits to the site but may not use GitHub regularly. It covers the
three most common tasks: editing text, adding a photo, and updating
a placeholder section.

---

## Setup (one time only)

You need a GitHub account. If you don't have one, create one at
https://github.com/join — it takes two minutes.

Then ask Tyler to add you to the **TSummersLab** organization as a
member with write access to this repository. Once added, you can
edit files directly in the GitHub web interface without installing
anything.

---

## Task 1: Edit text on the site

The entire site is in one file: `index.html`. You can edit it directly
in GitHub's web editor.

1. Go to https://github.com/TSummersLab/TSummersLab.github.io
2. Click on `index.html` in the file list
3. Click the pencil icon (✏️) in the top right — "Edit this file"
4. Find the text you want to change (use Ctrl+F / Cmd+F to search)
5. Make your edit
6. Scroll to the bottom to the "Commit changes" section
7. Write a brief description of what you changed (e.g. "Update Prof. Smith bio")
8. Click "Commit changes"

The live site updates automatically within about 60 seconds.

**Things that are safe to edit:**
- Any visible text between HTML tags
- Your faculty bio (search for `[Co-Director 1]` or `[Co-Director 2]`)
- The email address in the "Express Interest" button (search for `mailto:`)
- Your faculty page link (search for `Faculty page ↗`)

**Things to be careful with:**
- Don't delete `<` or `>` characters — they are part of the HTML structure
- Don't delete `class=` attributes — they control the visual styling
- If something looks broken after your edit, use the GitHub history to
  revert: go to the file, click "History", find the previous version,
  and click "Revert"

---

## Task 2: Add your faculty photo

1. Prepare your photo: a square or 4:3 aspect ratio JPEG works best.
   Resize to roughly 800×600px or 800×800px before uploading (keeps
   the repository size small).

2. Go to https://github.com/TSummersLab/TSummersLab.github.io

3. Navigate to `assets/images/` (create this folder if it doesn't exist:
   click "Add file" → "Create new file" → type `assets/images/.gitkeep`
   and commit)

4. Click "Add file" → "Upload files"

5. Drag your photo in. Name it something clear like `prof-smith.jpg`.
   Click "Commit changes".

6. Now edit `index.html` to replace the placeholder with your image.
   Find your faculty card section (search for your name or
   `[Co-Director 1]`). Replace:

```html
<div class="faculty-photo">Photo coming soon</div>
```

with:

```html
<img src="assets/images/prof-smith.jpg"
     alt="Prof. Jane Smith"
     style="width: 100%; aspect-ratio: 4/3; object-fit: cover;">
```

7. Commit the change. Your photo will appear on the live site within
   ~60 seconds.

---

## Task 3: Add a demo video

For short clips (under 10MB): upload to `assets/videos/` following the
same process as photos, then replace the placeholder:

```html
<!-- Replace this: -->
<div class="media-placeholder"> ... </div>

<!-- With this: -->
<video autoplay muted loop playsinline
       style="width: 100%; border-radius: 4px;">
  <source src="assets/videos/formation-demo.mp4" type="video/mp4">
</video>
```

For longer videos: upload to YouTube (unlisted is fine if you don't
want it publicly searchable), then replace the placeholder with an
iframe embed. YouTube provides the embed code under Share → Embed.
Paste it inside a `<div style="aspect-ratio: 16/9; overflow: hidden;">`.

---

## Task 4: Add a lab photo to the hero section

Find this block in `index.html`:

```html
<!-- Hero video placeholder -->
<div style="background: var(--ink); padding: 0 0 4rem;">
  <div class="container">
    <div class="media-placeholder"> ... </div>
  </div>
</div>
```

Replace the `<div class="media-placeholder">` with your image or video
following Task 2 or Task 3 above. For maximum impact, a wide panoramic
photo of the lab high bay with robots flying works best here.

---

## Task 5: Complete the co-director bios

Search `index.html` for `[Co-Director 1]` and `[Co-Director 2]`.
You'll find faculty card blocks like this:

```html
<div class="faculty-card">
  <div class="faculty-photo">Photo coming soon</div>
  <div class="faculty-info">
    <h3>Prof. [Co-Director 1]</h3>
    <div class="faculty-role">Co-Director</div>
    <p>[Research area and affiliation — to be completed.]</p>
    <p style="margin-top: 0.5rem;"><a href="#">Faculty page ↗</a></p>
  </div>
</div>
```

Replace the bracketed placeholders with real information. Update the
`href="#"` on the faculty page link to your actual faculty page URL.

---

## Checking what you changed before committing

When editing in GitHub's web interface, click the "Preview" tab above
the editor to see a rendered view. Note that GitHub's preview renders
Markdown files nicely but shows HTML as raw source — to preview HTML
changes, you can either:

1. Copy the full `index.html` content into a local file and open it
   in your browser, or
2. Commit the change and wait 60 seconds for the live site to update
   (then revert if something looks wrong)

---

## Getting help

- **Something looks broken:** Post a screenshot in the project Slack/Teams
  channel with a description of what you changed.
- **Not sure if a change is safe:** Ask before committing. Small questions
  in the channel are faster than fixing a broken site.
- **Want to make a bigger structural change:** Open a GitHub Issue
  describing what you want to do. Tyler or the Track 5 students can
  help plan it.

---

*Questions → tyler.summers@utdallas.edu or the project channel.*
