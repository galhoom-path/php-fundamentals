# Question 07 - What is the difference between == and ===?

Status: Not completed
Related lecture: Lecture 5
Folder: `02-Interview-Questions/Question-07-loose-vs-strict-comparison/`

## Interview Question

What is the difference between == and ===?

## What The Interviewer Is Testing

Whether you understand loose comparison with conversion versus strict comparison of value and type.

## A Strong Answer Should Cover

- `==` converts types when needed and then compares values.
- `===` compares both value and type without any conversion.
- Prefer `===` by default to avoid surprises such as `"1" == "01"` being true.

## Practice Task

Predict the result of `0 == "0"`, `0 === "0"`, `"1" == "01"`, and `null == false`.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.operators.comparison.php
