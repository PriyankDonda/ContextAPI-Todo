# Context API Todo App

A simple and modern Todo application built with **React**, leveraging the **Context API** for state management. This project demonstrates how to use React Context to manage and share state across components, with persistent storage using the browser's LocalStorage.

---

## Features

- Add new todos
- Edit existing todos (inline editing)
- Mark todos as complete/incomplete
- Delete todos
- Persistent storage (todos are saved in LocalStorage)
- Responsive and clean UI with TailwindCSS

---

## Tech Stack

- [React](https://react.dev/)
- [Vite](https://vitejs.dev/) (for fast development)
- [TailwindCSS](https://tailwindcss.com/) (utility-first CSS)
- **React Context API** (for global state management)
- LocalStorage (for persistence)

---

## Folder Structure

```
src/
  App.jsx                # Main app component
  main.jsx               # Entry point
  App.css, index.css     # Styles (Tailwind imported in index.css)
  assets/                # Static assets (e.g., react.svg)
  components/
    TodoForm.jsx         # Form to add todos
    TodoItem.jsx         # Single todo item (edit, complete, delete)
    index.js             # Components barrel export
  context/
    TodoContext.js       # Context API setup (provider, hook)
    index.js             # Context barrel export
public/
  vite.svg               # App favicon/logo
index.html               # HTML template
```

---

## How Context API is Used

- The `TodoContext` provides the todo list and all actions (add, update, delete, toggle complete) to any component in the app.
- The `TodoProvider` wraps the app in `App.jsx`, making todos and actions available via the `useTodo` hook.
- Components like `TodoForm` and `TodoItem` consume the context to interact with the todo list.

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd contextapi-todo
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

### Running Locally

Start the development server:

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser to see the app.

---

## Usage

- **Add Todo:** Type in the input and click "Add".
- **Edit Todo:** Click the ✏️ icon, modify the text, then click 📁 to save.
- **Complete Todo:** Check the box to mark as complete (turns green).
- **Delete Todo:** Click the ❌ icon.
- Todos persist even after refreshing the page.

---

## Customization

- **Styling:** Uses TailwindCSS. Modify `src/index.css` or component classes for custom styles.
- **Logic:** Extend the context in `src/context/TodoContext.js` for more features (e.g., filtering, priorities).
- **Components:** Add new components in `src/components/` as needed.

---

## License

This project is for learning and demonstration purposes.
