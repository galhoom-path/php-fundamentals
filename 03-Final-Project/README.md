---
name: php-fundamentals-final-project
purpose: >
  This file has exactly one purpose: to guide one realistic final project that
  proves the student understands the PHP Fundamentals lecture track and interview track.
scope: >
  This file should only contain the final project plan, milestones, validation
  checklist, folder conventions, and mentor rules for the PHP Fundamentals final project.
description: >
  Structured final-project guide for building one real-world procedural PHP
  web application after finishing the lectures and interview questions. Trigger
  when the student says "start final project", "continue final project", or
  "review my final project".
triggers:
  - user wants to start the PHP Fundamentals final project
  - user wants to continue the PHP Fundamentals final project
  - user asks for project review after finishing lectures and interview questions
---

# PHP Fundamentals Final Project (PHP 8.5+) - BookIt Lite

> **Status:** Not started — This folder is the student's workspace for the PHP Fundamentals final project.

## Rule

The student writes all implementation code. The mentor may guide, review, debug, and ask focused questions, but must not write the solution files.

## When To Start

Start only after:
1. All 30 lectures in `../01-Lectures/README.md` are completed.
2. All 45 interview questions in `../02-Interview-Questions/README.md` are completed.
3. The student explicitly says they are ready to start the final project.

This project is the final proof step. It is not a lecture replacement.

**Next step when ready:** Start with Milestone 00 in this README.

---

## Final Project Review Checklist

```
- [ ] Every milestone from 00 to 12 is marked with ✅ in the progress list.
- [ ] The app runs with `php -S localhost:8000 -t public` and `playground.php` runs from the CLI.
- [ ] Code is split into focused files loaded with `require_once` and `__DIR__` paths.
- [ ] Configuration lives in one file that returns an array; constants hold fixed values.
- [ ] Booking data is stored as arrays and saved to a JSON file with error checks.
- [ ] Every input is validated and every output is escaped with one `e()` helper.
- [ ] The admin area uses `password_hash()`/`password_verify()`, sessions, and `session_regenerate_id()`.
- [ ] Every form that changes data uses POST, a CSRF token, and Post/Redirect/Get.
- [ ] Listing and reports use array functions, callbacks, and the pipe operator where it improves readability.
- [ ] The CSV export uses a generator.
- [ ] Dates use one configured time zone.
- [ ] Phone numbers are validated with a regular expression.
- [ ] Errors are logged to a file; production settings do not display errors.
- [ ] `tests/run-checks.php` uses `assert()` to verify the most important helper functions.
- [ ] `notes.md` explains the main design decisions in interview style.
- [ ] The student can explain every major file and design choice without reading the code line by line.
```

The project is complete only when the code works and the student can explain why the design works.

---

## Project Summary

Build **BookIt Lite**, a small appointment-booking web app for a local business such as a barber shop or a clinic.

The project stays intentionally small:
- No framework.
- No database: data is stored in a JSON file.
- No classes or other OOP features (they come in the PHP OOP repository).
- No Composer and no external packages.

The goal is not to build a huge product. The goal is to prove the student can design and build a complete, secure procedural PHP web application from scratch.

---

## Student Role (Mandatory)

The mentor may:
- Explain requirements.
- **Show** short annotated examples in the chat (not full solution files).
- Ask design questions.
- Review code written by the student.
- Point out missing concepts.
- Suggest the next small step.
- Help debug errors after the student shares code or error output.

The mentor must not:
- Write complete solution files.
- Create the student's implementation files.
- Build the project on behalf of the student.
- Skip the student's design decisions.
- Turn this into an OOP, database, or framework course.

---

## Business Scenario

A small barber shop takes appointments by phone, and the owner keeps losing track of them on paper. Customers often call outside working hours, and double bookings happen every week.

The owner wants a simple website where customers book a time slot themselves, and a private admin page where the owner reviews, confirms, or cancels bookings.

The business wants to answer questions like:
- Which bookings are scheduled for today and this week?
- Which time slots are still free?
- Which bookings are pending, confirmed, or cancelled?
- How many bookings came in this month?
- Can the owner export bookings to a spreadsheet?

---

## Core Features

1. Show the business name, working hours, and services from one config file.
2. Public booking form: name, phone, service, date, and time slot.
3. Validate every field (required fields, real date, future date, working hours, valid phone).
4. Prevent double booking of the same date and time slot.
5. Show a success page after booking (Post/Redirect/Get with a flash message).
6. Store bookings in a JSON file with safe writing (`LOCK_EX`).
7. Admin login with a hashed password stored in config (never plain text).
8. Admin logout.
9. Admin dashboard listing bookings sorted by date and time.
10. Filter bookings by status (`pending`, `confirmed`, `cancelled`) and by date.
11. Confirm or cancel a booking (POST + CSRF only).
12. Search bookings by customer name (multibyte-safe).
13. Show simple statistics: totals per status and per service.
14. Export bookings to CSV using a generator.
15. Log errors and important admin actions to a log file.
16. Run an `assert()`-based check script for the helper functions.

