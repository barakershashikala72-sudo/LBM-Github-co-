# Library Project :full stack implementaton(made with github copilot)

###photo

<img width="977" height="617" alt="Screenshot 2026-05-18 110031" src="https://github.com/user-attachments/assets/c338a25b-a7d6-4a03-8227-0de2d22e5725" />


A lightweight Django library application that exposes a REST API for managing books and includes a simple frontend home page.

## What is an Application?

An application is software designed to perform specific tasks for users. In this project, the Django application provides book management functionality, including storing book details, displaying a home page, and offering an admin interface.

## What is an API?

API stands for Application Programming Interface. An API defines a set of rules that lets one piece of software communicate with another. In this project, the REST API allows clients to list, create, retrieve, update, and delete book records over HTTP.

## Key Features

- Django application with SQLite database
- Django REST Framework API for `Book` objects
- CRUD operations: create, read, update, delete
- Custom endpoints for available books and toggling availability
- Home page available at `/`
- Django admin available at `/admin/`

## Project Structure

- `manage.py` - Django command-line utility
- `library_project/` - Django project configuration
- `books/` - application logic for book management
- `templates/` - HTML templates
- `static/` - static assets
- `db.sqlite3` - SQLite database file

## API Basics

### Core API Endpoints

- `GET /api/books/` - List all books
- `POST /api/books/` - Create a new book
- `GET /api/books/{id}/` - Retrieve a single book by ID
- `PUT /api/books/{id}/` - Replace an existing book
- `PATCH /api/books/{id}/` - Partially update a book
- `DELETE /api/books/{id}/` - Delete a book

### Custom API Actions

- `GET /api/books/available/` - List books where `is_available` is `true`
- `POST /api/books/{id}/toggle_availability/` - Toggle availability for a specific book

### Additional Routes

- `/` - Render the home page
- `/admin/` - Django admin interface

## Setup Instructions

### 1. Create a virtual environment

Open PowerShell in the project folder and run:

```powershell
python -m venv venv
```

### 2. Activate the virtual environment

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Apply database migrations

```powershell
python manage.py migrate
```

### 5. Run the development server

```powershell
python manage.py runserver
```

Then open `http://127.0.0.1:8000/` in your browser.

## Understanding This API

This project exposes a REST API endpoint at `/api/books/` for managing book data.

- An `application` is the complete software system running on Django.
- An `API` is a contract that defines how external programs can access the application data.
- Clients send HTTP requests to the API and receive JSON responses.

## Notes

- The database is SQLite and stored in `db.sqlite3`.
- The project uses Django REST Framework for its API layer.
- If you want a production deployment, disable `DEBUG` and configure allowed hosts, static files, and a production database.
