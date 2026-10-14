# Question 42 - When should you use regular expressions, and which preg functions do you know?

Status: Not completed
Related lecture: Lecture 28
Folder: `02-Interview-Questions/Question-42-regular-expressions-when-and-how/`

## Interview Question

When should you use regular expressions, and which preg functions do you know?

## What The Interviewer Is Testing

Whether you can use regex correctly and also know when not to.

## A Strong Answer Should Cover

- Use regex for patterns that simple string functions cannot express, such as phone formats.
- Main functions: `preg_match`, `preg_match_all`, `preg_replace`, and `preg_split`; add the `u` flag for UTF-8.
- Prefer `str_contains()` and similar functions for simple checks, and use `preg_quote()` for user input inside a pattern.

## Practice Task

Write a pattern that validates an Egyptian mobile number and explain each part.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/book.pcre.php
