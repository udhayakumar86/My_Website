# Copilot Instructions for this Project

This repository is a small static website composed of standalone HTML pages and CSS files. The guidance below helps an AI coding agent be productive immediately when editing or extending the project.

**Quick Project Summary:**
- **Type:** Static HTML/CSS site (no build tools, no package.json, no server-side code).
- **Key files:** Menu.html, sb1.html, rewards.html, Me.css, Re.css, sb1.css (top-level HTML/CSS files). Example: `Menu.html` is a main navigation page linking to other pages.

**Primary goals for contributors/agents:**
- Edit or add static pages that follow existing structure and naming conventions.
- Keep CSS in existing files rather than creating multiple fragmented stylesheets unless clearly necessary.

**Project-specific patterns & conventions**
- Pages are standalone HTML — prefer modifying the closest HTML file (e.g., update `rewards.html` to change rewards content).
- CSS is global and shared by pages. Use existing class names and follow the style used in `Me.css` and `sb1.css` to match site-wide appearance.
- Filenames are case-sensitive on some hosts; do not rename files unless updating all references.

**Editing guidance & examples**
- To add a new page, create `newpage.html` in the repo root and link it from `Menu.html` using a relative `<a href="newpage.html">`.
- To change navigation text, edit the list in `Menu.html` (look for `<nav>` or visible links). Example: change link label in the `<li><a>` element.
- To update styles, append rules to the relevant CSS file (e.g., add a class in `Me.css` and then apply it in the target HTML).

**Testing & verification (how to preview changes)**
- No build step required — open the edited HTML file in a browser to view changes. In VS Code, use the Live Server extension or double-click the file in Explorer.
- On Windows development machines, open the file via the file path (e.g., `e:\project\Menu.html`) or use local Live Server at `http://127.0.0.1:5500/Menu.html` if available.

**What not to change without checking with maintainers**
- Do not add complex toolchains (webpack, npm, etc.) or tests; there are no existing CI hooks or package manifests.
- Avoid renaming top-level files (e.g., `sb1.html`, `Me.css`) — changing names may break links between pages.

**Commit & PR patterns**
- Small, focused commits with messages like: `fix: update rewards content in rewards.html` or `feat: add contact page contact.html`.
- Include a short description of manual verification steps in the PR body (e.g., which pages to open and what to expect).

**If you need to introduce tooling**
- Propose the change in an issue/PR first. If a build or toolchain is necessary, keep tool additions minimal and document local run steps in README.

**Where to look for examples in this repo**
- Navigation and linking pattern: Menu.html (site entry and links).
- Page + CSS pattern: sb1.html alongside sb1.css.

If any section here is unclear or you'd like additional examples (more file-level pointers or a short contributor checklist), say which parts to expand and I will iterate.
