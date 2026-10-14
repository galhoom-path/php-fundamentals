# Question 39 - How do you handle file uploads securely?

Status: Not completed
Related lecture: Lecture 26
Folder: `02-Interview-Questions/Question-39-secure-file-uploads/`

## Interview Question

How do you handle file uploads securely?

## What The Interviewer Is Testing

Whether you know that every part of an upload is untrusted.

## A Strong Answer Should Cover

- Check the upload error code and the file size limit.
- Detect the real type with `finfo_file()`; never trust the original name or the browser-sent type.
- Generate a new file name, move it with `move_uploaded_file()`, and store it outside the web root or where scripts cannot run.

## Practice Task

List every check you would perform before saving a profile picture.

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources: https://www.php.net/manual/en/features.file-upload.php, https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html
