# Question 36 - How do you protect a PHP session from hijacking and fixation?

Status: Not completed
Related lectures: Lectures 24, 25
Folder: `02-Interview-Questions/Question-36-session-security/`

## Interview Question

How do you protect a PHP session from hijacking and fixation?

## What The Interviewer Is Testing

Whether you know the basic session hardening steps.

## A Strong Answer Should Cover

- Regenerate the session ID with `session_regenerate_id(true)` after login and privilege changes.
- Configure the session cookie with `httponly`, `secure`, and `samesite`, and use HTTPS.
- Destroy the session completely on logout.

## Practice Task

List the steps your login and logout code must perform to keep the session safe.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/session.security.php
