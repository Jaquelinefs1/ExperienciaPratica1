This repository is a small static website (HTML-only) for an NGO project. The goal of these instructions is to help AI coding assistants be immediately productive.

Project layout (important files):

- `index.html` — main landing page (Portuguese content, navigation links to other pages).
- `cadastro.html` — volunteer/user registration form (simple HTML form, no backend wired).
- `projeto.html` — project details page (currently empty — treat as a placeholder to add static content).
This repository is a small static website (HTML-only) for an NGO project. The goal of these instructions is to help AI coding assistants be immediately productive.

Project layout (important files)

- index.html — main landing page (Portuguese content, navigation links to other pages)
- cadastro.html — volunteer/user registration form (simple HTML form, no backend wired)
- projeto.html — project details page (currently empty; safe placeholder for static content)
- README.md — minimal project title and repository info

Big picture / architecture

- Pure static site with only HTML files. No server code, no build system, no package.json. Keep edits to plain HTML, CSS, and small vanilla JS when needed.
- Images live in a relative folder (imagens). Example: index.html references imagens/cachorro.jpg. Create imagens/ for new assets and reference them using relative paths.

Developer workflows / quick commands

- No build steps. Preview by opening files in a browser or use an editor Live Server preview.
- Quick local HTTP server (PowerShell):
  - python -m http.server 8000
  - then open http://localhost:8000/index.html

Project-specific conventions and patterns

- Content language is Portuguese (index.html uses lang=pt-BR). Prefer Portuguese for new pages unless adding a separate English version.
- Keep the header/navigation consistent across pages: links to index.html, projeto.html, cadastro.html.
- cadastro.html contains a static HTML form; there is no backend. If adding client-side behavior, use vanilla JavaScript and localStorage. Document any change that expects a server endpoint.

Integration points / dependencies

- None found: no external scripts or CDNs. Avoid adding frameworks or build tooling unless requested.

Safe edit examples (concrete)

- Create projeto.html by copying the top-level structure (doctype, head, header, footer) from index.html and inserting content into the main element. Keep nav links unchanged.
- Add form validation to cadastro.html with simple vanilla JS (validate email pattern and phone length). Keep scripts unobtrusive and local.
- Add images to imagens/ and reference them like <img src="imagens/voluntarios.jpg" alt="voluntarios">.

Small PR ideas

- Populate projeto.html with sections: O Projeto, Como Ajudar, Galeria, plus a small local image gallery.
- Add client-side validation to cadastro.html (happy path + minimal inline error messages).
- Add imagens/README.md documenting naming rules: lowercase, hyphens, avoid spaces.

Constraints / don'ts

- Do not add package managers, bundlers, or other build tools without approval.
- Preserve filenames and relative links when renaming or moving pages.

If you'd like, I can implement one of the small PR examples now (projeto.html skeleton or form validation). Tell me which and I'll add the files and a short preview instruction.
  - This is a pure static site (no server-side code, no build system, no package manager files). Edits should preserve plain HTML structure.
