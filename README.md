# Mejia Photography

Website for mejia-photography.com (single-page static site: `index.html` + an `images` folder).

## Folder structure
- `index.html`: the whole site. Colors and fonts are in the `:root` block at the top of the file.
- `images/portfolio/`: portfolio photos
- `images/hero.jpg`: top banner photo (optional)
- `images/about.jpg`: About section photo (optional)

## Changing or adding portfolio photos

### Replace a placeholder or an existing photo
1. Save your photo in `images/portfolio/` using one of these names:
   `portraits-01.jpg`, `portraits-02.jpg`, `portraits-03.jpg`, `portraits-04.jpg`, `portraits-05.jpg`,
   `graduation-01.jpg`, `graduation-02.jpg`,
   `pets-01.jpg`, `pets-02.jpg`, `pets-03.jpg`, `pets-04.jpg`, `realestate-01.jpg`, `realestate-02.jpg`,
   `outdoors-01.jpg`, `outdoors-02.jpg`, `outdoors-03.jpg`, `outdoors-04.jpg`
2. That's it. A photo with a matching name replaces its gray placeholder automatically.
   Slots without a photo keep the placeholder. To swap an existing photo, save the new one with the same name.
3. The `-01` photo of each category is also used as that service's card image in the Services section.

### Add more photos than the defaults
1. Save the new file in `images/portfolio/` (e.g. `portraits-03.jpg`).
2. In `index.html`, find the `<div class="grid" id="gallery">` section and copy a whole
   `<figure class="item" data-cat="portraits"> ... </figure>` block.
3. Paste it inside the same grid, then change:
   - `data-cat` to one of: `portraits`, `graduation`, `pets`, `realestate`, `outdoors`
   - the `<img src="images/portfolio/portraits-03.jpg">` file name and its `alt` text
   - the caption text inside `<figcaption>`
4. Optional: use `class="item wide"` to make a landscape photo span two columns.

### Photo tips
- Resize before uploading: about 1600 px on the long edge, JPEG quality 80-85. Full-size camera files make the site slow.
- Write a short, descriptive `alt` text for each photo (helps accessibility and search).
- Use lowercase file names with no spaces.

## Publishing changes
From this folder:

    git add .
    git commit -m "Add new portfolio photos"
    git push

If you host on GitHub Pages, Netlify, or Cloudflare Pages, the live site updates automatically after the push.
