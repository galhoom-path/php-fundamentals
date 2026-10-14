# Question 27 - What do array_map, array_filter, and array_reduce do?

Status: Not completed
Related lecture: Lecture 17
Folder: `02-Interview-Questions/Question-27-map-filter-reduce/`

## Interview Question

What do array_map, array_filter, and array_reduce do?

## What The Interviewer Is Testing

Whether you can transform data with callbacks instead of manual loops.

## A Strong Answer Should Cover

- `array_map()` transforms every item and returns a new array of the same size.
- `array_filter()` keeps only items for which the callback returns true and preserves keys.
- `array_reduce()` combines all items into one value, such as a total.

## Practice Task

From a cart array, compute the total price of items with quantity above zero using filter, map, and reduce.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/function.array-map.php, https://www.php.net/manual/en/function.array-filter.php, https://www.php.net/manual/en/function.array-reduce.php
