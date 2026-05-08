# Standalone Knowledge Transition Monitoring Application

A lightweight single-file HTML app for visually planning, tracking, and managing structured knowledge transitions. Ideal for onboarding, handovers, and project transitions, it helps teams organize tasks, monitor progress, and ensure a smooth transfer of responsibilities - all in a portable, easy-to-use format.

## Current Features

- Configurable `1–8` week transition plans
- Editable weekly focus and week descriptions
- Plan edit/delete support
- Autosave for active plan metadata and daily notes
- Full backup and restore for all plans, tasks, weekly descriptions, and day notes
- Task counts and separated scheduled / ongoing / completed sections
- Day-by-day task tracker and progress charts
- Demo screen aligned with the latest workflow changes

## Feature Highlights

<p align="center">
	<img src="image/Dashboard.png" alt="Dashboard" width="600" />
	<br><br>
	<img src="image/Plan%20Dashboard.png" alt="Plan Dashboard" width="600" />
	<br><br>
	<img src="image/Task%20List.png" alt="Task List" width="600" />
	<br><br>
	<img src="image/Export%20Plan.png" alt="Export Plan" width="600" />
</p>

## Repository contents

-`Resource_transition_plan_tracker.html` — main application UI and logic

-`AGENTS.md` — repository guidance for documentation, comments, validation, and safe changes

## Tech stack

- HTML5 single-page application
- CSS3 with responsive layout, theme variables, gradients, and component styling
- Vanilla JavaScript (ES6+) for state management, form handling, rendering, and export flows
- Browser `localStorage` for client-side persistence
- JSON backup export/import for portable persistence across browser restarts or storage resets
- Chart.js for progress and status visualizations
- No backend service, package manager, or build step required

## How to use

1. Open `Resource_transition_plan_tracker.html` in a browser.
2. Create a transition plan with outgoing/incoming SA names, project, dates, and number of weeks.
3. Review the suggested weekly descriptions and change them where needed.
4. Open a plan to manage tasks, day-by-day tracking, and progress charts.
5. Use `Demo` to preview the latest sample data and screen behavior.
6. Use `Save Backup` to download a full JSON backup of all plans and `Load Backup` to restore it later.
7. Use `Export Plan` to download a portable HTML summary for the selected plan.

## Testing and validation

This project is a standalone browser app, so there is currently **no automated test runner configured**. The recommended validation approach is a focused manual smoke test.

### Happy path checks

- create a new `2-week` plan and verify the week cards appear immediately
- open the plan and add a task; confirm the task count increases in the plans table
- edit the plan and confirm the updated values persist
- launch `Demo` and confirm scheduled, ongoing, and completed plans are visible

### Edge case checks

- change the number of weeks from `1` to `8` and verify the end date/day limits update
- switch a week from `Use suggested text` to `Change it` and save custom content
- confirm task phase options only show the generated weeks for the selected plan

### Error handling checks

- try saving a plan with missing required fields and confirm the validation alert appears
- try using an end date earlier than the start date and confirm the date validation alert appears
- try adding a task without a task name and confirm the validation alert appears

## Verified status

- VS Code error check for `Resource_transition_plan_tracker.html`: **No errors found**
- Validation date: `2026-04-06`

## Author

**DJ Rajasekar**
🔗 [LinkedIn](https://www.linkedin.com/in/rajasekar-dj) &nbsp;|&nbsp; 💻 [GitHub](https://github.com/djrajasekar)
