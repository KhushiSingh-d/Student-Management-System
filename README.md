# Student Management System

A menu-driven console application built with Python and SQLite for managing student records. Users can add, view, update, delete and search students from the terminal.

## Features
- Add a student (name, age, branch)
- View all students
- Update a student's age and branch by ID
- Delete a student by ID
- Search students by name (partial match, case-insensitive)

## Technologies Used
- Python 3
- SQLite (via the built-in `sqlite3` module)

## Concepts Used
- CRUD operations
- SQL queries (INSERT, SELECT, UPDATE, DELETE, LIKE)
- Parameterized queries to prevent SQL injection
- Modular programming (UI separated from database logic)
- Exception handling for invalid input (delete option)

## Project Structure
```
Student-Management-System/
├── menu.py        # Menu and user input
├── database.py    # Database table and CRUD functions
└── README.md
```

## How to Run
1. Make sure Python 3 is installed. No extra packages are needed.
2. Clone the repository:
   ```bash
   git clone https://github.com/KhushiSingh-d/Student-Management-System.git
   cd Student-Management-System
   ```
3. Run the program:
   ```bash
   python menu.py
   ```
4. Choose an option from the menu. The `student.db` file is created automatically on first run.

## Sample Output
```
------STUDENT MANAGEMENT SYSTEM------
1. Add student
2. Update student
3. View student
4. Delete student
5. Search student
6. Exit
Enter your choice: 3
(1, 'Asha', 20, 'ECE')
```

## Database Schema
| Column     | Type    | Notes                     |
|------------|---------|---------------------------|
| student_id | INTEGER | Primary key, auto-generated|
| name       | TEXT    | Required                  |
| age        | INT     |                           |
| branch     | TEXT    | Required                  |

## Limitations and Future Improvements
- Input validation is limited to the delete option; add and update would crash on non-numeric input.
- No check for duplicate students or a missing ID on update and delete.
