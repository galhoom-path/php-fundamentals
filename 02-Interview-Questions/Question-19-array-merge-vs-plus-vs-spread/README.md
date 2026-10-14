# Question 19 - What is the difference between array_merge, the + operator, and the spread operator on arrays?

Status: Not completed
Related lecture: Lecture 12
Folder: `02-Interview-Questions/Question-19-array-merge-vs-plus-vs-spread/`

## Interview Question

What is the difference between array_merge, the + operator, and the spread operator on arrays?

## What The Interviewer Is Testing

Whether you can predict how keys behave when combining arrays.

## A Strong Answer Should Cover

- `array_merge()` re-indexes integer keys and lets later string keys overwrite earlier ones.
- `$a + $b` keeps the first value for any duplicate key and ignores the second.
- `[...$a, ...$b]` behaves like `array_merge()` and also supports string keys since PHP 8.1.

## Practice Task

Predict the result of combining `['a' => 1, 0 => 'x']` and `['a' => 2, 0 => 'y']` with all three approaches.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.array-merge.php, https://www.php.net/manual/en/language.operators.array.php
