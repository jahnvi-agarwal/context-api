# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.


# React Context API with Local storage Todo App

A simple yet effective Todo application built with React, leveraging the Context API for state management and local storage for data persistence. This project demonstrates a clean architecture for managing application-wide state without prop drilling.

## Features

* **Add Todos**: Easily add new tasks to your list.
* **Edit Todos**: Modify existing tasks.
* **Delete Todos**: Remove tasks you no longer need.
* **Toggle Complete**: Mark tasks as complete or incomplete.
* **Persistent Storage**: Your todos are saved in your browser's local storage, so they'll be there even after you close and reopen the browser.
* **Context API**: Efficient state management using React's Context API.
* **Responsive Design**: A clean and simple UI that works well on different screen sizes.

## Technologies Used

* React
* Tailwind CSS (for styling - as indicated by class names like `bg-[#172842]`, `rounded-lg`, etc.)

## Project Structure

The project is structured to promote modularity and reusability:

* `src/App.jsx`: The main application component that manages the overall todo state, including `addTodo`, `updateTodo`, `deleteTodo`, and `toggleComplete` functions. It also handles local storage interactions using `useEffect`.
* `src/context/TodoContext.js`: Defines the `TodoContext` using `createContext`, provides a `useTodo` custom hook for easy consumption, and exports `TodoProvider`.
* `src/components/TodoForm.jsx`: A functional component responsible for rendering the input field and add button for creating new todos. It uses the `useTodo` hook to access the `addTodo` function.
* `src/components/TodoItem.jsx`: Represents an individual todo item, including its text, a checkbox for completion, and buttons for editing/saving and deleting. It utilizes `useTodo` for `updateTodo`, `deleteTodo`, and `toggleComplete` functionalities.
* `src/components/index.js`: A barrel file to simplify imports of `TodoForm` and `TodoItem`.

## How to Run Locally

1.  **Clone the repository:**
    ```bash
    git clone 
    cd 
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    # OR
    yarn install
    ```
3.  **Start the development server:**
    ```bash
    npm run dev
    # OR
    yarn dev
    ```
    This will typically open the application in your browser at `http://localhost:5173/` (or a similar port).

## Usage

* Type your todo in the input field and click "Add" or press Enter.
* Click the checkbox next to a todo to mark it as complete/incomplete.
* Click the "✏️" icon to edit a todo. After editing, click the "📁" icon to save changes.
* Click the "❌" icon to delete a todo.

## Contributing

Feel free to fork the repository, make improvements, and submit pull requests.

## License

This project is open source and available under the [MIT License](LICENSE).