---

## Required Folder Structure

```
03-Final-Project/
  README.md                      // This guide
  public/                        // The only folder served by the web server
    index.php                    // Home page and booking form
    book.php                     // Handles the booking POST
    admin/
      login.php
      logout.php
      dashboard.php
      update-status.php          // Confirm / cancel (POST only)
      export.php                 // CSV export
  src/
    config.php                   // Returns the config array
    bootstrap.php                // Error settings, time zone, session start, requires
    helpers.php                  // e(), redirect(), flash messages
    csrf.php                     // csrfToken(), checkCsrf()
    validation.php               // validateBooking() and small rule functions
    storage.php                  // loadBookings(), saveBookings()
    bookings.php                 // Booking rules: free slots, double-booking check, status changes
    reports.php                  // Filtering, sorting, statistics, CSV generator
    auth.php                     // login(), logout(), requireAdmin()
  templates/
    header.php
    footer.php
  storage/
    bookings.json                // Created by the app
  logs/
    app.log                      // Created by the app
  tests/
    run-checks.php               // assert()-based checks
  playground.php                 // Student-created CLI runner for quick experiments
  notes.md                       // Student's design notes and final reflection
```

This structure is a target, not a starting dump. The student creates files gradually as each milestone requires them.

---

## Development Rules

1. Use PHP 8.5 or newer.
2. Procedural PHP only: functions, arrays, and files. No classes, interfaces, enums, exceptions, or namespaces.
3. Keep each file focused on one clear responsibility.
4. Load files with `require_once __DIR__ . '/...'`.
5. Validate every input, escape every output, and use POST + CSRF for every change.
6. Do not add features outside the checklist until the core project is complete.
7. Every important rule must be enforced by code, not by comments.
8. Never hardcode real secrets; the admin password is stored only as a hash.

---

## Milestone Plan

### Milestone 0 - Project Setup

**Goal:** Create the project workspace and explain the first design.

The student must create:
- `notes.md`
- A first draft of the folder structure.

The student must answer:
- What problem does this project solve?
- What are the main pages and the main data in the system?
- Which code runs in the browser request, and which data lives on the server?

Completion check:
- The student can explain the request/response flow of a booking in plain English without code.

---

### Milestone 1 - Config, Constants, and Data Shape

**Goal:** Describe the business and one booking with variables, constants, and arrays.

The student must create:
- `src/config.php`
- `playground.php`

Required concepts:
- Variables, constants, data types (Lectures 3–4)
- Associative and nested arrays (Lecture 11)

Behavior to implement:
- The config returns business name, time zone, working hours, slot length, and services.
- `playground.php` builds two sample bookings as arrays and prints them with `var_dump()`.

Completion check:
- The student can explain why the config is an array returned from a file while fixed values are constants.

---

### Milestone 2 - Calculations, Types, and Safe Parsing

**Goal:** Compute time slots and convert raw input safely.

Required concepts:
- Operators, `===`, `??` (Lecture 5)
- Type juggling and casting (Lecture 6)

Behavior to implement:
- Generate the list of time slots from opening hour, closing hour, and slot length.
- Convert raw form values with explicit casts and reject non-numeric values.

Completion check:
- The student can show one bug that loose comparison or automatic conversion would cause here.

---

### Milestone 3 - Text Formatting

**Goal:** Present names, prices, and messages correctly, including Arabic names.

Required concepts:
- Strings and interpolation (Lecture 7)
- String functions and `mb_*` (Lecture 8)

Behavior to implement:
- Trim and normalize customer names with multibyte-safe functions.
- Format service prices with `number_format()` or `sprintf()`.
- Build confirmation messages with interpolation or heredoc.

Completion check:
- The student can explain why `strlen()` would give a wrong length for an Arabic name.

---

### Milestone 4 - Booking Rules with Control Flow

**Goal:** Decide whether a booking is allowed.

Required concepts:
- `if` and `match` (Lecture 9)
- Loops (Lecture 10)

Behavior to implement:
- Reject bookings outside working hours or on closed days.
- Map a status to a label and color with `match`.
- Loop over existing bookings to detect a double booking.

Completion check:
- The student can explain why `match` was chosen over `switch` for status labels.

