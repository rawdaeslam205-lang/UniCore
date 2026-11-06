# Unicore

Unicore is a web app that gives each university student a personal, organized timetable. The student chooses university, college, year, group and section once, and sees only their own lectures and sections, with the subject, doctor or TA, time, and place.

Graduation project for the **Digital Egypt Pioneers Initiative (DEPI)** – Track: **Front-End React**.

## Team

| Name | Role |
| --- | --- |
| Rawda Eslam Mohamed | Team leader |
| Mariem Nasser Ebrahim | Front-end developer |
| Rawan Ahmed Abdelhamed | Front-end developer |
| Bassant Hamdy Abdelhalim | UI/UX and front-end developer |
| Khaled Reda Mohamed | Front-end developer |

## Features

- Select university, college, year, group and section
- Personal timetable by day (subject, doctor/TA, time, lecture or section, place)
- Reminders before a lecture or section, with a lead time you choose
- Faculty guide: amphitheaters, halls and labs with directions
- Search for a doctor or TA
- Exam schedule and announcements about changes
- Responsive, mobile-first interface

The first version starts with Benha University and one faculty. Faculties and universities come from the API, so more can be added without changing the code.

## Screenshots

Add screenshots of the selection screen, timetable, faculty guide and search here.

## Tech stack

| Layer | Technology |
| --- | --- |
| Front end | React, React Router |
| State and data | React hooks, Context (or Redux Toolkit), fetch (or Axios) |
| Back end and database | Provided ready by the track (REST API) |
| Notifications | Browser Notifications API |
| Testing | Jest, React Testing Library |
| Version control | Git, GitHub |

> Confirm this list with the team and edit it to match what the project really uses.

## System requirements

- Node.js (current LTS version) and npm
- A modern browser (latest Chrome, Edge, Firefox or Safari)
- Access to the back-end API (URL provided by the back-end team)

## Installation

```bash
git clone <repository-url>
cd unicore
npm install
```

## Configuration

Copy the example environment file and set the API address:

```bash
cp .env.example .env
```

`.env`:

```
# Use the variable name that matches your build tool
VITE_API_URL=https://your-backend-url/api
# For Create React App use: REACT_APP_API_URL=https://your-backend-url/api
```

Never commit the `.env` file or any secret to GitHub.

## Run locally

```bash
npm run dev
```

(With Create React App use `npm start`.) Open the address shown in the terminal.

## Run the tests

```bash
npm test
```

## Build for production

```bash
npm run build
```

The built files are in the `dist` folder (`build` with Create React App). Upload them to any static hosting service.

## Live demo

<deployment-link>

## Project structure

```text
unicore/
  public/
  src/
    assets/
    components/   reusable UI
    pages/        SelectGroup, Timetable, FacultyGuide, StaffSearch, Exams, Announcements, Settings
    hooks/        custom hooks (useSelection, useTimetable, useReminders)
    services/     api, notifications, storage
    context/      shared state
    utils/        helpers
    routes/
  tests/
  docs/           project documentation, diagrams, wireframes
  .env.example
  README.md
```

## API documentation

The app uses these endpoints from the ready back end. Replace the placeholder paths with the real ones.

| Method | Endpoint | Purpose |
| --- | --- | --- |
| GET | /universities | List universities |
| GET | /universities/{id}/colleges | List colleges |
| GET | /colleges/{id}/years | List academic years |
| GET | /years/{id}/groups | List groups and sections |
| GET | /timetable?groupId=&sectionId= | Personal timetable |
| GET | /staff?search= | Search doctors and TAs |
| GET | /colleges/{id}/places | Faculty guide |
| GET | /exams?yearId=&groupId= | Exam schedule |
| GET | /announcements?collegeId= | Announcements |

## Git workflow

- `main`: stable and deployed
- `develop`: integration branch
- `feature/<name>`: one branch per task, merged by pull request after a review

Commit messages: `feat: add section selector`, `fix: wrong day order`.

## Documentation

All project documents are in the [`docs`](docs) folder:

1. Project Planning & Management
2. Literature Review
3. Requirements Gathering
4. System Analysis & Design
5. Implementation
6. Testing & Quality Assurance
7. Final Presentation & Reports

## License

Educational project for DEPI. Add a license here if the team decides to publish it.
