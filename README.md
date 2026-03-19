# STUDBUD

![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

> An all-in-one student productivity dashboard with subject tracking, grade analysis, Pomodoro timer, to-do lists, and a Jarvis chatbot.

## About

STUDBUD is a feature-rich student productivity web application built with React and TypeScript. It combines essential study tools into a single dashboard — manage subjects and grades, track study sessions with a Pomodoro timer, organize tasks with a to-do list, get inspired with daily quotes, and interact with a Jarvis-like chatbot assistant. Integrates with Google Drive and Google Calendar for seamless workflow. Supports dark mode for late-night study sessions.

## Tech Stack

- **Frontend:** React 18, TypeScript
- **Build Tool:** Vite
- **Styling:** Tailwind CSS
- **Charts:** Chart.js + react-chartjs-2
- **Icons:** Lucide React
- **Backend:** Firebase
- **Linting:** ESLint

## Features

- **Subject management** — add, edit, and delete subjects with grade tracking
- **Grade analysis** — visual grade breakdown with Chart.js charts
- **Pomodoro timer** — built-in study timer with start/pause/reset (also controllable by chatbot)
- **To-do list** — task management to stay organized
- **Jarvis chatbot** — AI assistant that can toggle dark mode and control the Pomodoro timer
- **Daily quotes** — motivational quote display
- **Google Drive integration** — quick-access button to open Google Drive
- **Google Calendar integration** — quick-access button to open Google Calendar
- **Dark mode** — toggle with persistence via localStorage
- **Responsive design** — works on desktop and mobile

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Installation

```bash
git clone https://github.com/iampreetdave/STUDBUD.git
cd STUDBUD
npm install
```

### Run

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build

```bash
npm run build
```

## How It Works

The app is a single-page React application bootstrapped with Vite. State is managed with React hooks (`useState`, `useEffect`). The Pomodoro timer communicates with the Jarvis chatbot via custom DOM events (`CustomEvent`). Google Drive and Calendar are opened in persistent browser tabs that are reused on subsequent clicks. Dark mode preference is stored in `localStorage`. Firebase handles backend data persistence.

## Project Structure

```
STUDBUD/
├── src/
│   ├── App.tsx              # Main app with routing and state
│   ├── main.tsx             # Entry point
│   ├── types.ts             # TypeScript type definitions
│   ├── components/          # UI components
│   │   ├── PomodoroTimer    # Study timer
│   │   ├── TodoList         # Task management
│   │   ├── SubjectForm      # Subject input
│   │   ├── SubjectList      # Subject display
│   │   ├── GradeAnalysis    # Charts & grade breakdown
│   │   ├── EditModal        # Subject editing modal
│   │   ├── DarkModeToggle   # Theme switcher
│   │   ├── QuoteBox         # Daily quotes
│   │   └── ChatBot          # Jarvis AI assistant
│   └── firebase.ts/         # Firebase configuration
├── index.html
├── package.json
├── vite.config.ts
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

## License

This project is licensed under the [MIT License](LICENSE).
