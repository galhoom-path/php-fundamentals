# Question 34 - How do you validate user input in PHP?

Status: Not completed
Related lecture: Lecture 23
Folder: `02-Interview-Questions/Question-34-validating-user-input/`

## Interview Question

How do you validate user input in PHP?

## What The Interviewer Is Testing

Whether you check input shape and meaning before using it.

## A Strong Answer Should Cover

- Never trust input from `$_GET`, `$_POST`, cookies, or files.
- Use `filter_var()` with filters such as `FILTER_VALIDATE_EMAIL` and `FILTER_VALIDATE_INT`, plus your own business rules.
- Collect errors, reject invalid data, and show clear messages instead of silently "fixing" input.

## Practice Task

Validate an age field so it accepts only whole numbers from 18 to 99.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/filter.filters.validate.php
