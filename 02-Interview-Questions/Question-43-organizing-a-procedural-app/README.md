# Question 43 - How would you organize a small PHP web app without a framework?

Status: Not completed
Related lectures: Lectures 20, 29
Folder: `02-Interview-Questions/Question-43-organizing-a-procedural-app/`

## Interview Question

How would you organize a small PHP web app without a framework?

## What The Interviewer Is Testing

Whether you can structure files by responsibility and keep them secure.

## A Strong Answer Should Cover

- Serve only a `public/` folder; keep config, helpers, storage, and data outside it.
- Split code into focused files (config, helpers, validation, storage) loaded with `require_once __DIR__`.
- Use one bootstrap file for error settings, time zone, and session start, and shared templates for the layout.

## Practice Task

Sketch the folder tree of the Lecture 29 notes app and explain why each folder exists.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/function.include.php
