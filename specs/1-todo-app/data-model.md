# Data Model: Phase-I In-Memory Python Console-Based Todo Application

## Task Entity

**Attributes:**
- `id`: UUID string (unique identifier, generated automatically)
- `title`: String (required, non-empty)
- `description`: String (optional, can be empty)
- `completed`: Boolean (default: False)

**Validation Rules:**
- `id` must be unique across all tasks
- `title` must be a non-empty string
- `completed` must be a boolean value

**State Transitions:**
- `incomplete` → `complete` (when user marks task as complete)
- `complete` → `incomplete` (when user marks task as incomplete)

## TaskManager Entity

**Responsibilities:**
- Store and manage all Task objects in memory
- Handle CRUD operations for tasks
- Maintain unique ID assignment

**Operations:**
- `add_task(title, description)` → Task (creates and stores a new task)
- `get_task(task_id)` → Task (retrieves a specific task)
- `get_all_tasks()` → List[Task] (returns all tasks)
- `update_task(task_id, title=None, description=None)` → Task (updates a task)
- `delete_task(task_id)` → Boolean (removes a task)
- `toggle_task_status(task_id)` → Task (toggles completion status)

**Relationships:**
- Contains zero-to-many Task entities