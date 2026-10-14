# Question 04 - What is the difference between a variable and a constant, and between define() and const?

Status: Not completed
Related lecture: Lecture 3
Folder: `02-Interview-Questions/Question-04-variables-vs-constants-define-vs-const/`

## Interview Question

What is the difference between a variable and a constant, and between define() and const?

## What The Interviewer Is Testing

Whether you know when a value should be fixed and how PHP defines global constants.

## A Strong Answer Should Cover

- A variable starts with `$` and can be reassigned; a constant has no `$` and can never change after it is defined.
- `const` is resolved at compile time and must be used at the top level of a file.
- `define()` is a function call at runtime, so it can be used inside conditions or with computed names.

## Practice Task

Define a tax rate with `const` and a debug flag with `define()` inside an `if`, and explain why each choice fits.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.constants.php
