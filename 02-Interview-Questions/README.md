---
name: php-fundamentals-interview-questions
purpose: >
  This file has exactly one purpose: to serve as the single learning source for
  realistic core-PHP interview questions after the PHP Fundamentals lectures are complete.
scope: >
  This file should only contain interview-question guidance, progress, practice
  rules, and folder conventions related to core-PHP interview preparation.
description: >
  Structured, iterative interview-preparation skill for core PHP. Trigger this
  skill when the student wants PHP fundamentals interview questions, asks to
  practice interview answers, or says "next interview question".
triggers:
  - user asks for core PHP interview questions
  - user wants to practice PHP fundamentals interview answers
  - user says "next interview question"
---

# PHP Fundamentals Interview Questions (PHP 8.5+) - Iterative Practice Track

## Who This Is For

Student profile: finished or is close to finishing the PHP Fundamentals lecture track and wants to prepare for realistic core-PHP interview questions.

---

## Interview Questions Track (45 Questions, One Per Session)

Start this track only after Lecture 30 in `../01-Lectures/README.md` is complete. Deliver exactly one interview question per session unless the student explicitly asks to continue.

Every interview question must be handled like a lecture:
- Understand the question first.
- Explain what the interviewer is really testing.
- Build the answer step by step.
- Write code only when the answer genuinely needs code.
- Ask one CHECK task at the end.
- Mark the question with ✅ only after the student can answer it clearly and pass the practice task.
- Always keep a `Source:` line at the end of each question folder's `README.md`.

