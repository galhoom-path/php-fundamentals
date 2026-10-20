# Map 11 - Forms, Validation, and Escaping

Status: Not completed
Related lectures: Lecture 22, Lecture 23
Folder: `03-Visual-Maps/Map-11-forms-validation-escaping/`
Diagram kind: sequence

## What To Show

Sequence a form POST: browser → PHP reads `$_POST` → validate → either re-display errors or redirect (PRG). Mark where every output value is escaped with `htmlspecialchars` / `e()`.

## CHECK

Explain the diagram out loud in under two minutes without reading every label.
Also open `map.md` on GitHub: the Mermaid must render as a clear, readable SVG.

## Files

- `map.md` — your Mermaid diagram (must look good on GitHub).
- `notes.md` — optional short reflection.

## Completion Rule

After the diagram is accurate, renders cleanly on GitHub, and you pass the CHECK, mark this map with ✅ in `../README.md`.

Sources: https://www.php.net/manual/en/tutorial.forms.php, https://www.php.net/manual/en/function.htmlspecialchars.php, https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms
