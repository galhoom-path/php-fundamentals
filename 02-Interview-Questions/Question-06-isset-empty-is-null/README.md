# Question 06 - What is the difference between isset(), empty(), and is_null()?

Status: Not completed
Related lecture: Lecture 4
Folder: `02-Interview-Questions/Question-06-isset-empty-is-null/`

## Interview Question

What is the difference between isset(), empty(), and is_null()?

## What The Interviewer Is Testing

Whether you can safely check missing, null, and empty values without warnings.

## A Strong Answer Should Cover

- `isset()` is true when a variable exists and is not `null`; it never warns for undefined variables.
- `empty()` is true for missing values and for "falsy" values such as `0`, `"0"`, `""`, `[]`, and `null`.
- `is_null()` checks only for `null` and warns if the variable is undefined.

## Practice Task

Build a small table for the values `0`, `""`, `"0"`, `null`, and `[]` showing the result of each check.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/types.comparisons.php
