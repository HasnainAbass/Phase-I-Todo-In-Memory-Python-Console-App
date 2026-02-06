# Quickstart Guide: Phase-I In-Memory Python Console-Based Todo Application

## Prerequisites
- Python 3.13+ installed
- UV package manager installed

## Setup
1. Clone the repository
2. Navigate to the project directory
3. Install dependencies with UV: `uv sync`
4. Activate the virtual environment: `source .venv/bin/activate` (Linux/Mac) or `source .venv/Scripts/activate` (Windows)

## Running the Application
Execute the main CLI application:
```
python -m src.todo_app.main
```

## Basic Usage
1. Run the application to see the main menu
2. Choose options 1-5 to perform tasks:
   - Add new tasks with titles and optional descriptions
   - View all tasks with their status
   - Update existing tasks by ID
   - Delete tasks by ID
   - Mark tasks as complete/incomplete
3. Enter 'quit' or 'exit' to close the application

## Example Workflow
1. Add a task: Select option 1, enter "Buy groceries" as title
2. View tasks: Select option 2 to see all tasks
3. Mark complete: Select option 5, enter the task ID to toggle status
4. Exit: Type 'quit' when done