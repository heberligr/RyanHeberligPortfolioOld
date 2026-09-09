# Engineering Portfolio — Starter Site

A blank, plain HTML/CSS/JS portfolio site. No build tools, no
frameworks, no installs required — open the files in a browser or
a code editor and start editing.

## Folder structure

```
engineering-portfolio/
├── index.html                 Homepage (hero, featured work, about teaser)
├── about.html                 About me, skills, résumé link
├── projects/
│   ├── project-template.html  Blank template — duplicate this for new projects
│   ├── project-01.html        Sample project page (edit or delete)
│   └── project-02.html        Sample project page (edit or delete)
├── assets/
│   ├── css/style.css          All styling — one file, heavily commented
│   ├── js/main.js             Mobile nav toggle + active-link highlight
│   └── images/projects/       Put your project photos here
└── resume/
    └── (put resume.pdf here)
```

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
- Your résumé PDF goes in `/resume/resume.pdf` — see
  `resume/PUT_RESUME_HERE.txt`.

## Adding a new project page

1. Copy `projects/project-template.html` and rename it, e.g.
   `projects/project-03.html`.
2. Open the new file and fill in every `EDIT ME` spot: title, spec
   strip (role/tools/timeline/team), overview text, and images.
3. Update the "prev / next" links at the bottom of the new page, and
   the page(s) next to it, so the project pager chain stays correct.
4. Open `index.html`, duplicate one `<a class="project-card">` block
   in the "Featured work" section, and point it at your new file.
5. Save — no rebuild step needed, just refresh the browser.

## Editing styles (colors, fonts, spacing)

Everything is controlled from the top of `assets/css/style.css`,
inside the `:root { ... }` block. Change a value there (a color hex
code, a font name, a spacing size) and it updates across every page,
since all pages share this one stylesheet.

## Editing the nav bar or footer

The nav bar and the title-block footer are repeated at the top/bottom
of every page. If you add or rename a top-level page (not a project
page — those go through the pager instead), update the `<nav>` block
on every page to match.
