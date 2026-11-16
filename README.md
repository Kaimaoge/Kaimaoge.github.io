# Yuankai Wu — Academic homepage

Personal academic website published at https://kaimaoge.github.io/ by GitHub Pages from the `wkm改` branch.

## Pages

- `index.html`: biography, research interests, selected news and publications, funding, students, and contact.
- `students.html`: current students and alumni. `students-redirects.html` maintains personal-homepage URLs; incomplete URLs return to the matching roster card.
- `teaching.html`: courses.
- `cv.html`: CV viewer, using `assets/pdf/cv.pdf`.
- `news.html`, `publications.html`, `projects.html`, `people.html`: preserved historical content, with the same visual style as the main pages.
- `cv-redirect.html`: GitHub Pages/Jekyll generates `/CV.html` for old links. This avoids the previous `CV.html` / `cv.html` filename collision on macOS and Windows.
- `talks.html`: existing compatibility redirect to the homepage.

## Assets and maintenance

`assets/css/styles.css` is the single shared stylesheet. `assets/img/` contains only images used by the current pages. `Images/202206.pdf` and `Images/202305.pdf` are preserved historical slides; `assets/pdf/cv.pdf` is the canonical CV.

Edit page content directly in HTML. Update both `index.html` and `publications.html` when adding a publication to both the selected list and the archive. The ALETHEIA entry uses the author list and conference information from https://arxiv.org/abs/2611.11252; its thumbnail is Figure 2 from that paper. Code and dataset links point to the authors' repository.

To configure a student's homepage, replace their value in the `mapping` object in `students-redirects.html` with a full `https://` URL. Leave it as `#` until a real address is available.

## Local preview

No dependency installation or application build is required:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000/. GitHub Pages processes only the front matter in `cv-redirect.html` to produce the uppercase compatibility URL; the canonical lowercase CV works in the local static preview.

## Cleanup

The visual refresh retains all original page text, research records, student information, courses, historical external links, and the two distinct slide PDFs. It adds the NeurIPS 2026 ALETHEIA paper and corrects leftover template browser titles.

Removed: unreferenced template illustrations/avatars, duplicate PDFs, the unused old portrait/icons, empty files, and the retired `style.css` / `table_header.js` layout. The main portrait is a compressed WebP of the same photograph. Old Google Analytics template code and a broken script that guessed publication image names have been removed. Deleted files remain recoverable from Git history; history has not been rewritten.
