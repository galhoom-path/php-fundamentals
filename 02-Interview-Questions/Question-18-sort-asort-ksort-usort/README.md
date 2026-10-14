# Question 18 - What is the difference between sort, asort, ksort, and usort?

Status: Not completed
Related lectures: Lectures 12, 17
Folder: `02-Interview-Questions/Question-18-sort-asort-ksort-usort/`

## Interview Question

What is the difference between sort, asort, ksort, and usort?

## What The Interviewer Is Testing

Whether you know which sorting function keeps keys and which uses custom rules.

## A Strong Answer Should Cover

- `sort()` sorts values and re-indexes keys from 0.
- `asort()` sorts by value and `ksort()` sorts by key, both keeping key-value pairs.
- `usort()` sorts with your own comparison callback, often written with `<=>`.

## Practice Task

Sort a list of users by age with `usort` and explain why `sort` would not work here.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/array.sorting.php
