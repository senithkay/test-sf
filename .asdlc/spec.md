# Overview

**Sefef** is a web-based task management application designed to help individuals organize, track, and complete their daily work. The system provides a structured environment where users can create and manage personal to-do lists enriched with metadata such as categories and due dates, enabling better prioritization and time management.

The application targets individual users — students, professionals, and anyone managing personal workloads — who need a lightweight yet capable tool for staying on top of their responsibilities. Each user's data is fully private and isolated behind an authenticated account.

The core approach centers on simplicity and speed: users can quickly capture tasks, organize them into meaningful groups, set deadlines, and monitor progress through a clean, responsive web interface accessible from any modern browser.

---

# Capabilities

## User Authentication

- Users can register for an account using a unique email address and a password.
- Users can log in with their email and password to access their personal workspace.
- Users can log out, immediately ending their authenticated session.
- Passwords must meet a minimum security standard: at least 8 characters, including at least one letter and one number.
- Users can request a password reset via a link sent to their registered email address.
- Each user can only access their own data; no user can view or modify another user's tasks or categories.
- Sessions expire after a defined period of inactivity and require re-authentication.

## Task Management (CRUD)

- Users can create a new task by providing at minimum a title.
- Each task supports the following optional fields: description, due date, category, and priority level.
- Users can view a list of all their tasks.
- Users can view the full details of a single task.
- Users can edit any field of an existing task at any time.
- Users can delete a task permanently; deletion requires a confirmation step.
- Users can mark a task as complete or incomplete with a single action.
- Completed tasks are visually distinguished from incomplete tasks in all list views.

## Categories

- Users can create named categories to group related tasks.
- Users can rename an existing category.
- Users can delete a category; tasks previously assigned to that category become uncategorized.
- Each task can be assigned to at most one category.
- Users can filter their task list to show only tasks belonging to a specific category.

## Due Dates & Scheduling

- Users can assign a due date (and optionally a due time) to any task.
- The task list can be sorted or filtered by due date.
- Tasks that are past their due date and still incomplete are visually flagged as overdue.
- Users can clear a due date from a task without deleting the task.

## Task Organization & Filtering

- Users can filter tasks by status (all, incomplete, complete).
- Users can filter tasks by category.
- Users can filter tasks by due date range (e.g., due today, due this week, overdue).
- Users can sort tasks by due date, creation date, or priority.
- Users can search tasks by keyword matched against title and description.

## Priority

- Each task can be assigned one of three priority levels: Low, Medium, or High.
- Tasks can be filtered or sorted by priority level.

## Performance & Reliability

- All task list views load within 2 seconds under normal network conditions.
- The application is fully usable on modern desktop and mobile browsers without installing any software.
- Form inputs provide immediate inline validation feedback before submission.
- All user data is persisted reliably; no task is lost due to a page refresh or navigation event.

## Security & Privacy

- All communication between the client and server is encrypted in transit.
- User passwords are never stored in plain text.
- Unauthenticated users are redirected to the login page when attempting to access protected pages.
- The application protects against common web vulnerabilities including cross-site scripting (XSS) and cross-site request forgery (CSRF).
