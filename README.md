# SA Resource Transition Plan

A single-page HTML application to manage outgoing/incoming SA transition plans, tasks, daily tracking, and progress charts.

## Project Files

- `sa_resource_transition_plan - Claude - v2.html`: Main application
- `requirements.txt`: Project runtime requirements (this file)

## Features

- Create and manage transition plans
- Prevent duplicate plans for the same outgoing/incoming pair
- Add, edit, and delete tasks per plan
- Day-by-day task tracking with calendar/day selection
- Progress and chart views for plan status
- Demo mode with clear visual indicator
- Export opened plan to shareable HTML
- Local browser persistence using `localStorage`

## How To Run

1. Open `sa_resource_transition_plan - Claude - v2.html` in a browser.
2. Create a plan from the Plans tab.
3. Open the plan to manage tasks, day-by-day, and progress.

## Data Persistence

- App data is stored in browser `localStorage`.
- Data is retained across refresh/reopen on the same browser profile.
- Clearing browser site data/localStorage removes saved plans and tasks.

## Export

- Open a plan.
- Click **Export Plan**.
- A standalone, shareable HTML file is downloaded with all plan and task details.

## Notes

- This is a static client-side app.
- No server or database is required.
