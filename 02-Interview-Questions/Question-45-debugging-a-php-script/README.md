# Question 45 - How do you debug a PHP script that does not work as expected?

Status: Not completed
Related lecture: Lecture 30
Folder: `02-Interview-Questions/Question-45-debugging-a-php-script/`

## Interview Question

How do you debug a PHP script that does not work as expected?

## What The Interviewer Is Testing

Whether you debug with a method instead of guessing.

## A Strong Answer Should Cover

- Read the full error message and line number first; PHP 8.5 adds a backtrace to fatal errors.
- Inspect values with `var_dump()` / `print_r()` and write messages to a log with `error_log()`.
- Reproduce the problem with a small input and confirm the fix with `assert()` checks.

## Practice Task

Describe your step-by-step process for a form that saves nothing and shows no error.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.var-dump.php, https://www.php.net/manual/en/function.error-log.php, https://www.php.net/manual/en/function.assert.php
