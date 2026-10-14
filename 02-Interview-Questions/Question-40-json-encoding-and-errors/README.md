# Question 40 - How do you work with JSON in PHP and detect decoding errors?

Status: Not completed
Related lecture: Lecture 27
Folder: `02-Interview-Questions/Question-40-json-encoding-and-errors/`

## Interview Question

How do you work with JSON in PHP and detect decoding errors?

## What The Interviewer Is Testing

Whether you convert data safely and never ignore invalid JSON.

## A Strong Answer Should Cover

- `json_encode()` converts arrays to JSON; flags such as `JSON_UNESCAPED_UNICODE` keep Arabic text readable.
- `json_decode($json, true)` returns associative arrays instead of objects.
- `json_decode()` returns `null` on invalid input, so check `json_last_error()` / `json_last_error_msg()`.

## Practice Task

Explain how you would load a JSON file that might be missing or broken without crashing the page.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Source: https://www.php.net/manual/en/book.json.php
