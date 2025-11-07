# Django To-Do List Application

A simple and elegant To-Do List web application built with Django that demonstrates full CRUD (Create, Read, Update, Delete) functionality.

## Features

- ✅ **Create Tasks**: Add new tasks with title, description, and completion status
- 📋 **View Tasks**: See all your tasks in a beautiful list view
- 🔍 **Task Details**: View complete details of individual tasks
- ✏️ **Edit Tasks**: Update task information and mark as complete/incomplete
- 🗑️ **Delete Tasks**: Remove tasks with confirmation
- 🎨 **Beautiful UI**: Modern, responsive design with gradient background
- ⏰ **Automatic Timestamps**: Tasks are automatically timestamped when created

## Project Structure

```
BIA_Sem-3_12_Dhruval Rana_EDA/
├── todoproject/              # Main project directory
│   ├── settings.py          # Project settings
│   ├── urls.py              # Main URL configuration
│   └── ...
├── todo/                     # Todo app directory
│   ├── models.py            # Task model definition
│   ├── views.py             # Class-based views for CRUD operations
│   ├── urls.py              # App URL patterns
│   ├── admin.py             # Admin panel configuration
│   ├── templates/           # HTML templates
│   │   └── todo/
│   │       ├── base.html           # Base template with styling
│   │       ├── task_list.html      # List view template
│   │       ├── task_detail.html    # Detail view template
│   │       ├── task_form.html      # Create/Update form template
│   │       └── task_confirm_delete.html  # Delete confirmation template
│   └── migrations/          # Database migrations
├── manage.py                # Django management script
├── requirements.txt         # Python dependencies
└── db.sqlite3              # SQLite database (created after migration)
```

## Model Definition

The `Task` model includes:
- **title**: CharField (max 200 characters) - Task title
- **description**: TextField (optional) - Detailed description
- **completed**: BooleanField (default: False) - Completion status
- **created_at**: DateTimeField (auto) - Creation timestamp

## URL Patterns

- `/` - List all tasks (TaskListView)
- `/task/<id>/` - View task details (TaskDetailView)
- `/task/new/` - Create a new task (TaskCreateView)
- `/task/<id>/edit/` - Edit an existing task (TaskUpdateView)
- `/task/<id>/delete/` - Delete a task (TaskDeleteView)

## Setup Instructions

### 1. Prerequisites
Make sure you have Python installed:
```bash
python --version
```

### 2. Navigate to Project Directory
```bash
cd "d:\BIA\Sem - 3\Internal\BIA_Sem-3_12_Dhruval Rana_EDA"
```

### 3. Create Virtual Environment (Recommended)
It's recommended to use a virtual environment to isolate project dependencies:

**For Windows (PowerShell):**
```bash
# Create virtual environment
python -m venv env

# Activate virtual environment
.\env\Scripts\Activate.ps1
```

**For Windows (Command Prompt):**
```bash
# Create virtual environment
python -m venv env

# Activate virtual environment
env\Scripts\Activate
```



> **Note:** After activation, you should see `(venv)` at the beginning of your command prompt.

### 4. Install Dependencies
Install all required packages from requirements.txt:
```bash
pip install -r requirements.txt
```

This will install:
- Django 4.2.7
- asgiref 3.7.2
- sqlparse 0.4.4
- tzdata 2023.3

### 5. Apply Database Migrations
Run migrations to create the database tables:
```bash
python manage.py migrate
```

### 5. Run the Development Server
```bash
python manage.py runserver
```

### 6. Access the Application
Open your web browser and go to:
```
http://127.0.0.1:8000/
```

### 7. (Optional) Create Admin User
To access the Django admin panel:
```bash
python manage.py createsuperuser
```

``` super user Credential is
Username : Dhruval
Password : Pass@123
```

Then visit: `http://127.0.0.1:8000/admin/`

## Quick Start (Summary)

```bash
# Navigate to project directory
cd "d:\BIA\Sem - 3\Internal\BIA_Sem-3_12_Dhruval Rana_EDA"

# Create and activate virtual environment (Windows PowerShell)
python -m venv venv
.\venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start server
python manage.py runserver

# Open browser to http://127.0.0.1:8000/
```

## Usage Guide

### Creating a Task
1. Click on "Add New Task" button
2. Fill in the task title (required)
3. Optionally add a description
4. Check "Mark as completed" if the task is already done
5. Click "Create Task"

### Viewing Tasks
- The home page displays all tasks
- Completed tasks are marked with a green indicator
- Pending tasks are marked with a yellow indicator
- Each task shows its creation date and time

### Editing a Task
1. Click "View" on any task or go to task details
2. Click "Edit Task"
3. Modify the fields as needed
4. Click "Update Task"

### Deleting a Task
1. Click "Delete" on any task
2. Confirm the deletion on the confirmation page
3. The task will be permanently removed

## Technologies Used

- **Backend**: Django 4.2.7
- **Database**: SQLite3
- **Frontend**: HTML5, CSS3 (inline styles)
- **Template Engine**: Django Templates
- **Views**: Django Class-Based Views (CBVs)

## Key Concepts Demonstrated

1. **Models**: Django ORM with field types (CharField, TextField, BooleanField, DateTimeField)
2. **Views**: Class-Based Views (ListView, DetailView, CreateView, UpdateView, DeleteView)
3. **Templates**: Template inheritance, template tags, and filters
4. **URLs**: URL routing and reverse URL lookup
5. **Forms**: Django ModelForm with validation
6. **Admin**: Custom admin configuration

## Development Notes

- The application uses Django's built-in class-based views for cleaner code
- Template inheritance is used to maintain consistent styling
- The database uses SQLite for simplicity (suitable for development)
- CSRF protection is enabled for form submissions
- The Task model is ordered by creation date (newest first)

## Future Enhancements

Possible improvements for this application:
- Add user authentication
- Implement task categories/tags
- Add due dates and reminders
- Include search and filter functionality
- Add task priority levels
- Implement task sorting and pagination

## Author

**Dhruval Rana**  
## License

This is an educational project created for learning purposes.

