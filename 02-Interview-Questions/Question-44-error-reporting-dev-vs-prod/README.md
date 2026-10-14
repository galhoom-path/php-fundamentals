# Question 44 - How do you configure error reporting for development and for production?

Status: Not completed
Related lecture: Lecture 30
Folder: `02-Interview-Questions/Question-44-error-reporting-dev-vs-prod/`

## Interview Question

How do you configure error reporting for development and for production?

## What The Interviewer Is Testing

Whether you show errors to developers but never to visitors.

## A Strong Answer Should Cover

- In development: `error_reporting(E_ALL)` and `display_errors=On` so every problem is visible.
- In production: keep `E_ALL` but set `display_errors=Off` and `log_errors=On` with an `error_log` file.
- Showing errors to visitors can leak paths, queries, and secrets.

## Practice Task

Write the `php.ini` lines for development and for production.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/errorfunc.configuration.php
