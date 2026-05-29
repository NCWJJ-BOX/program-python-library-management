# Library Management System

Desktop library management application with PyQt6 GUI and SQLite database. Manages books, users, and loan operations.

## Features

- **Books:** Add/edit/delete, search by title/author/isbn, availability status
- **Users:** Add/edit/delete, search
- **Loans:** Checkout with due dates (default 14 days), return tracking, filter by open/all/user
- **Tools:** CSV import/export for books and users, database backup/restore
- Seed data with 5 classic books on first run
- ISBN uniqueness enforcement, prevents deletion of checked-out books

## Tech Stack

- Python 3.10+, PyQt6, SQLite

## Project Structure

```
program-python-library-management/
├── library_management/
│   ├── main.py           # CLI entry point with argparse
│   ├── qt_app.py         # PyQt6 GUI application
│   ├── db.py             # Database layer (SQLite CRUD)
│   └── errors.py         # Custom exceptions
├── "library management.py"   # Alternate entry script
├── img/                  # Screenshots
├── requirements.txt
└── pyrightconfig.json
```

## Setup

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python "library management.py"
```

Optional custom database path:

```bash
python "library management.py" --db ./data/library.db
```

## Dependencies

- `PyQt6>=6.6`
