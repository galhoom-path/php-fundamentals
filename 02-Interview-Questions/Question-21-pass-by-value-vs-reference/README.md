# Question 21 - What is the difference between passing by value and passing by reference?

Status: Not completed
Related lecture: Lecture 14
Folder: `02-Interview-Questions/Question-21-pass-by-value-vs-reference/`

## Interview Question

What is the difference between passing by value and passing by reference?

## What The Interviewer Is Testing

Whether you can predict whether a function changes the caller's variable.

## A Strong Answer Should Cover

- By default, PHP passes a copy of the value; changes inside the function do not affect the caller.
- With `&$param`, the function receives a reference and changes the original variable.
- References make code harder to follow; returning a new value is usually clearer.

## Practice Task

Write the same "add item to cart" function by value (returning the array) and by reference, and compare them.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.references.pass.php
