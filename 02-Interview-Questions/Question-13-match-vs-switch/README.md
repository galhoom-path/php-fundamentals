# Question 13 - What is the difference between match and switch?

Status: Not completed
Related lecture: Lecture 9
Folder: `02-Interview-Questions/Question-13-match-vs-switch/`

## Interview Question

What is the difference between match and switch?

## What The Interviewer Is Testing

Whether you know the modern, safer decision expression.

## A Strong Answer Should Cover

- `match` is an expression that returns a value; `switch` is a statement.
- `match` uses strict comparison (`===`); `switch` uses loose comparison (`==`).
- `match` has no fall-through and throws an error for an unhandled value, while `switch` silently does nothing.

## Practice Task

Rewrite a `switch` that maps a status code to a label as a `match` expression.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/control-structures.match.php, https://www.php.net/manual/en/control-structures.switch.php
