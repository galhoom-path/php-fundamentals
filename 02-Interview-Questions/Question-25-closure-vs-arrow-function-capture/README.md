# Question 25 - How do anonymous functions and arrow functions capture outside variables?

Status: Not completed
Related lecture: Lecture 16
Folder: `02-Interview-Questions/Question-25-closure-vs-arrow-function-capture/`

## Interview Question

How do anonymous functions and arrow functions capture outside variables?

## What The Interviewer Is Testing

Whether you understand capturing by value, by reference, and automatically.

## A Strong Answer Should Cover

- An anonymous function sees outside variables only when they are listed in `use`, captured by value at creation time.
- `use (&$var)` captures by reference, so changes are shared.
- An arrow function `fn() =>` captures outside variables automatically by value and contains a single expression.

## Practice Task

Predict the output when `$rate` changes after creating a closure with `use ($rate)` and an arrow function using `$rate`.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/functions.anonymous.php, https://www.php.net/manual/en/functions.arrow.php
