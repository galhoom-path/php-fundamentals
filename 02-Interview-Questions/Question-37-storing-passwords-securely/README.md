# Question 37 - How should you store user passwords in PHP?

Status: Not completed
Related lecture: Lecture 25
Folder: `02-Interview-Questions/Question-37-storing-passwords-securely/`

## Interview Question

How should you store user passwords in PHP?

## What The Interviewer Is Testing

Whether you use modern hashing instead of encryption or fast hashes.

## A Strong Answer Should Cover

- Never store plain text, and never use `md5()` or `sha1()` for passwords.
- Use `password_hash($password, PASSWORD_DEFAULT)` and verify with `password_verify()`.
- Use `password_needs_rehash()` to upgrade old hashes when the algorithm or cost changes.

## Practice Task

Describe the registration and login flow using the three password functions.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.password-hash.php, https://www.php.net/manual/en/function.password-verify.php
