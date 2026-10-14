# Question 31 - What are superglobals?

Status: Not completed
Related lecture: Lecture 21
Folder: `02-Interview-Questions/Question-31-what-are-superglobals/`

## Interview Question

What are superglobals?

## What The Interviewer Is Testing

Whether you know where request data lives in PHP and that it is untrusted.

## A Strong Answer Should Cover

- Superglobals are built-in arrays available in every scope, such as `$_GET`, `$_POST`, `$_SERVER`, `$_SESSION`, `$_COOKIE`, and `$_FILES`.
- PHP fills them automatically for each request.
- Values that come from the user must always be treated as untrusted input.

## Practice Task

Name the superglobal you would read for: a query string value, the request method, an uploaded file, and a logged-in user ID.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.variables.superglobals.php
