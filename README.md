# Online Examination and Proctoring System

A modular, desktop-based online examination platform with built-in activity proctoring, built using Java Swing and file-based storage — no database required.

---

## Description

The Online Examination and Proctoring System is a Java desktop application designed to simulate a real-world examination environment for educational institutions. It provides role-based access for administrators and students, enables exam creation and management, and logs student activity during exams as a lightweight proctoring mechanism.

The project addresses the need for a simple, self-contained examination platform that can run without any database setup, using plain text and JSON files for persistent storage. It is well-suited for college-level demonstrations and academic projects.

---

## Features

- Role-based login system with separate access for Admin and Student users
- Admin panel for managing questions, viewing results, and monitoring activity logs
- Student exam interface for taking timed multiple-choice examinations
- Automatic result calculation and storage upon exam completion
- File-based proctoring log that records student activity during the exam session
- Simple, self-contained setup with no database or server required
- Modular Java package structure for easy maintenance and extension

---

## Tech Stack

| Category   | Technology                     |
|------------|-------------------------------|
| Language   | Java (100%)                   |
| GUI        | Java Swing                    |
| Storage    | File handling (JSON, TXT)     |
| Build Tool | Manual / IDE-based (javac)    |
| Data Format| JSON (users), plain text (questions, results, logs) |

---

## Project Structure

```
Online-Examination-and-Proctoring-System/
│
├── src/                        # Java source files (main application logic)
│
├── out/                        # Compiled output (.class files)
│
├── build_check/                # Build verification scripts or files
│
├── data/                       # Application data files
│   ├── users.json              # Registered user credentials and roles
│   ├── questions.txt           # Exam question bank
│   ├── results.txt             # Stored exam results for all students
│   └── activity_log.txt        # Proctoring log — records in-exam activity
│
├── docs/                       # Documentation and supporting files
│
└── README.md                   # Project overview
```

### Key Files

| File | Description |
|------|-------------|
| `data/users.json` | Stores user credentials and role assignments (Admin / Student) |
| `data/questions.txt` | Holds the exam question bank in plain text format |
| `data/results.txt` | Persists exam scores and outcomes for each student attempt |
| `data/activity_log.txt` | Proctoring log that captures student activity events during exams |

---

## Installation and Setup

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- A Java IDE (IntelliJ IDEA, Eclipse, or VS Code with Java extension) or command-line tools

### Steps

**1. Clone the repository**

```bash
git clone https://github.com/Gauravb741/Online-Examination-and-Proctoring-System.git
cd Online-Examination-and-Proctoring-System
```

**2. Compile the source files**

Using the command line from the project root:

```bash
javac -d out src/**/*.java
```

Or open the project in your preferred Java IDE and build using the built-in tools.

**3. Run the application**

```bash
java -cp out Main
```

> If the entry point class name differs, check the `src/` directory for the main class (e.g., `LoginFrame`, `Main`, or similar) and adjust the command accordingly.

---

## Usage

### Default Login Credentials

| Role    | Username  | Password  |
|---------|-----------|-----------|
| Admin   | `admin`   | `admin123` |
| Student | `student1`| `stud123`  |

### Typical Workflow

**As a Student:**
1. Launch the application.
2. Log in using your student credentials.
3. Read the exam instructions displayed before the exam begins.
4. Answer the multiple-choice questions within the allotted time.
5. Submit the exam to save your result.

**As an Admin:**
1. Launch the application.
2. Log in using the admin credentials.
3. View and manage exam questions via the admin panel.
4. Review student results stored in `data/results.txt`.
5. Check `data/activity_log.txt` to review proctoring logs for any session.

### Modifying Data Files

- To add or update questions, edit `data/questions.txt` following the existing format.
- To add new users, update `data/users.json` with the appropriate role and credentials.

---

## Screenshots / Demo

> Screenshots will be added here. To contribute screenshots, place images in the `docs/` folder and update this section.

```
[ Login Screen ]
[ Admin Dashboard ]
[ Student Exam Interface ]
[ Results View ]
```

---

## Future Improvements

- Integrate a relational database (e.g., SQLite or MySQL) to replace file-based storage for better scalability
- Add a timer display within the student exam interface
- Implement question randomization to reduce the risk of cheating
- Introduce a student registration module within the application
- Add support for multiple question types (true/false, short answer)
- Enhance the proctoring module with tab-switch detection or screenshot capture
- Migrate the GUI to JavaFX for a more modern user interface
- Add export functionality for results (PDF or CSV reports)

---

## Contributing

Contributions are welcome. To contribute:

1. Fork the repository.
2. Create a new branch for your feature or fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and commit with a clear message:
   ```bash
   git commit -m "Add: brief description of your change"
   ```
4. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a Pull Request against the `main` branch.

Please ensure your code follows standard Java naming conventions and includes comments where necessary.

---

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

You are free to use, modify, and distribute this project with attribution.

---

## Author

**Gaurav Bansod**
GitHub: [@Gauravb741](https://github.com/Gauravb741)

> This project is forked from [abhijeetd05/Online-Examination-and-Proctoring-System](https://github.com/abhijeetd05/Online-Examination-and-Proctoring-System) and extended as part of academic coursework.
