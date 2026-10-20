# Question 02 - What is the difference between running PHP from the CLI and through a web server?

Status: Not completed
Related lecture: Lecture 2
Folder: `02-Interview-Questions/Question-02-cli-vs-web-server/`

## Interview Question

What is the difference between running PHP from the CLI and through a web server?

## What The Interviewer Is Testing

Whether you know the two main ways PHP runs (CLI SAPI vs web), when each one is used, and why long jobs leave the browser.

## A Strong Answer Should Cover

- A `.php` file is text; the `php` executable (CLI SAPI) reads and runs it. PHP asks the OS to print, read files, and use memory — it does not talk to hardware directly.
- The CLI runs a script from the terminal with `php file.php`; it is used for scripts, scheduled jobs (cron), tools, and long-running work. CLI defaults `max_execution_time` to unlimited.
- Through a web server, PHP runs once per HTTP request and sends its output to the browser; web requests are bound by timeouts and the request/response cycle.
- The web server and PHP are separate jobs: the server receives the request; PHP executes the script. On real hosts they often connect via PHP-FPM (FastCGI), not by embedding PHP in every Apache worker (`mod_php`).
- The built-in server `php -S localhost:8000` is for development only; real sites usually use Apache or Nginx with PHP-FPM — never use `php -S` in production.

## Practice Task

Name one task you would run with the CLI and one you would serve through a web server, and explain why (include at least one reason that is about timeouts or "no browser involved").

## Files You May Create Here

- `code-1.php` for the first code attempt if the answer needs code.
- `code-2.php` for an improved version after feedback.
- `notes.md` for the final interview-style answer in your own words.

## Completion Rule

After you can answer this question clearly and solve the practice task, mark the question with the check mark in `../README.md`.

## Source

Sources:
- https://www.php.net/manual/en/features.commandline.php
- https://www.php.net/manual/en/features.commandline.differences.php
- https://www.php.net/manual/en/features.commandline.webserver.php
- https://www.php.net/manual/en/function.php-sapi-name.php
- https://www.php.net/manual/en/install.fpm.php
- https://www.php.net/manual/en/install.unix.apache2.php
