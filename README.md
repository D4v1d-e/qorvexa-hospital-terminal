# QORVEXA HOSPITAL TERMINAL

One offline HTML file: the QORVEXA Health Technologies platform — laboratory network directory, interactive 3D
anatomy and laboratory environments, grounded site search, learning center and a device-local member workspace.

Live preview: https://d4v1d-e.github.io/qorvexa-hospital-terminal/

## What is in it

| Area | Contents |
|---|---|
| Centers | 4: Advanced Medical Research · Human Body & Medical Sciences · Diagnostics & Laboratory Science · AI Biomedical Research |
| Laboratory pages | 40, each on the same seven-section structure |
| Seven sections | Scope and importance · Departments · Equipment and models · Interactive 3D · Scientific library · Learning center · Research and publications |
| 3D model library | 20 entries: 18 rotatable in the viewer, 2 labelled reference renders |
| Search | Site-wide nav search, directory search bar, per-laboratory scoped field; results grouped by type and illustrated |
| Learning | Teaching cases, interactive activities, progress tracking, grounded Q&A over the site's own notes |
| Index | 626 documents, 217 with an illustration |

## How to run it

Open `index.html` in any modern browser. No install, no build step, no network connection.

The file is self-contained: 0 external `src` or `href`, 0 stylesheets links, 0 `fetch`/XHR, 26 images embedded as
`data:` URIs, about 1.69 MB. `file://` works, so it runs on a machine that is offline permanently.

## Data and privacy

- Everything is stored in the visitor's own browser (`localStorage`). There is no server, no account system and no
  analytics collection anywhere.
- Visitor search history (the phrases they typed, with revisit and clear) and administrator search analytics (counts,
  no-result queries, click-through, content gaps) are separate screens. Analytics opens only after the workspace
  sign-in on that device.
- Analytics figures are real counts from the device being viewed. No traffic numbers are invented.
- Clearing member data removes the local record and nothing else.

## No patient information

All clinical content is educational text about laboratory science. Teaching cases are labelled as simulations, not
medical advice, and do not describe real people. There are no names, identifiers, results or notes of any actual
patient in this repository.

## Repository layout

- `index.html` — the whole site
- `README.md` — this file

## Not medical advice

QORVEXA is presented here as a research and teaching platform. Nothing in this repository diagnoses, treats or
monitors any condition, and none of it should be used in place of a qualified clinician.
