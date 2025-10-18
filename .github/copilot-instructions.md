This repository is a small static website (HTML-only) for an NGO project. The goal of these instructions is to help AI coding assistants be immediately productive.

- Project layout (important files):
  - `index.html` — main landing page (Portuguese content, navigation links to other pages).
  - `cadastro.html` — volunteer/user registration form (simple HTML form, no backend wired).
  - `projeto.html` — project details page (currently empty — treat as a placeholder to add static content).
  - `README.md` — minimal project title.

- Big picture / architecture:
  - Pure static site: no server-side code, no build system, and no package manager files. Edits should preserve plain HTML structure.
  - Static assets (images) are referenced by relative paths (see `index.html` referencing `imagens/cachorro.jpg`). Create an `imagens/` folder for new images and reference them with relative paths.

- Developer workflows / quick commands:
  - No build or test runner. Preview changes by opening files in a browser or using an editor Live Server.
  - Quick local HTTP server (PowerShell): `python -m http.server 8000` (run from project root) then open `http://localhost:8000/index.html`.

- Project-specific conventions and patterns:
  - Language: `index.html` uses `lang="pt-BR"`. Prefer Portuguese for new content unless adding a separate English page.
  - Header/Nav: keep the simple header/nav structure (links to `index.html`, `projeto.html`, `cadastro.html`) consistent across pages.
  - Forms: `cadastro.html` uses a static `<form action="#" method="post">`. There is no backend; if adding client-side behavior, use vanilla JS and localStorage or clearly document backend wiring.

- Integration points / external dependencies:
  - None detected (no external scripts, no CDN). Assume no frameworks and avoid adding build tooling unless requested.

- Safe edit examples (concrete):
  - Populate `projeto.html` by copying the DOCTYPE/head/body from `index.html` and adding content within `<main>` using the same header/footer.
  - Add client-side validation to `cadastro.html`: validate `email` and `telefone` with plain JS, keep code unobtrusive (either inline at the end of the body or in a new `scripts/` folder).
  - Add images to `imagens/` and reference them like `<img src="imagens/voluntarios.jpg" alt="...">`.

- Small PR ideas an AI agent can prepare:
  - Create a `projeto.html` skeleton with sections "O Projeto", "Como Ajudar", and "Galeria".
  - Add basic JS form validation to `cadastro.html` (happy path + minimal error messages). Use only vanilla JS.
  - Add `imagens/README.md` describing filename conventions (lowercase, hyphens preferred).

- Constraints / don'ts:
  - Do not introduce bundlers, package.json, or other build tooling unless converting the repo intentionally—ask first.
  - Preserve existing filenames and relative links when renaming or moving pages.

If you want, I can implement one of the small PR examples (populate `projeto.html` or add form validation). Tell me which and I'll create the changes and a short test/preview instruction.
This repository is a small static website (HTML-only) for an NGO project. The goal of these instructions is to help AI coding assistants be immediately productive.

- Project layout (important files):
  - `index.html` — main landing page (Portuguese content, navigation links to other pages).
  - `cadastro.html` — volunteer/user registration form (simple HTML form, no backend wired).
  - `projeto.html` — project details page (currently empty — treat as a placeholder to add static content).
  - `README.md` — minimal project title.

- Big picture / architecture:
  - This is a pure static site (no server-side code, no build system, no package manager files). Edits should preserve plain HTML structure.
  - Static assets (images) are referenced from relative paths (e.g., `imagens/cachorro.jpg` from `index.html`). When adding assets, place them in an `imagens/` folder and reference with relative paths.

- Developer workflows / quick commands:
  - No build/test steps required. To preview changes, open the HTML files in a browser (double-click or use an editor Live Server extension).
  - On Windows PowerShell, a quick preview can be served with a simple Python HTTP server if needed:
    - `python -m http.server 8000` (run from the project root) and open `http://localhost:8000/index.html` in a browser.

- Project-specific conventions and patterns:
  - Language: main site content uses Portuguese (`index.html` uses `lang="pt-BR"`). Keep new copy consistent in language unless adding an English page intentionally.
  - Navigation: `index.html` contains a simple header nav linking to `index.html`, `projeto.html`, and `cadastro.html`. Maintain these filenames and relative links when renaming or moving pages.
  - Forms: `cadastro.html` has a static form (`action="#"`, method `post`). There is no backend; if implementing client-side validation or storage, do so with vanilla JS and localStorage, or document where server wiring is expected.

- Integration points / external dependencies:
  - None detected in the repository (no CDN references, no external scripts). Assume no JS frameworks or build tooling.

- How to make safe edits (examples):
  - To add content to `projeto.html`, copy the structure from `index.html` or `cadastro.html` (doctype, head, and body) and place content in the `<main>` section. Keep header and footer structure consistent across pages.
  - To add an image: create `imagens/` if missing, add the file (e.g., `imagens/voluntarios.jpg`) and use `<img src="imagens/voluntarios.jpg" alt="...">`.
  - To wire a contact form to a backend later, preserve input `name` attributes (`nome`, `email`, `telefone`) and change the `form action` to the endpoint; document the change in `README.md`.

- Examples of desirable small PRs an AI assistant can prepare:
  - Populate `projeto.html` with sections: "O Projeto", "Como Ajudar", and "Galeria" using the same header/footer layout.
  - Add basic client-side form validation in `cadastro.html` using unobtrusive vanilla JS (validate email format and phone length). Keep scripts inline or add a new `scripts/` folder.
  - Add an `imagens/README.md` to document the filename conventions (lowercase, hyphens, forward slashes).

- Constraints and what not to change:
  - Do not introduce build tools (webpack, npm, etc.) unless converting the site to a different architecture—ask for approval first.
  - Preserve existing filenames and relative links unless also updating all references.

If anything here is unclear or you'd like additional examples (for example, a sample `projeto.html` skeleton or a small JS validation snippet), tell me which section to expand and I will iterate.
