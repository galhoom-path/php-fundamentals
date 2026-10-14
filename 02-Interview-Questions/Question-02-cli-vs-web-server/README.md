# Question 02 - What is the difference between running PHP from the CLI and through a web server?

Status: Not completed
Related lecture: Lecture 2
Folder: `02-Interview-Questions/Question-02-cli-vs-web-server/`

## Interview Question

What is the difference between running PHP from the CLI and through a web server?

## What The Interviewer Is Testing

Whether you know the two main ways PHP runs and when each one is used.

## A Strong Answer Should Cover

- The CLI runs a script from the terminal with `php file.php`; it is used for scripts, tasks, and tools.
- Through a web server, PHP runs once per HTTP request and sends its output to the browser.
- The built-in server `php -S localhost:8000` is for development only, never for production.

## Practice Task

Name one task you would run with the CLI and one you would serve through a web server, and explain why.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/features.commandline.php, https://www.php.net/manual/en/features.commandline.webserver.php
