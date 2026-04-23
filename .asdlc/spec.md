# Overview

This system is a web-based todo management application that allows individual users to create, organize, and track personal tasks. The application supports user accounts so that each person's data is private and accessible only to them. It is designed for everyday users who need a straightforward tool to manage their workload without unnecessary complexity.

The core experience centers on a clean task list interface where users can add tasks with optional due dates and category labels, then update or remove them as their work evolves. The application surfaces what needs attention — overdue items, upcoming deadlines, and tasks by category — so users can stay organized at a glance.

Target users are individuals managing personal or professional tasks who expect a fast, reliable, and accessible web experience. The application must work well across desktop and mobile browsers and keep user data secure at all times.

---

# Capabilities

## User Authentication

- A visitor can create a new account by providing a unique email address and a password.
- A registered user can log in with their email and password.
- A logged-in user can log out, ending their session immediately.
- Passwords must be at least 8 characters long and are never stored or transmitted in plain text.
- A user can request a password reset via a link sent to their registered email address.
- Each user can only access their own tasks and data; no cross-user data access is permitted.
- Sessions expire after a configurable period of inactivity (default: 30 days).

## Task Management (CRUD)

- A logged-in user can create a new task with a required title (1–255 characters).
- A user can add an optional plain-text description (up to 2,000 characters) to any task.
- A user can mark a task as complete or incomplete at any time.
- A user can edit the title, description, due date, and category of any of their tasks.
- A user can delete a task; deletion is permanent and requires a confirmation step.
- Each task records the date and time it was created and last modified.

## Categories

- A user can create a named category (1–50 characters) to group related tasks.
- A user can rename or delete any of their categories.
- Deleting a category does not delete its tasks; those tasks become uncategorized.
- A task can belong to at most one category at a time.
- A user can reassign a task to a different category or remove it from its current category.

## Due Dates

- A user can assign an optional due date (date only, no time required) to any task.
- A task is visually flagged as overdue when its due date is in the past and it is not yet complete.
- A user can remove or change the due date on any task at any time.

## Task Viewing &amp; Filtering

- A user can view all of their tasks in a single list, sorted by due date (ascending) by default.
- A user can filter tasks by category, showing only tasks in the selected category.
- A user can filter tasks by status: all, active (incomplete), or completed.
- A user can filter tasks to show only overdue items.
- A user can search tasks by keyword, matching against task titles and descriptions.
- A user can sort tasks by due date (ascending/descending) or by creation date (ascending/descending).

## Non-Functional Requirements

- All pages and API interactions must be served over HTTPS.
- The application must load the main task list within 2 seconds under normal conditions.
- The application must be usable on modern desktop and mobile browsers (Chrome, Firefox, Safari, Edge — latest two major versions each).
- The interface must meet WCAG 2.1 Level AA accessibility standards.
- The application must handle at least 500 concurrent users without degraded performance.
- All user data must be logically isolated; no user can read, modify, or delete another user's tasks or categories.

