# Question 20 - What are named arguments, and when are they useful?

Status: Not completed
Related lecture: Lecture 14
Folder: `02-Interview-Questions/Question-20-named-arguments/`

## Interview Question

What are named arguments, and when are they useful?

## What The Interviewer Is Testing

Whether you can make function calls readable and skip optional parameters.

## A Strong Answer Should Cover

- Named arguments pass values by parameter name: `fn(name: 'Sara')`.
- They make calls self-documenting and allow skipping optional parameters in the middle.
- Renaming a parameter becomes a breaking change for callers who use its name.

## Practice Task

Call `htmlspecialchars()` with a named `double_encode` argument and explain what it improves.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/functions.arguments.php
