# Week 1 Assessment: Starter App Exploration

## 1. Introduction

I explored the Task Tracker starter application provided for the She Code Africa AI Software Engineering track.

The application allows users to create, manage, edit, delete and track tasks. Users can assign priorities, set due dates, mark tasks as completed and filter tasks based on their completion status.

I successfully installed the dependencies and ran the application locally.

## 2. Technologies Used

The application uses:

- **React:** Builds the interface users interact with.
- **Vite:** Runs the frontend during development.
- **Express.js:** Handles requests from the frontend.
- **Node.js:** Runs the backend JavaScript application.
- **SQLite:** Stores task information.
- **sql.js:** Allows the backend to work with SQLite using JavaScript.

## 3. Application Structure

The project is divided into two main folders:

### Client (Frontend)

This contains the part of the application users interact with.

- `App.jsx`: Contains the main interface, task list, buttons, filters and task management functions.
- `main.jsx`: Starts the React application.
- `index.html`: Provides the webpage where the application runs.
- `vite.config.js`: Configures Vite and forwards API requests to the backend.

### Server (Backend)

This handles the operations behind the application.

- `server.js`: Contains the Express server and API endpoints for creating, retrieving, updating and deleting tasks.
- `db.js`: Handles database initialization, queries and saving changes.
- `data/tasks.db`: Stores the task records.

## 4. How the Application Works

The frontend sends requests to the backend when users perform actions such as adding, editing or deleting tasks.

The backend processes these requests and communicates with the SQLite database.

For example, when a user adds a task, React sends the task details to the Express backend. The backend inserts the information into the database, saves the changes and returns the new task to the frontend.

The frontend then updates the task list.

The application uses four main API operations:

- GET: Retrieves tasks.
- POST: Creates tasks.
- PUT: Updates tasks.
- DELETE: Deletes tasks.

## 5. Improvements I Would Make

### 1. Add input validation

The application currently allows users to submit tasks with empty titles. I would introduce validation to ensure that every task has a meaningful title before it can be saved.

### 2. Improve error handling

The application does not provide sufficient feedback when requests fail. I would introduce clearer error messages so users understand when an operation is unsuccessful.

### 3. Allow users to edit all task details

The current editing feature only allows users to change a task's title. I would allow users to also update the priority and due date.

### 4. Improve mobile responsiveness

The application currently uses a fixed width of 900 pixels. I would introduce a responsive layout so the application works comfortably on mobile phones and smaller screens.

### 5. Introduce loading and success indicators

I would add loading indicators and success messages to inform users when tasks are being processed, saved or updated.

## 6. AI Tools and Prompts Used

### AI Tools

- ChatGPT: Used to understand the application structure, explain the source code, trace how the frontend communicates with the backend and identify possible improvements.

### Prompts Used

1. Examine this React, Express and SQLite task tracker project. Explain its folder structure and the purpose of each important file.

2. Explain how the React frontend works. Identify the main components, state management, event handlers and how tasks are displayed, added, updated or deleted.

3. Explain the Express backend. Identify the API endpoints, HTTP methods, request and response formats, and how the frontend communicates with the backend.

4. Explain how SQLite is used in this project. Identify the database configuration, tables and queries. Explain how tasks are saved, retrieved, updated and deleted.

5. Review this task tracker codebase. Identify realistic improvements covering code quality, usability, security, performance and reliability. Explain the problems and suggest practical improvements.

## 7. Something AI Got Wrong or Initially Missed

During the exploration, AI initially suspected that the task counter was incorrect because the interface displayed four tasks while showing only two remaining.

After inspecting the database configuration in `server/db.js`, I discovered that the first two tasks were already marked as completed in the initial database records.

I also inspected the counter calculation in `App.jsx` and confirmed that it counts only unfinished tasks.

This helped me understand the importance of checking AI explanations against the actual source code rather than accepting every suggestion without verification.

## 8. Testing

- Successfully installed project dependencies.
- Successfully started the frontend and backend.
- Opened the application in the browser.
- Tested adding tasks.
- Tested deleting tasks.
- Tested editing task titles.
- Confirmed that empty task titles are accepted, identifying an area for improvement.

