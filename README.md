# Engineering Portfolio — Starter Site

A blank, plain HTML/CSS/JS portfolio site. No build tools, no
frameworks, no installs required — open the files in a browser or
a code editor and start editing.

## Folder structure

```
engineering-portfolio/
├── index.html                 Homepage: contact info + clickable project grid
├── projects.html              All projects as quick-read paragraph summaries
├── resume.html                Résumé as a webpage (optional PDF download button)
├── projects/
│   ├── project-template.html  Blank template — duplicate this for new projects
│   ├── project-01.html        Sample project page (edit or delete)
│   └── project-02.html        Sample project page (edit or delete)
├── assets/
│   ├── css/style.css          All styling — one file, heavily commented
│   ├── js/main.js             Mobile nav toggle + active-link highlight
│   └── images/projects/       Put your project photos here
└── resume/
    └── (optional: put resume.pdf here for the download button)
```

## Site map

- **Home** (`index.html`) — lands here first. Contact info sits right
  below the nav bar, then a grid of project cards (photo, title,
  skills used). Clicking a card opens that project's full page.
- **Projects** (`projects.html`) — the same projects, but as short
  paragraphs so someone can read the whole thing without clicking
  through. Each entry also links to the same full project page.
- **Résumé** (`resume.html`) — your résumé as an actual webpage
  (summary, experience, education, skills), with an optional
  "Download as PDF" button if you keep a PDF version too.
- **Project pages** (`projects/project-*.html`) — one page per
  project with a hero image, overview, gallery, and prev/next links
  to the other projects.

## How to view the site

There's no server or build step needed. Just open `index.html` in a
web browser. Links between pages use relative paths, so the folder
structure needs to stay intact (don't move files out of `/projects/`
or `/assets/` individually).

## Adding text and images

- Every spot meant for your own content is marked with an
  `EDIT ME` comment in the HTML.
- Photo spots are dashed boxes (`<div class="img-placeholder">`)
  with a suggested filename and size right on them. Once you have a
  photo, delete the placeholder `<div>` and replace it with a plain
  `<img src="..." alt="...">` tag — see `assets/images/projects/PUT_IMAGES_HERE.txt`
  for exact instructions and naming suggestions.
- If you want a downloadable PDF résumé too, put it at
  `/resume/resume.pdf` — see `resume/PUT_RESUME_HERE.txt`. The button
  on `resume.html` already points there.

## Adding a new project page

A new project needs to be added in **three** places so it shows up
everywhere consistently:

1. Copy `projects/project-template.html` and rename it, e.g.
   `projects/project-03.html`. Fill in every `EDIT ME` spot: title,
   spec strip (role/tools/timeline/team), overview text, and images.
   Update the "prev / next" links at the bottom to connect it to the
   projects next to it in your list.
2. Open `index.html`, duplicate one `<a class="project-card">` block
   in the "Projects" grid, and point it at your new file. Update the
   thumbnail placeholder and the skills tags.
3. Open `projects.html`, duplicate one `<article class="project-entry">`
   block, point it at the same new file, and write the paragraph
   summary.

No rebuild step needed for any of this — just save and refresh the
browser.

## Editing styles (colors, fonts, spacing)

Everything is controlled from the top of `assets/css/style.css`,
inside the `:root { ... }` block. Change a value there (a color hex
code, a font name, a spacing size) and it updates across every page,
since all pages share this one stylesheet.

## Editing the nav bar or footer

The nav bar ("hot bar") and the title-block footer are repeated at
the top/bottom of every page: Home, Projects, and Résumé. If you add
another top-level page later, update the `<nav>` block on every page
to match.
