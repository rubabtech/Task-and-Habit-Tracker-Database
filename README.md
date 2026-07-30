# ✅ Task and Habit Tracker Database

Task and Habit Tracker is a MySQL database project designed to manage users' daily tasks, habits, goals, reminders, progress, notifications, and habit streaks.

The project demonstrates practical implementation of database concepts, including database design, relationships, DDL commands, DML queries, joins, nested queries, views, and stored procedures.

## 📌 Project Overview

Managing daily tasks and maintaining consistent habits can become difficult without an organized system.

The Task and Habit Tracker database provides a structured solution where users can:

- Create and manage tasks
- Organize tasks into categories
- Set task priorities and deadlines
- Create and track habits
- Record daily habit completion
- Create personal goals
- Monitor goal progress
- Set task reminders
- Receive notifications
- Track current and maximum habit streaks

## 🎯 Project Objectives

- Design a structured relational database.
- Store user tasks, habits, goals, and progress.
- Demonstrate primary and foreign key relationships.
- Perform CRUD operations using SQL.
- Retrieve meaningful information using SQL queries.
- Apply different types of joins.
- Use nested and aggregate queries.
- Implement reusable stored procedures.
- Create views for simplified data retrieval.

## 🛠️ Technologies Used

- **Database:** MySQL
- **Database Tool:** MySQL Workbench
- **Query Language:** SQL
- **Documentation:** Microsoft Word
- **Design:** ER Diagram and Relational Schema

## 🗄️ Database Tables

The database contains the following tables:

| Table | Purpose |
|---|---|
| `User` | Stores registered user information |
| `Category` | Stores task categories |
| `Task` | Stores user tasks, deadlines, status and priority |
| `Habit` | Stores habits created by users |
| `Habit_Tracking` | Records daily habit completion |
| `Reminder` | Stores reminders associated with tasks |
| `Goal` | Stores user goals and target dates |
| `Progress` | Records progress made toward goals |
| `Notification` | Stores notifications for users |
| `Streak` | Stores current and maximum habit streaks |

## 🔗 Main Database Relationships

- One user can create multiple tasks.
- One user can create multiple habits.
- One user can create multiple goals.
- One user can receive multiple notifications.
- One category can contain multiple tasks.
- One habit can contain multiple tracking records.
- One habit can have streak information.
- One task can have one or more reminders.
- One goal can contain multiple progress records.

## 📐 Database Design

The project documentation includes:

- Entity Relationship Diagram
- Relational Schema
- Primary Keys
- Foreign Keys
- Table relationships
- Database constraints

## 🧱 DDL Operations

The project contains `CREATE TABLE` queries for all database entities.

Example:

```sql
CREATE TABLE Task (
    TaskID INT PRIMARY KEY,
    UserID INT,
    CategoryID INT,
    Title VARCHAR(100),
    Description VARCHAR(255),
    DueDate DATE,
    Status VARCHAR(20),
    Priority VARCHAR(20),
    FOREIGN KEY (UserID) REFERENCES User(UserID),
    FOREIGN KEY (CategoryID) REFERENCES Category(CategoryID)
);
