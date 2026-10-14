# Question 15 - What can go wrong when you use foreach by reference?

Status: Not completed
Related lectures: Lectures 10, 14
Folder: `02-Interview-Questions/Question-15-foreach-by-reference-pitfall/`

## Interview Question

What can go wrong when you use foreach by reference?

## What The Interviewer Is Testing

Whether you know a classic, hard-to-spot PHP bug.

## A Strong Answer Should Cover

- `foreach ($items as &$item)` lets the loop modify the original array.
- After the loop, `$item` is still a reference to the last element.
- Reusing `$item` in a later loop overwrites the last element; call `unset($item)` after the loop or avoid references.

## Practice Task

Predict the output of two loops over `[1, 2, 3]`, the first by reference and the second by value with the same variable name.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/control-structures.foreach.php
