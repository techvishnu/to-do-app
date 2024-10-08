# Java Todo Application

A simple command-line Todo application built using Core Java. This app allows users to add, update, delete, and list tasks, making it an efficient tool to manage daily tasks with data persistence.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Add a Task](#add-a-task)
  - [Update a Task](#update-a-task)
  - [Delete a Task](#delete-a-task)
  - [List Tasks](#list-tasks)
- [File Structure](#file-structure)
- [Data Persistence](#data-persistence)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Add Task**: Create a new task with a description and category (Personal, Work, Hobby, Other).
- **Update Task**: Modify an existing task’s description, category, and completion status.
- **Delete Task**: Remove a task by its unique ID.
- **List Tasks**: View all tasks with their details such as ID, description, category, and completion status.
- **Data Persistence**: Tasks are saved to a file (`tasks.dat`) and loaded automatically when the application starts again.

## Installation

### Prerequisites
- **Java Development Kit (JDK)**: Ensure that JDK 8 or later is installed on your system.
- **IDE (IntelliJ IDEA or Eclipse)**: Recommended to run the project easily.

### Steps to Run the Project
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/java-todo-app.git
   ```
2. **Open the Project in your preferred IDE (IntelliJ IDEA is recommended).**

3. **Build the Project:**
   - Open the project in IntelliJ.
   - Build the project using `Build -> Build Project` to compile all the files.

4. **Run the Application:**
   - Right-click the `Main.java` file and select `Run Main`.

## Usage
Upon running the application, you will be presented with a simple menu for interacting with the tasks:

```
To-Do List Application
1. Add Task
2. Update Task
3. Delete Task
4. List Tasks
5. Exit
Enter your choice:
```

### Add a Task
- Select option 1 from the menu.
- Provide a description and select a category (PERSONAL, WORK, HOBBY, OTHER).

Example:

```
Enter task description: Complete Java Project
Enter task category (PERSONAL, WORK, HOBBY, OTHER): WORK
Task added successfully.
```

### Update a Task
- Select option 2 from the menu.
- Enter the ID of the task to be updated.
- Provide the new description, category, and whether the task is completed or not.

Example:

```
Enter task ID: 1
Enter new description: Finalize Java App
Enter new category (PERSONAL, WORK, HOBBY, OTHER): WORK
Is the task completed? (true/false): true
Task updated successfully.
```

### Delete a Task
- Select option 3 from the menu.
- Enter the ID of the task to be deleted.

Example:

```
Enter task ID: 1
Task deleted successfully.
```

### List Tasks
- Select option 4 to see all tasks currently in the list.

Example output:

```
Task{id=1, description='Finalize Java App', category=WORK, isCompleted=true}
Task{id=2, description='Study for exam', category=PERSONAL, isCompleted=false}
```

Exit the Application
- Select option 5 to exit the program.

## File Structure
arduino
Copy code
src/
│
├── net/javaguides/todo/
│   ├── Main.java        // Entry point of the application with user interface
│   ├── Task.java        // Task model class
│   ├── TaskManager.java // Manages tasks (CRUD operations + file handling)
│   └── Category.java    // Enum for task categories
│
├── tasks.dat            // Serialized data for saving tasks (auto-generated)
│
├── README.md            // Project documentation

## Data Persistence
Tasks are saved to a file named tasks.dat located in the project directory. This file is automatically created when you add tasks, and it ensures that your tasks are preserved between sessions.

Saving Tasks: Tasks are serialized and saved to tasks.dat every time a new task is added, updated, or deleted.
Loading Tasks: When the application starts, it reads tasks from tasks.dat to ensure that previous tasks are loaded.

## Contributing
Contributions are welcome! If you find a bug or want to add a feature, feel free to submit an issue or pull request.

Steps to Contribute:
Fork the project.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit your changes (git commit -m 'Add some feature').
Push to the branch (git push origin feature-branch).
Open a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
