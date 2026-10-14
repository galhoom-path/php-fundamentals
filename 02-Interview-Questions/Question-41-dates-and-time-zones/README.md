# Question 41 - How do you handle dates and time zones correctly in PHP?

Status: Not completed
Related lecture: Lecture 27
Folder: `02-Interview-Questions/Question-41-dates-and-time-zones/`

## Interview Question

How do you handle dates and time zones correctly in PHP?

## What The Interviewer Is Testing

Whether you avoid wrong times caused by missing time zone settings.

## A Strong Answer Should Cover

- Set one time zone for the app with `date_default_timezone_set()` or `date.timezone` in `php.ini`.
- Store dates in a clear format such as `Y-m-d H:i:s`.
- Use `strtotime()` and `date()` for simple calculations and formatting; the object-based date API comes after the OOP repo.

## Practice Task

Show how to print the date seven days from now in the `Africa/Cairo` time zone.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.date.php, https://www.php.net/manual/en/function.date-default-timezone-set.php
