# Question 22 - What is a variadic function?

Status: Not completed
Related lecture: Lecture 14
Folder: `02-Interview-Questions/Question-22-variadic-functions/`

## Interview Question

What is a variadic function?

## What The Interviewer Is Testing

Whether you know how to accept and spread any number of arguments.

## A Strong Answer Should Cover

- A variadic parameter `...$items` collects any number of arguments into an array.
- It must be the last parameter of the function.
- The spread operator `...$array` does the opposite: it unpacks an array into separate arguments.

## Practice Task

Write `sumAll(...$numbers)` and call it once with separate values and once with a spread array.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/functions.arguments.php
