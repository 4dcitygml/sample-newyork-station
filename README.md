# Grand Central Building Data (Practice Repository)

<!-- practice-repo-template: README for the 4dcitygml demo repo
sample-newyork-station. CityGML for the Grand Central area published as a
manually reset practice environment. Not a production city deployment — a
learning ground for the tools, the PR flow, and collaborative data upkeep. -->

Building data (CityGML) for the Grand Central Terminal area, collaboratively
maintained via pull requests. **This is a practice repository that is reset
manually when needed** — designed for learning the editing workflows and tools before
contributing to production city data.

- **Get started (practice):** download the
  [starter kit](https://github.com/4dcitygml/sample-newyork-station/releases/download/starter-kit/newyork-station-starter.zip),
  unzip it, and double-click `start-mac.command` (macOS) or `start-windows.bat`
  (Windows). The shared editing tool is downloaded automatically and connects to
  this city; you do not need to clone the repository (the tool creates your own copy).
  Step by step, including working with Git directly: [Getting started](docs/getting-started.md).
- **Data source & license:** see `4dcitygml.json` (`attribution` / `license`).
  NYC 3D Building Massing Model — NYC Office of Technology and Innovation
  (DoITT), NYC Open Data.
- **Building ID:** the NYC BIN is used when assigned. The upstream placeholder
  `1000000` is not treated as an identifier; those three buildings fall back to
  their unique source `gml:id` without modifying the source data.
- **Look & feel:** `theme.json` (declarative tokens only; changes go through PR
  review).
- **City logo (optional):** set `logo` in `4dcitygml.json` to a raster image
  (png / jpg / jpeg / webp, ≤ 1 MiB) inside this repository; it is shown
  top-left in every tool. SVG is not accepted — an SVG opened directly can
  execute scripts, which would break the "no XSS by construction" design shared
  with themes.

## Viewing the data in a standalone viewer

If you just want to look at the CityGML without contributing, the free
Windows viewer **[KITModelViewer](https://www.iai.kit.edu/english/4561.php)**
by KIT (successor of the FZKViewer) opens
`citygml/da12_grand_central_area.gml` directly. The older
[FZKViewer](https://www.iai.kit.edu/english/1648.php) (development ended at
6.3) also displays it. The file has no textures, so downloading the single
GML file is enough.

To edit attributes and propose changes, use the shared editing tool (see
"Get started" above).

## Practice Environment

The daily reset and automatic merge are currently **disabled**. This repository
is a sandbox for practicing the editing tools and PR workflows with maintainer
review, without affecting production data.

- **Manual reset:** only a maintainer can reset `main` to `baseline`, after
  entering the confirmation word `RESET`. Open pull requests receive guidance
  when a reset is performed.
- **Manual merge:** every pull request is checked by the maintainer before it is
  merged. The auto-merge implementation is retained for future review, but it
  does not start while its dedicated repository variable is unset.
- **After each reset, sync your fork:** If you have a fork of this repository,
  click **Sync fork** → **Update branch** on GitHub before your next practice
  session. Otherwise, edits you made before the reset (which were wiped from
  `main`) would appear in your next PR's diff and be rejected by the
  commit-scope check.
  - **If you use the official editing tools:** This sync is automatic every time
    you start a tool. You do not need to manually sync via GitHub.

## Transparency Notice

Practice pull requests, reviews, and CI comments remain in the normal public
GitHub history. Collection in a separate practice-log repository is not enabled
in the current operation. Include only information that may be made public in
pull requests and comments.

---

CityGML is a standard of the Open Geospatial Consortium (OGC). This project is
not affiliated with or endorsed by OGC.
