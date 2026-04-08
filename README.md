# SA Resource Transition Plan Tracker

A lightweight single-file HTML app for planning and tracking structured onboarding and handover work between an outgoing and incoming Solutions Architect.

## Repository contents

- `Resource_transition_plan_tracker.html` — main application UI and logic
- `AGENTS.md` — repository guidance for documentation, comments, validation, and safe changes

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

## Current features

- configurable `1–8` week transition plans
- editable weekly focus and week descriptions
- plan edit/delete support
- autosave for active plan metadata and daily notes
- full backup and restore for all plans, tasks, weekly descriptions, and day notes
- task counts and separated scheduled / ongoing / completed sections
- day-by-day task tracker and progress charts
- demo screen aligned with the latest workflow changes

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