This track stays inside core PHP. Do not ask OOP questions (classes, interfaces, traits, enums, exceptions, namespaces, PHPUnit, type declarations); they belong to the [PHP OOP repository](https://github.com/galhoom-path/php-oop) interview track. Do not ask about databases, Composer, or frameworks.

### Interview Track Review Checklist

```
- [ ] Every interview question from 1 to 45 is marked with ✅ in the progress list.
- [ ] Every question folder has a `README.md`.
- [ ] Every question folder `README.md` ends with a `Source:` or `Sources:` line.
- [ ] Every completed question folder has `Status: Completed`.
- [ ] The student can answer each question out loud in interview style.
- [ ] The student can explain the code-based questions without copying the answer.
- [ ] The student can connect each interview question back to the related lecture.
- [ ] The student has written `notes.md` for any question that felt difficult.
- [ ] Weak questions were repeated until the student could answer clearly and confidently.
```

Do not start `../03-Final-Project/README.md` until this checklist is complete.

### Interview Question Progress

```
Question 01 - What is PHP, and how does it handle a web request?
Question 02 - What is the difference between running PHP from the CLI and through a web server?
Question 03 - What is the difference between echo and print?
Question 04 - What is the difference between a variable and a constant, and between define() and const?
Question 05 - Which data types does PHP have?
Question 06 - What is the difference between isset(), empty(), and is_null()?
Question 07 - What is the difference between == and ===?
Question 08 - What is the difference between ?? and ?: ?
Question 09 - What is type juggling, and which bugs can it cause?
Question 10 - What changed in PHP 8 when comparing strings with numbers?
Question 11 - What is the difference between single quotes, double quotes, heredoc, and nowdoc?
Question 12 - Why should you use mb_* functions for non-English text?
Question 13 - What is the difference between match and switch?
Question 14 - When do you use for, foreach, or while?
Question 15 - What can go wrong when you use foreach by reference?
Question 16 - How do PHP arrays work, and what is the difference between indexed and associative arrays?
Question 17 - How does array destructuring work?
Question 18 - What is the difference between sort, asort, ksort, and usort?
Question 19 - What is the difference between array_merge, the + operator, and the spread operator on arrays?
Question 20 - What are named arguments, and when are they useful?
Question 21 - What is the difference between passing by value and passing by reference?
Question 22 - What is a variadic function?
Question 23 - How does variable scope work in PHP, and why should you avoid global?
Question 24 - What is a static variable inside a function?
Question 25 - How do anonymous functions and arrow functions capture outside variables?
Question 26 - What is a callable, and what is first-class callable syntax?
Question 27 - What do array_map, array_filter, and array_reduce do?
Question 28 - What is the pipe operator in PHP 8.5, and what problem does it solve?
Question 29 - What is a generator, and why does it save memory?
Question 30 - What is the difference between include, require, include_once, and require_once?
Question 31 - What are superglobals?
Question 32 - What is the difference between GET and POST?
Question 33 - How do you prevent XSS in PHP?
Question 34 - How do you validate user input in PHP?
Question 35 - What is the difference between sessions and cookies?
Question 36 - How do you protect a PHP session from hijacking and fixation?
Question 37 - How should you store user passwords in PHP?
Question 38 - What is CSRF, and how do you protect a form against it?
Question 39 - How do you handle file uploads securely?
Question 40 - How do you work with JSON in PHP and detect decoding errors?
Question 41 - How do you handle dates and time zones correctly in PHP?
Question 42 - When should you use regular expressions, and which preg functions do you know?
Question 43 - How would you organize a small PHP web app without a framework?
Question 44 - How do you configure error reporting for development and for production?
Question 45 - How do you debug a PHP script that does not work as expected?
```

---

## Question Source Map

```
Question 01 Source: https://www.php.net/manual/en/intro-whatis.php
Question 02 Sources: https://www.php.net/manual/en/features.commandline.php, https://www.php.net/manual/en/features.commandline.webserver.php
Question 03 Sources: https://www.php.net/manual/en/function.echo.php, https://www.php.net/manual/en/function.print.php
Question 04 Source: https://www.php.net/manual/en/language.constants.php
Question 05 Source: https://www.php.net/manual/en/language.types.intro.php
Question 06 Source: https://www.php.net/manual/en/types.comparisons.php
Question 07 Source: https://www.php.net/manual/en/language.operators.comparison.php
Question 08 Source: https://www.php.net/manual/en/language.operators.comparison.php
Question 09 Source: https://www.php.net/manual/en/language.types.type-juggling.php
Question 10 Source: https://www.php.net/manual/en/migration80.incompatible.php
Question 11 Source: https://www.php.net/manual/en/language.types.string.php
Question 12 Source: https://www.php.net/manual/en/book.mbstring.php
Question 13 Sources: https://www.php.net/manual/en/control-structures.match.php, https://www.php.net/manual/en/control-structures.switch.php
Question 14 Sources: https://www.php.net/manual/en/control-structures.for.php, https://www.php.net/manual/en/control-structures.foreach.php, https://www.php.net/manual/en/control-structures.while.php
Question 15 Source: https://www.php.net/manual/en/control-structures.foreach.php
Question 16 Source: https://www.php.net/manual/en/language.types.array.php
Question 17 Source: https://www.php.net/manual/en/language.types.array.php
Question 18 Source: https://www.php.net/manual/en/array.sorting.php
Question 19 Sources: https://www.php.net/manual/en/function.array-merge.php, https://www.php.net/manual/en/language.operators.array.php
Question 20 Source: https://www.php.net/manual/en/functions.arguments.php
Question 21 Source: https://www.php.net/manual/en/language.references.pass.php
Question 22 Source: https://www.php.net/manual/en/functions.arguments.php
Question 23 Source: https://www.php.net/manual/en/language.variables.scope.php
Question 24 Source: https://www.php.net/manual/en/language.variables.scope.php
Question 25 Sources: https://www.php.net/manual/en/functions.anonymous.php, https://www.php.net/manual/en/functions.arrow.php
Question 26 Sources: https://www.php.net/manual/en/language.types.callable.php, https://www.php.net/manual/en/functions.first_class_callable_syntax.php
Question 27 Sources: https://www.php.net/manual/en/function.array-map.php, https://www.php.net/manual/en/function.array-filter.php, https://www.php.net/manual/en/function.array-reduce.php
Question 28 Source: https://www.php.net/manual/en/language.operators.functional.php
Question 29 Source: https://www.php.net/manual/en/language.generators.overview.php
Question 30 Sources: https://www.php.net/manual/en/function.include.php, https://www.php.net/manual/en/function.require.php
Question 31 Source: https://www.php.net/manual/en/language.variables.superglobals.php
Question 32 Sources: https://www.php.net/manual/en/tutorial.forms.php, https://www.php.net/manual/en/reserved.variables.post.php
Question 33 Sources: https://www.php.net/manual/en/function.htmlspecialchars.php, https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html
Question 34 Source: https://www.php.net/manual/en/filter.filters.validate.php
Question 35 Sources: https://www.php.net/manual/en/book.session.php, https://www.php.net/manual/en/function.setcookie.php
Question 36 Source: https://www.php.net/manual/en/session.security.php
Question 37 Sources: https://www.php.net/manual/en/function.password-hash.php, https://www.php.net/manual/en/function.password-verify.php
Question 38 Source: https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html
Question 39 Sources: https://www.php.net/manual/en/features.file-upload.php, https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html
Question 40 Source: https://www.php.net/manual/en/book.json.php
Question 41 Sources: https://www.php.net/manual/en/function.date.php, https://www.php.net/manual/en/function.date-default-timezone-set.php
Question 42 Source: https://www.php.net/manual/en/book.pcre.php
Question 43 Source: https://www.php.net/manual/en/function.include.php
Question 44 Source: https://www.php.net/manual/en/errorfunc.configuration.php
Question 45 Sources: https://www.php.net/manual/en/function.var-dump.php, https://www.php.net/manual/en/function.error-log.php, https://www.php.net/manual/en/function.assert.php
```

---

## Interview Question Session Cycle

### PLAN
Before answering, state:
- The exact interview question.
- The real skill the interviewer is testing.
- Which lecture or lectures this question depends on.

### DO
- Start with a plain-English answer that could be said in an interview.
- Explain each important term before using it deeply.
- If code is needed, show the smallest possible PHP 8.5+ example first.
- Annotate every line of every code snippet.
- Then improve the answer into a stronger interview-ready version.

### CHECK
- For theory questions: ask the student to answer in their own words.
- For code questions: ask the student to write or fix one small code example.
Wait for the student's answer before moving on.

### ACT
- Correct answer: confirm it, give a polished interview answer, and mark the question with ✅.
- Partially correct: identify the missing point, re-teach only that point, then re-ask.
- Stuck: return to the simplest analogy, give a smaller version of the question, then re-ask.

---

## Code Standards

1. Target PHP 8.5 or newer.
2. Every code block starts with `<?php`. Procedural code only: no classes, `try/catch`, namespaces, or type declarations.
3. Naming follows PSR-12 style: `camelCase` variables and functions, `UPPER_SNAKE_CASE` constants.
4. Keep code examples focused on the interview question.
5. Annotate every line of every code snippet. Zero uncommented lines.
6. Every code block has a label above it stating what file it belongs to.
7. Do not pre-write final solution files for the student.

---

## Source Reference Rules

- Each question folder's `README.md` must end with a `Source:` line.
- Use the official PHP Manual when the question is about language behavior.
- Use the OWASP Cheat Sheet Series as a secondary source for web security questions.
- If one question depends on more than one official page, write `Sources:` and include all relevant links.
- The source line must be the final line in the `README.md`.

---

## Interview Questions Folder Structure

```
02-Interview-Questions/
  Question-01-what-is-php-and-how-it-runs/
    README.md
    code-1.php
    code-2.php
    notes.md
  Question-02-cli-vs-web-server/
    README.md
    ...
  ...
  Question-45-debugging-a-php-script/
    README.md
    ...
```

Only `README.md` is created as a scaffold. The code files and `notes.md` are created only when the student works through that question.

---

## Question Folder Rules

Each question folder contains a `README.md` with:
- The exact interview question.
- The related lecture or lectures.
- What the interviewer is testing.
- What a strong answer should cover.
- A practice task.
- The completion rule.
- The source reference as the final line.

When a question is completed:
1. Update its folder `README.md` status from `Not completed` to `Completed`.
2. Mark the matching question with ✅ in the progress list in this file.
3. If code was practiced, keep the student's code inside that question folder.

---

## What Not To Do

- Do not answer more than one interview question per session unless the student explicitly asks to continue.
- Do not turn the track into generic career advice.
- Do not teach OOP topics (they belong to the PHP OOP repository) or databases, Composer, and frameworks in this file.
- Do not pre-write final answers before the student tries the CHECK task.
- Do not create solution files unless the student is actively working through that question.
- Do not move lecture curriculum content into this file.
