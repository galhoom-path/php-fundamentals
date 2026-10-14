# Question 10 - What changed in PHP 8 when comparing strings with numbers?

Status: Not completed
Related lecture: Lecture 6
Folder: `02-Interview-Questions/Question-10-php8-string-number-comparison/`

## Interview Question

What changed in PHP 8 when comparing strings with numbers?

## What The Interviewer Is Testing

Whether you know a real behavior change between PHP versions.

## A Strong Answer Should Cover

- Before PHP 8, a non-numeric string was converted to a number, so `0 == "abc"` was true.
- Since PHP 8, if the string is not numeric, the number is converted to a string and compared as strings, so `0 == "abc"` is false.
- Numeric strings such as `"1e3"` are still compared as numbers.

## Practice Task

Predict the PHP 8 result of `0 == "abc"`, `"1" == "01"`, and `100 == "1e2"`.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/migration80.incompatible.php
