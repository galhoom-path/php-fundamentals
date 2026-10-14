# Question 08 - What is the difference between ?? and ?: ?

Status: Not completed
Related lecture: Lecture 5
Folder: `02-Interview-Questions/Question-08-null-coalescing-vs-ternary/`

## Interview Question

What is the difference between ?? and ?: ?

## What The Interviewer Is Testing

Whether you can provide fallback values correctly and safely.

## A Strong Answer Should Cover

- `$a ?? $b` returns `$a` if it exists and is not `null`, otherwise `$b`, without warnings for missing keys.
- `$a ?: $b` returns `$a` if it is truthy, otherwise `$b`; a value like `0` or `""` falls back too.
- `??=` assigns a default only when the variable is missing or `null`.

## Practice Task

Explain which operator you would use for `$_GET['page']` and why the other one could be wrong for the value `0`.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.operators.comparison.php
