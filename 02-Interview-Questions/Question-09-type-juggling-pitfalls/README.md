# Question 09 - What is type juggling, and which bugs can it cause?

Status: Not completed
Related lecture: Lecture 6
Folder: `02-Interview-Questions/Question-09-type-juggling-pitfalls/`

## Interview Question

What is type juggling, and which bugs can it cause?

## What The Interviewer Is Testing

Whether you can predict automatic conversions and protect code from them.

## A Strong Answer Should Cover

- Type juggling is PHP converting a value to another type automatically depending on the context.
- It can cause bugs in comparisons, arithmetic with numeric strings, and boolean checks of values like `"0"`.
- Use strict comparison, explicit casts, and validation to control conversion (strict type declarations come in the OOP repo).

## Practice Task

Show one example where automatic conversion gives an unexpected result and fix it.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.types.type-juggling.php
