# Question 12 - Why should you use mb_* functions for non-English text?

Status: Not completed
Related lecture: Lecture 8
Folder: `02-Interview-Questions/Question-12-why-mb-string-functions/`

## Interview Question

Why should you use mb_* functions for non-English text?

## What The Interviewer Is Testing

Whether you understand bytes versus characters in UTF-8 text.

## A Strong Answer Should Cover

- Normal string functions such as `strlen()` and `substr()` count bytes, not characters.
- In UTF-8, Arabic and many other letters use more than one byte, so byte-based functions give wrong lengths or broken text.
- `mb_strlen()`, `mb_substr()`, and similar functions work with real characters.

## Practice Task

Explain why `strlen("مرحبا")` is not 5 and which function returns 5.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/book.mbstring.php
