# Task Management App

A dynamic web based Task Management Application built with HTML, CSS, and JavaScript. Users can create tasks with deadlines and categories, update task progress, automatically detect overdue items, and filter tasks in real time.

## Features
- Add Tasks: Create tasks with a name, category, deadline, and initial status.
- Automatic Overdue Detection: Compares task deadlines against the current date and automatically updates past-due, incomplete tasks to `Overdue`.
- Dynamic Status Updates: Change any task's status (`In Progress`, `Completed`, `Overdue`) directly from its dropdown menu with live feedback messages.
- Real Time Filtering: Filter the displayed task list by status, category, or both simultaneously.

## Project Structure
- `index.html` — Semantic HTML layout for the task form, filter controls, and task list.
- `style.css` — Minimal styling for layout structure and visual overdue highlights.
- `app.js` — JavaScript logic managing the task array, DOM rendering, date comparisons, and filters.

## Reflection
One of the main challenges during this project was keeping the displayed task list synchronized whenever a user added a task, changed a status, or switched filters. Initially, handling each action separately risked creating duplicate or outdated DOM elements. I solved this by storing all tasks as objects inside a single central array and building one reusable `renderTasks()` function that clears the list, checks for overdue deadlines, applies the active filters, and rebuilds the view cleanly from scratch. Another challenge was comparing deadlines reliably without timezone shifts, which I resolved by formatting dates as `YYYY-MM-DD` strings. Given more time, I would implement `localStorage` persistence with AI so tasks remain saved after refreshing the browser, add a delete button for removing completed tasks, and include a search bar to find tasks by keyword.