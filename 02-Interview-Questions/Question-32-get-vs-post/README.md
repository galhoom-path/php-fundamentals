# Question 32 - What is the difference between GET and POST?

Status: Not completed
Related lecture: Lecture 22
Folder: `02-Interview-Questions/Question-32-get-vs-post/`

## Interview Question

What is the difference between GET and POST?

## What The Interviewer Is Testing

Whether you choose the right HTTP method for reading and for changing data.

## A Strong Answer Should Cover

- GET sends data in the URL; it is visible, bookmarkable, cached, and limited in size.
- POST sends data in the request body and is used for actions that create or change data.
- GET should never change data; use POST plus Post/Redirect/Get for forms that change state.

## Practice Task

Decide GET or POST for: a search box, a login form, a delete button, and pagination, and justify each.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/tutorial.forms.php, https://www.php.net/manual/en/reserved.variables.post.php
