# Doctor Appointment Management System

A lightweight PHP + MySQL web application for managing clinic appointments, with separate workflows for **patients** and **doctors**.

## ✨ Overview

This project provides a simple appointment booking flow:
- Patients can register, sign in, view schedules, and book appointments.
- Doctors can sign in, manage available schedules, and review patient appointments.

The system is designed for classic LAMP/XAMPP-style deployments and uses server-rendered PHP pages with Bootstrap-based UI.

## 🧩 Core Features

### Patient side
- Account registration and login.
- Profile view/update.
- Browse available doctor schedule slots.
- Book appointments with symptom and comment details.
- View appointment history/list.
- Basic invoice page.

### Doctor side
- Doctor login/dashboard.
- Manage schedule slots (add/delete).
- View appointment list.
- View patient list and details.
- Mark/manage appointment states from dashboard actions.

## 🛠️ Tech Stack

- **Backend:** PHP (procedural)
- **Database:** MySQL / MariaDB
- **Frontend:** HTML, CSS, Bootstrap, jQuery
- **Session/Auth:** PHP sessions

## 📁 Project Structure

```text
.
├── index.php                 # Patient landing page (login/register)
├── adminlogin.php            # Doctor login page
├── assets/                   # Shared CSS/JS/images + DB connection
├── patient/                  # Patient module pages
├── doctor/                   # Doctor module pages
├── database/db_healthcare.sql# Main SQL schema + seed data
└── db_healthcare.sql         # Additional SQL dump copy
```

## 🚀 Getting Started

### 1) Prerequisites
- PHP 5.6+ (or newer compatible version)
- MySQL/MariaDB
- Apache (or equivalent web server)
- phpMyAdmin (optional, for easy DB import)

### 2) Clone and place project in web root

```bash
git clone <your-repo-url>
cd DoctorAppoitmint
```

If using XAMPP, place it inside:
- Windows: `C:\xampp\htdocs\DoctorAppoitmint`
- Linux: `/opt/lampp/htdocs/DoctorAppoitmint`

### 3) Create database and import schema

Create a database named `db_healthcare`, then import:
- `database/db_healthcare.sql` (recommended)

Example with MySQL CLI:

```bash
mysql -u root -p -e "CREATE DATABASE IF NOT EXISTS db_healthcare;"
mysql -u root -p db_healthcare < database/db_healthcare.sql
```

### 4) Configure database connection

Edit:
- `assets/conn/dbconnect.php`

Default local config is:
- Host: `localhost`
- User: `root`
- Password: *(empty)*
- Database: `db_healthcare`

Update credentials as needed for your environment.

### 5) Run the app

Open in browser:
- `http://localhost/DoctorAppoitmint/`

## 🔐 Default Demo Credentials

From the seed SQL data:

- **Doctor login** (`adminlogin.php`)
  - Doctor ID: `123`
  - Password: `123`

- **Patient login** (`index.php`)
  - IC Number: `920517105553`
  - Password: `123`

> You can also register a new patient account from the home page.

## 📌 Important Notes

- This is a learning/demo-style project and may require hardening before production use.
- Improve security before deployment (password hashing, prepared statements, validation, CSRF protection, etc.).
- Use environment-specific DB credentials instead of defaults.

## 🤝 Contributing

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a pull request.

## 📄 License

No explicit license file is currently included. Add a `LICENSE` file if you plan to distribute or open-source this project formally.
