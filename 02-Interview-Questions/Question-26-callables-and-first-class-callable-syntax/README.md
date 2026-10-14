# Question 26 - What is a callable, and what is first-class callable syntax?

Status: Not completed
Related lecture: Lecture 17
Folder: `02-Interview-Questions/Question-26-callables-and-first-class-callable-syntax/`

## Interview Question

What is a callable, and what is first-class callable syntax?

## What The Interviewer Is Testing

Whether you know the different ways to pass a function as a value.

## A Strong Answer Should Cover

- A callable is anything PHP can call: a function name string, an anonymous function, or an arrow function.
- First-class callable syntax `strlen(...)` creates a callable from a function directly.
- It is clearer and safer than passing the name as a string such as `'strlen'`.

## Practice Task

Pass `trim` to `array_map` in two ways and explain why `trim(...)` is preferred.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/language.types.callable.php, https://www.php.net/manual/en/functions.first_class_callable_syntax.php
