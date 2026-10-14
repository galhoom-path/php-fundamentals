# Question 33 - How do you prevent XSS in PHP?

Status: Not completed
Related lecture: Lecture 23
Folder: `02-Interview-Questions/Question-33-preventing-xss/`

## Interview Question

How do you prevent XSS in PHP?

## What The Interviewer Is Testing

Whether you escape output in the right place and with the right settings.

## A Strong Answer Should Cover

- XSS happens when untrusted data is printed into a page and runs as script code in another user's browser.
- Escape every output with `htmlspecialchars($value, ENT_QUOTES, 'UTF-8')`, usually through one small helper.
- Validation on input is not enough: escape on output, in the context where the value is printed.

## Practice Task

Show how a comment containing `<script>` breaks a page, then fix the output line.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.htmlspecialchars.php, https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html
