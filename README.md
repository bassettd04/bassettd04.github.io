# bassettd04.github.io

The personal portfolio website of **Daniel Bassett**, a final-year mechanical engineering student at the University of Southampton. It shows my engineering projects, experience and technical skills.

**Live site:** https://bassettd04.github.io/

## What's on the site

- **Featured projects.** Each project opens a detail view with an image and video gallery, a summary, key highlights and, where available, a link to the full report.
  - Arduino Sound-Seeking Robot (embedded systems, C++, signal processing)
  - Formula Student Bodywork Manufacturing (CAD, composites, manufacturing)
  - Aluminium Alloy Research Project (materials science, vacuum design, testing)
  - Vibration Analysis of an Electron Beamline (STFC placement, Python, experimental methods)
- **About & experience.** Background, the STFC industrial placement and Formula Student leadership roles.
- **Technical toolkit.** Mechanical/design and software/hardware skills.
- **CV and contact.** A downloadable CV plus links to email, LinkedIn and GitHub.

## How it's built

It's a single static page with no build step:

| File | Purpose |
| --- | --- |
| `index.html` | All markup, styles and the small script that drives the project filter and detail view |
| `Assets/resume.pdf` | CV linked from the header |
| `Assets/<project>/` | Images, videos and PDFs for each project |

Fonts come from Google Fonts (Archivo) and icons from Font Awesome via cdnjs. GitHub Pages serves the `main` branch directly.

## Running locally

Any static file server works. For example, from the repo root:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Adding or editing a project

Project details live in the `projectData` object near the bottom of `index.html`. To add one:

1. Put its media in a new folder under `Assets/`.
2. Add an entry to `projectData` with a `title`, `tags`, `images` (each with a `url` and `caption`; `.mp4` files play as video), `summary`, `highlights` and an optional `link` to a report.
3. Add a matching row in the projects list with `data-project="<key>"` and a `data-group` of `software` or `mechanical` so the filter picks it up.

## Contact

- Email: danielbassett1706@gmail.com
- LinkedIn: https://www.linkedin.com/in/daniel-bassett-5aa94621b/
- GitHub: https://github.com/bassettd04
