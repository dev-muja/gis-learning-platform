# ATLAS — GIS Learning Platform

A responsive Arabic/English static learning site for GIS and CAD integration,
designed for a computer science graduate learning information systems analysis.

## Run

Open this folder in VS Code, install Live Server and select **Open with Live Server**
on `index.html`. No Node.js, database or build step is needed. Direct `file://`
opening may block JSON loading.

## Publish on GitHub Pages

Repository Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save.
All application paths are relative to support project-site hosting.

## Content

- `content/ar/chapters.json` and `content/en/chapters.json`: 10 chapters per language.
- `content/*/glossary.json`: terminology. Update this separately if you add terms.
- `content/*/resources.json`: curated sources, access notes and categories.
- `js/app.js`: navigation, diagrams, quizzes, project plan and backup controls.
- `css/styles.css`: responsive RTL/LTR layout and print styles.
- `assets/training/`: synthetic DXF, PRJ, GeoJSON, CSV templates and data notes.

To extend a chapter, add `{ "title": "…", "body": "…" }` to `sections` in both
languages. Keep chapter identifiers synchronized. The present course has 10
chapters; adding whole chapters also requires updating progress totals and
navigation limits in `app.js` and `index.html`.

## Privacy and dependencies

Completion and notes use browser localStorage with JSON backup/restore. No
accounts, database, analytics or server submission. Google Fonts is optional;
system fonts are used when it is unavailable. External resources open on their
publishers' websites. All diagrams are original inline SVG, with accessible names.

## Scope and source notes

Educational prototype, not a certification course, production GIS, real survey
or official Esri/Autodesk/QGIS product. The lesson copy is original educational
explanation. Linked official documentation is authoritative for version-specific
behavior and licensing. Resource review date: 2026-10-29. Free learning content
does not imply free software, certificates or unrestricted educational licenses.

The one-week GIS project is completed separately in GIS software. The website
provides lessons and sample data; its buffer illustration is not a GIS engine.
