🎓 ATHENA: Notes Sharing System

A centralized digital platform designed to streamline academic collaboration, note-sharing, and study group management for students and educators [cite: uploaded:abhinav022569/athena/Athena-5d6698f5a184b705fc2e9cd4b40b693186618e9d/Documents/ATHENA - Notes Sharing System.docx].

💻 Tech Stack & Dependencies

Component

Technology

File Location

Front-End

HTML, CSS, JavaScript

index.php, style.css, script.js

Back-End Logic

PHP

users/, admin/ directories

Database

MySQL Server

database/athena.sql

Server

Apache (Assumed)

N/A

✨ Core Modules & Features

🧑‍🎓 User Features (Students)

Feature

Description

Key Mechanism

Notes Sharing

Upload/download academic files in a centralized repository.

Reputation System rewards contributions [cite: uploaded:abhinav022569/athena/Athena-5d6698f5a184b705fc2e9cd4b40b693186618e9d/users/dashboard/chat_box/upload_file.php].

Study Groups

Create, join, and manage groups for focused collaboration.

Uses study_group and group_members tables.

Group Chat

Real-time messaging within joined groups.

PHP scripts handle message send_message.php, get_messages.php.

To-Do List

Personal task management for organization.

Handled by users/dashboard/to-do/ scripts.

🛡️ Admin Features

Feature

Description

Key Mechanism

Group Control

Approve or reject new study group creation requests.

admin/dashboard/approve_group/approve_group.php.

User Moderation

Manage user status (active/banned) and monitor activity.

admin/dashboard/user_management/user_management.php.

Report Handling

Review flagged content/users and mark issues as resolved.

admin/dashboard/reports/reports.php handles status.

Announcements

Send targeted or mass communication to users.

admin/dashboard/announcements/announcements.php.

🚀 Installation Guide

Prerequisites

Ensure you have a working LAMP/XAMPP/MAMP stack installed with PHP and MySQL [cite: uploaded:abhinav022569/athena/Athena-5d6698f5a184b705fc2e9cd4b40b693186618e9d/Documents/ATHENA - Notes Sharing System.docx].

1. Database Setup

Create a new MySQL database named athena.

Import the schema:

mysql -u [your_user] -p athena < database/athena.sql


2. Configure Connections

Update the database connection details in both configuration files to match your MySQL credentials (localhost, root, '', athena are defaults):

Admin Connection: admin/connect.php

<?php
$conn = new mysqli('localhost', 'root', '', 'athena');
// ...


User Connection: users/connect.php

<?php
$conn = new mysqli('localhost', 'root', '', 'athena');
// ...


3. Deployment

Place the entire athena folder into your web server's public directory (e.g., htdocs or www).

Ensure correct file permissions for the upload directories (user_files/notes/ and user_files/profile_pics/).

Access the application via your browser: http://localhost/athena/index.php.

🔒 Default Credentials

Role

Username

Password

Admin

admin

123

Test User

testuser

123456

Developed by Abhinav R Nair
