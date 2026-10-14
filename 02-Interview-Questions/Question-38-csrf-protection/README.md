# Question 38 - What is CSRF, and how do you protect a form against it?

Status: Not completed
Related lecture: Lecture 25
Folder: `02-Interview-Questions/Question-38-csrf-protection/`

## Interview Question

What is CSRF, and how do you protect a form against it?

## What The Interviewer Is Testing

Whether you understand forged requests and token-based protection.

## A Strong Answer Should Cover

- CSRF tricks a logged-in user's browser into sending a request the user did not intend.
- Protect forms with a secret random token stored in the session and sent as a hidden field.
- Compare tokens with `hash_equals()`, accept changes only via POST, and use `SameSite` cookies as extra defense.

## Practice Task

Describe how an attacker could delete a booking without CSRF protection and how the token stops it.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html
