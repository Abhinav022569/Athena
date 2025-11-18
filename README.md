# 🎓 ATHENA: Notes Sharing System

A centralized digital platform designed to streamline **academic collaboration**, **note-sharing**, and **study group management** for students and educators.

## 💻 Tech Stack & Dependencies

| Component | Technology | File Location |
| :--- | :--- | :--- |
| **Front-End** | HTML, CSS, JavaScript | `index.php`, `style.css`, `script.js` |
| **Back-End Logic** | PHP | `users/`, `admin/` directories |
| **Database** | MySQL Server | `database/athena.sql` |
| **Server** | Apache (Assumed) | N/A |

---

## ✨ Core Modules & Features

### 🧑‍🎓 User Features (Students)

| Feature | Description | Key Mechanism |
| :--- | :--- | :--- |
| **Notes Sharing** | Upload/download academic files in a centralized repository. | **Reputation System** rewards contributions. |
| **Study Groups** | Create, join, and manage groups for focused collaboration. | Uses `study_group` and `group_members` tables. |
| **Group Chat** | Real-time messaging within joined groups. | PHP scripts handle message `send_message.php`, `get_messages.php`. |
| **To-Do List** | Personal task management for organization. | Handled by `users/dashboard/to-do/` scripts. |

### 🛡️ Admin Features

| Feature | Description | Key Mechanism |
| :--- | :--- | :--- |
| **Group Control** | Approve or reject new study group creation . | `admin/dashboard/approve_group/approve_group.php`. |
| **User Moderation** | Manage user status (`active`/`banned`) and monitor activity. | `admin/dashboard/user_management/user_management.php`. |
| **Report Handling** | Review flagged content/users and mark issues as resolved. | `admin/dashboard/reports/reports.php`. |
| **Announcements**| Send targeted updates and broadcast messages to the community. | `admin/dashboard/announcements/announcements.php`. |

---

## 🚀 Installation Guide

### Prerequisites
Ensure you have a working **LAMP/XAMPP/MAMP stack** installed with **PHP** and **MySQL**.

### Quick Setup

1.  **Clone the Repository:**
    ```bash
    git clone [repository_url] athena
    cd athena
    ```

2.  **Database Import:**
    Create a MySQL database named `athena`, then import the schema:
    ```bash
    mysql -u [your_user] -p athena < database/athena.sql
    ```

3.  **Update Connection:**
    Ensure the database credentials (`localhost`, `root`, `''`, `athena` are typical defaults) are correct in:
    * `admin/connect.php`
    * `users/connect.php`

4.  **Deployment:**
    Deploy the entire `athena` file structure to your configured web server's public directory.

## 🔒 Initial Default Credentials

These are the credentials pre-loaded into the `Admin` and `Users` tables via the `athena.sql` file.

| Role | Username | Password |
| :--- | :--- | :--- |
| **Admin** | `admin` | `123` |
| **Test User** | `testuser` | `123456` |

***

*Developed by Abhinav R Nair.*
