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

## Opening screens

| Screen | Behaviour |
|---|---|
| Intro | Plays once per visit: a progress bar that reports how many of the 26 embedded renders have actually decoded |
| Skip | "Skip intro" ends the intro immediately; the bar still reflects real decode work |
| Gate | After the intro, a Sign In screen covers the site and the page behind it is `inert` (keyboard cannot reach it) |
| Sign In | Opens the workspace stored on this device; verified against a salted SHA-256 hash, the passphrase is never stored |
| Create account | Sets a name and passphrase on this device only, then enters the workspace |
| Continue as guest | Browses the whole site without touching the stored workspace or its identity |
| Remember me | Keeps the sign-in across browser restarts; off, the sign-in ends when the tab closes |
| SSO buttons | Google and Microsoft explain that single sign-on needs a server this offline file does not have, then offer local sign-in or guest |
| Forgot password | Explains that no recovery exists because nothing leaves the device, and offers a fresh workspace or guest entry |

The gate can be raised again from the avatar control (Sign out). "Clear this device" removes the workspace, the hash
and every local record after a confirmation.

## Chrome

| Element | Behaviour |
|---|---|
| Header | Two fixed tiers above 1150px (identity row, then the section rail); one tier plus an openable menu below it |
| Rail groups | Each group opens its own panel; hover and keyboard both work, `Esc` closes, nothing slides sideways |
| Home | Wordmark, BODYVERSE figure, six real feature cards, a Quick Access rail, an Impact rail and an on-device rail |
| Status bar | Reports the offline build, the file's own timestamp, a live local-storage write test and a running clock |
| Bell | Lists the pages actually opened, the searches actually run and the drafts actually prepared on this device |

## Reading modes

| Mode | Behaviour |
|---|---|
| One scrolling page | Default on a wide pointer device: every section on one page, the rail tracks the section in view |
| One section per page | Default on narrow or touch screens: each tap replaces the screen, with a breadcrumb and Back/Next |
| Switch | The control in the page bar changes mode and the choice is remembered on that device |

## How to run it

Open `index.html` in any modern browser. No install, no build step, no network connection.

The file is self-contained: 0 external `src` or `href`, 0 stylesheets links, 0 `fetch`/XHR, 26 images embedded as
`data:` URIs, about 1.79 MB. `file://` works, so it runs on a machine that is offline permanently.

Every figure on the home rails and in the menus is counted from the data inside the file at load time. None of it is
typed into the markup.

## Data and privacy

- Everything is stored in the visitor's own browser (`localStorage`). There is no server, no account system and no
  analytics collection anywhere.
- The workspace passphrase is kept as a salted SHA-256 digest produced by Web Crypto; the text is never written down.
  Where the browser withholds Web Crypto, sign-in says so instead of pretending.
- Sign-in identity follows the session record, so a guest never inherits the stored workspace name.
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
