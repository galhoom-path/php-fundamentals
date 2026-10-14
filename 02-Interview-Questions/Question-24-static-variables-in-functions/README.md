# Question 24 - What is a static variable inside a function?

Status: Not completed
Related lecture: Lecture 15
Folder: `02-Interview-Questions/Question-24-static-variables-in-functions/`

## Interview Question

What is a static variable inside a function?

## What The Interviewer Is Testing

Whether you know how a function can remember a value between calls.

## A Strong Answer Should Cover

- A `static` variable inside a function keeps its value between calls.
- It is initialized only once, the first time the function runs.
- It is useful for counters or simple caches, but hidden state should be used carefully.

## Practice Task

Write a function that returns how many times it has been called.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.variables.scope.php
