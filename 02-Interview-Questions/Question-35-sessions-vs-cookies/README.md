# Question 35 - What is the difference between sessions and cookies?

Status: Not completed
Related lecture: Lecture 24
Folder: `02-Interview-Questions/Question-35-sessions-vs-cookies/`

## Interview Question

What is the difference between sessions and cookies?

## What The Interviewer Is Testing

Whether you know where state is stored and what the user can change.

## A Strong Answer Should Cover

- HTTP is stateless: the protocol itself does not remember the previous request, so apps need cookies/sessions for continuity.
- A cookie is stored in the browser and sent with every request; the user can read and edit it.
- A session stores data on the server; the browser keeps only a session ID cookie.
- Sensitive data such as the logged-in user ID belongs in the session, never in a plain cookie.

## Practice Task

Explain where you would store a "dark mode" preference and where you would store the logged-in user ID.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources:
- https://www.php.net/manual/en/book.session.php
- https://www.php.net/manual/en/function.setcookie.php
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview
