# Task-Manager-App
Task Manager API
This is a simple Task Manager API built with Express.js and MongoDB. It includes functionality for managing tasks, sub-tasks, and users, as well as authentication using JWT tokens.

Features
Create Task:

Input: Title, Description, Due Date with JWT Auth Token.
Create Subtask:

Input: Task ID, Title
Get User Tasks:

Filter: Priority, Due Date.
Pagination.
Get User Subtasks:

Filter: Task ID.
Update Task:

Update Due Date.
Update Status ("TODO" or "DONE").
Update Subtask:

Update Status (0 or 1).
Delete Task:

Soft Deletion.
Delete Subtask:

Soft Deletion.
Models
Sub Task
id (int, unique identifier)
task_id (int) // references task table
title (String)
status (0, 1) // 0 - incomplete, 1 - complete
created_at (date/string)
updated_at (date/string)
deleted_at (date/string)
User
id (int, unique identifier)
phone_number (num)
password (String)
priority (0, 1, 2) // for Twilio calling priority
Task
Additional Fields: Title, Description, Due Date, Priority, Status
Getting Started
Clone the repository.
Install dependencies: npm install.
Set up MongoDB and update the connection string in the code.
Run the server: npm start.
API Endpoints
Tasks
POST /api/tasks/ - Create Task.
POST /api/subtasks/ - Create Subtask.
GET /api/tasks/ - Get User Tasks.
GET /api/subtasks/ - Get User Subtasks.
PUT /api/tasks/update/:taskId - Update Task.
PUT /api/subtasks/update/:subtaskId - Update Subtask.
DELETE /api/tasks/delete/:taskId - Delete Task.
DELETE /api/subtasks/delete/:subtaskId - Delete Subtask.
Users
POST /api/users/register - Register User.
POST /api/users/login - User Login.
Usage
Register and login to get the JWT Auth Token.
Use the token for authenticated requests to tasks and subtasks endpoints.
Author
This Task Manager API was created by [Samriddhi Singh].
