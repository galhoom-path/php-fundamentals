# Question 29 - What is a generator, and why does it save memory?

Status: Not completed
Related lecture: Lecture 19
Folder: `02-Interview-Questions/Question-29-generators-and-memory/`

## Interview Question

What is a generator, and why does it save memory?

## What The Interviewer Is Testing

Whether you understand lazy, one-at-a-time value production.

## A Strong Answer Should Cover

- A generator is a function that uses `yield` to hand out values one at a time.
- It does not build the whole result in memory, so it can process huge files or ranges.
- The caller loops over it with `foreach`, and execution pauses at each `yield`.

## Practice Task

Explain how you would read a 2 GB log file line by line without running out of memory.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/language.generators.overview.php
