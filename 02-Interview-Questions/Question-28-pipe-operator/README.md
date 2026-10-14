# Question 28 - What is the pipe operator in PHP 8.5, and what problem does it solve?

Status: Not completed
Related lecture: Lecture 18
Folder: `02-Interview-Questions/Question-28-pipe-operator/`

## Interview Question

What is the pipe operator in PHP 8.5, and what problem does it solve?

## What The Interviewer Is Testing

Whether you know the newest PHP 8.5 language feature and its limits.

## A Strong Answer Should Cover

- `$value |> fn(...)` passes the left value into the callable on the right and returns its result.
- It replaces deeply nested calls with a readable left-to-right chain without temporary variables.
- The right side must accept one required parameter; arrow functions must be wrapped in parentheses.

## Practice Task

Rewrite `strtolower(str_replace(' ', '-', trim($title)))` with the pipe operator.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.operators.functional.php