---

### Milestone 5 - Functions and File Organization

**Goal:** Move all logic into small, named functions spread across focused files.

The student must create:
- `src/bootstrap.php`, `src/helpers.php`, `src/validation.php`, `src/bookings.php`

Required concepts:
- Functions, arguments, scope (Lectures 13–15)
- `include` / `require` (Lecture 20)

Behavior to implement:
- Every rule from Milestones 2–4 becomes a function with clear parameters and return values.
- Functions use named arguments where it improves clarity.
- No function uses `global`.

Completion check:
- The student can explain why each function receives data as parameters instead of reading outside variables.

---

### Milestone 6 - Pages, Forms, Validation, and Escaping

**Goal:** Make the public booking flow work in the browser safely.

The student must create:
- `public/index.php`, `public/book.php`, `templates/header.php`, `templates/footer.php`

Required concepts:
- HTTP and superglobals (Lecture 21)
- Forms and POST, Post/Redirect/Get (Lecture 22)
- Validation and escaping (Lecture 23)

Behavior to implement:
- The form posts to `book.php`, which validates input and redirects back with errors or success.
- Old values and errors are re-displayed, escaped with `e()`.
- Invalid requests (wrong method) get a proper status code.

Completion check:
- The student can show where every user value is validated and where it is escaped.

---

### Milestone 7 - Persistent Storage with JSON

**Goal:** Save and load bookings from a file safely.

The student must create:
- `src/storage.php`

Required concepts:
- Files (Lecture 26)
- JSON and dates (Lecture 27)

Behavior to implement:
- `loadBookings()` returns an empty array when the file is missing and logs invalid JSON.
- `saveBookings()` writes with `LOCK_EX` and keeps Arabic text readable.
- Dates are stored as `Y-m-d` and times as `H:i` in the configured time zone.

Completion check:
- The student can explain what happens if two customers book at the same moment and how `LOCK_EX` helps.

---

### Milestone 8 - Admin Login and Protection

**Goal:** Protect the admin area.

The student must create:
- `src/auth.php`, `src/csrf.php`, `public/admin/login.php`, `public/admin/logout.php`

Required concepts:
- Sessions and cookies (Lecture 24)
- Password hashing and CSRF (Lecture 25)

Behavior to implement:
- Login verifies the password with `password_verify()` against the hash in config.
- The session ID is regenerated after login; logout destroys the session.
- Every admin page calls `requireAdmin()`.
- Every admin form carries a CSRF token checked with `hash_equals()`.

Completion check:
- The student can explain what an attacker could do without the CSRF check.

---

### Milestone 9 - Dashboard, Filters, and Statistics

**Goal:** Give the owner a clear view of the bookings.

The student must create:
- `src/reports.php`, `public/admin/dashboard.php`, `public/admin/update-status.php`

Required concepts:
- Array functions (Lecture 12)
- Anonymous and arrow functions, callbacks (Lectures 16–17)
- Pipe operator (Lecture 18)

Behavior to implement:
- Sort bookings by date and time with `usort` and `<=>`.
- Filter by status, date, and multibyte name search with `array_filter`.
- Compute totals per status and service with `array_reduce` or `array_count_values`.
- Use a pipe operator chain for at least one clean-up or reporting pipeline.
- Confirm or cancel a booking through POST + CSRF.

Completion check:
- The student can explain one place where the pipe operator improved readability and one place where it would not.

---

### Milestone 10 - CSV Export with a Generator

**Goal:** Export bookings without building the whole CSV in memory.

The student must create:
- `public/admin/export.php`

Required concepts:
- Generators (Lecture 19)
- Headers for downloads (Lecture 21)

Behavior to implement:
- A generator yields one CSV row at a time.
- The export sends correct download headers and writes rows with `fputcsv()` to `php://output`.

Completion check:
- The student can explain why a generator scales better than building one large array.

---

### Milestone 11 - Regex Validation, Logging, and Checks

**Goal:** Harden validation and prove the helpers work.

The student must create:
- `tests/run-checks.php`

Required concepts:
- Regular expressions (Lecture 28)
- Errors, logging, and `assert()` (Lecture 30)

Behavior to implement:
- Validate phone numbers with `preg_match()`.
- Development and production error settings live in `bootstrap.php`; production writes errors to `logs/app.log`.
- Log admin actions (login, status change, export) with `error_log()`.
- `run-checks.php` asserts normal and edge cases for validation, slot generation, and double-booking detection.

Completion check:
- The student can show one bug that a check in `run-checks.php` would catch.

---

### Milestone 12 - Final Review

**Goal:** Prove understanding, not only working code.

