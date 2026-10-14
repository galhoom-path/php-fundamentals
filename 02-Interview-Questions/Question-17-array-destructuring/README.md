# Question 17 - How does array destructuring work?

Status: Not completed
Related lecture: Lecture 11
Folder: `02-Interview-Questions/Question-17-array-destructuring/`

## Interview Question

How does array destructuring work?

## What The Interviewer Is Testing

Whether you can unpack array values into variables cleanly.

## A Strong Answer Should Cover

- `[$a, $b] = $pair;` assigns values by position.
- `['name' => $name] = $user;` assigns values by key.
- Destructuring works in `foreach` too, and PHP 8.5 warns when the value is not an array.

## Practice Task

Destructure a `['name' => ..., 'email' => ...]` array inside a `foreach` loop.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.types.array.php
