# Question 23 - How does variable scope work in PHP, and why should you avoid global?

Status: Not completed
Related lecture: Lecture 15
Folder: `02-Interview-Questions/Question-23-variable-scope-and-global/`

## Interview Question

How does variable scope work in PHP, and why should you avoid global?

## What The Interviewer Is Testing

Whether you understand that functions have their own isolated scope.

## A Strong Answer Should Cover

- Variables defined outside a function are not visible inside it, and the other way round.
- The `global` keyword or `$GLOBALS` can reach outside variables, but it creates hidden dependencies.
- Passing values as parameters and returning results keeps functions predictable and easy to test.

## Practice Task

Fix a function that reads an outside `$taxRate` with `global` by passing it as a parameter.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.variables.scope.php
