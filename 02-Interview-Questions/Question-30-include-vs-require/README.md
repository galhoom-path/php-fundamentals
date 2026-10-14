# Question 30 - What is the difference between include, require, include_once, and require_once?

Status: Not completed
Related lecture: Lecture 20
Folder: `02-Interview-Questions/Question-30-include-vs-require/`

## Interview Question

What is the difference between include, require, include_once, and require_once?

## What The Interviewer Is Testing

Whether you know how PHP loads files and handles missing ones.

## A Strong Answer Should Cover

- `require` stops the script with a fatal error if the file is missing; `include` only emits a warning and continues.
- The `_once` versions skip a file that was already loaded, preventing "cannot redeclare" errors.
- Use `require_once __DIR__ . '/file.php'` for files the program cannot run without.

## Practice Task

Explain which statement you would use for a config file and for an optional banner template, and why.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.include.php, https://www.php.net/manual/en/function.require.php
