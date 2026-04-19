# Overview

This system is a web-based task management application that allows individuals to create, organize, and track their personal to-do items. It provides a structured way to manage daily work and personal goals through an intuitive interface that supports categorization, due dates, and priority tracking.

The application targets individual users — students, professionals, and anyone seeking to manage personal tasks — who need a lightweight but capable tool accessible from any web browser. Users must authenticate to access their data, ensuring their task lists remain private and persistent across sessions.

The system centers on a straightforward CRUD model for tasks, enriched with categories and due-date awareness to help users focus on what matters most. The experience is designed to be fast and frictionless, minimizing the overhead of keeping a task list up to date.

---

# Capabilities

## User Authentication

- Users can register a new account using a unique email address and a password.
- Passwords must meet a minimum complexity requirement: at least 8 characters, including one number and one special character.
- Registered users can log in with their email and password.
- Users can log out, ending their authenticated session.
- Users can request a password reset via a link sent to their registered email address.
- Each user can only access their own tasks and categories — no cross-user data visibility.
- Sessions expire after a configurable period of inactivity (default: 30 minutes).

## Task Management (CRUD)

- Users can create a new task with a title (required), description (optional), due date (optional), category (optional), and priority level.
- Task titles must be between 1 and 200 characters.
- Users can view a list of all their tasks.
- Users can open a single task to view its full details.
- Users can edit any field of an existing task.
- Users can delete a task; deletion requires a confirmation step.
- Users can mark a task as complete or revert it to incomplete.
- The system records the creation timestamp and last-modified timestamp for every task.

## Categories

- Users can create custom categories with a unique name (per user) and an optional color label.
- Users can rename or delete a category they own.
- Deleting a category does not delete the tasks assigned to it; those tasks become uncategorized.
- Users can assign a task to exactly one category or leave it uncategorized.
- Users can filter their task list to show only tasks belonging to a selected category.

## Due Dates & Scheduling

- Users can set a due date (and optionally a due time) on any task.
- The task list visually distinguishes tasks that are overdue (past due date and incomplete).
- Users can filter tasks by due date range (e.g., due today, due this week, overdue).
- Tasks without a due date are displayed separately or clearly indicated as undated.

## Task Organization & Filtering

- Users can sort their task list by due date, creation date, priority, or title (ascending/descending).
- Users can filter tasks by completion status (all, active, completed).
- Users can filter tasks by priority level (low, medium, high).
- Users can search tasks by keyword matching the title or description.
- Combined filters (e.g., category + status + due date) must all apply simultaneously.

## Priority Levels

- Each task has a priority level: Low, Medium, or High (default: Medium).
- Priority is visually indicated in the task list view.
- Users can change the priority of a task at any time.

## User Account Management

- Users can update their display name and email address.
- Users can change their password while logged in by providing their current password.
- Users can delete their account, which permanently removes all their tasks and categories after a confirmation step.

## Non-Functional Requirements

- All pages must load and become interactive within 2 seconds under normal network conditions.
- The application must be fully usable on modern desktop and mobile browsers (responsive layout).
- All data transmitted between the client and server must be encrypted in transit (HTTPS).
- Passwords must be stored using a secure one-way hashing algorithm — never in plain text.
- The system must handle at least 500 concurrent users without degraded performance.
- Input fields must be validated on both the client side (immediate feedback) and server side (authoritative enforcement).
- The application must display clear, user-friendly error messages for all failure states (e.g., login failure, network error, validation error).