The student must write `notes.md` with answers to:
- What are the most important files in the project, and what is each responsible for?
- Where is every user input validated, and where is every output escaped?
- How does the admin area stay protected?
- Why is the CSV export built with a generator?
- Where did callbacks or the pipe operator make the code clearer?
- What happens when the JSON file is missing or broken?
- Which check in `run-checks.php` protects the most important rule?
- Which parts of this project would become simpler with OOP, and which PHP OOP lectures cover them?
- What would you change before using this project in production?

Completion check:
- The student can explain the whole project from memory.
- The student can answer interview-style questions about every major design choice.

---

## Concept Coverage Checklist

```
Lecture 01 - Server-side PHP and the request/response cycle
Lecture 02 - Running PHP with the CLI and the built-in server
Lecture 03 - Variables and constants
Lecture 04 - Scalar types and null
Lecture 05 - Operators
Lecture 06 - Type juggling and casting
Lecture 07 - Strings and interpolation
Lecture 08 - String functions and multibyte text
Lecture 09 - if, switch, and match
Lecture 10 - Loops
Lecture 11 - Arrays
Lecture 12 - Array functions (including array_first / array_last)
Lecture 13 - Functions
Lecture 14 - Default, named, variadic, and by-reference arguments
Lecture 15 - Scope and static variables
Lecture 16 - Anonymous and arrow functions
Lecture 17 - Callbacks and first-class callables
Lecture 18 - Pipe operator
Lecture 19 - Generators
Lecture 20 - include and require
Lecture 21 - HTTP, superglobals, headers, redirects
Lecture 22 - Forms, POST, Post/Redirect/Get
Lecture 23 - Validation and output escaping
Lecture 24 - Sessions and cookies
Lecture 25 - Password hashing and CSRF
Lecture 26 - Files and uploads
Lecture 27 - JSON and dates
Lecture 28 - Regular expressions
Lecture 29 - End-to-end mini-project thinking
Lecture 30 - Error reporting, logging, and assert()
Interview Questions 01-45 - Explain every major design choice in interview form
```

---

## Mentor Session Flow

### PLAN
Ask:
- Which milestone are you working on?
- What files did you create or change?
- What behavior should work now?

### DO
The student writes the code in their own files. The mentor may explain the next step and show small examples in chat, but must not write or save the implementation.

### CHECK
The mentor asks one focused question or gives one small verification task.

Examples:
- "Show me where the phone number is validated."
- "What happens if someone submits the status form without a CSRF token?"
- "What does `loadBookings()` return when the file is missing?"

### ACT
- If correct: mark the milestone as complete.
- If partially correct: name the missing concept and ask for one focused change.
- If stuck: reduce the task to a smaller version.

---

## Progress

```
Milestone 00 - Project Setup
Milestone 01 - Config, Constants, and Data Shape
Milestone 02 - Calculations, Types, and Safe Parsing
Milestone 03 - Text Formatting
Milestone 04 - Booking Rules with Control Flow
Milestone 05 - Functions and File Organization
Milestone 06 - Pages, Forms, Validation, and Escaping
Milestone 07 - Persistent Storage with JSON
Milestone 08 - Admin Login and Protection
Milestone 09 - Dashboard, Filters, and Statistics
Milestone 10 - CSV Export with a Generator
Milestone 11 - Regex Validation, Logging, and Checks
Milestone 12 - Final Review
```

Mark a milestone with ✅ only after the student can explain it and the code behavior works.

---

## Source References

This project is based on the same official learning sources used by the lecture and interview tracks.

Sources:
- https://www.php.net/manual/en/langref.php
- https://www.php.net/manual/en/language.types.array.php
- https://www.php.net/manual/en/ref.array.php
- https://www.php.net/manual/en/functions.user-defined.php
- https://www.php.net/manual/en/functions.anonymous.php
- https://www.php.net/manual/en/language.operators.functional.php
- https://www.php.net/manual/en/language.generators.overview.php
- https://www.php.net/manual/en/function.include.php
- https://www.php.net/manual/en/language.variables.superglobals.php
- https://www.php.net/manual/en/function.htmlspecialchars.php
- https://www.php.net/manual/en/filter.filters.validate.php
- https://www.php.net/manual/en/book.session.php
- https://www.php.net/manual/en/function.password-hash.php
- https://www.php.net/manual/en/book.json.php
- https://www.php.net/manual/en/function.fputcsv.php
- https://www.php.net/manual/en/book.pcre.php
- https://www.php.net/manual/en/errorfunc.configuration.php
- https://www.php.net/manual/en/function.assert.php
- https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html
