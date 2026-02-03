# MS CARE — Hospital Appointment Management 🏥🩺

> A simple hospital appointment and management system (PHP + MySQL) — cleaned up and documented.

## 🚀 Project Overview

MS CARE is a PHP-based web application for managing hospital appointments, doctor availability, patient feedback, and basic admin/doctor/patient workflows. The project contains frontend pages, PHP server-side logic, and a SQL dump to create the database schema and seed some example data.

Key features:
- Book and manage appointments
- Admin dashboard for appointments and feedback
- Doctor availability management
- Patient feedback submission and admin moderation
- Basic user authentication and password reset support

## 🧭 Quicklinks (important files)
- Main entry: `index.html`
- SQL schema & data: `hospital_management (2).sql`
- Admin pages: `Admin/` (dashboard, appointment management, user-management)
- Appointment flow: `appointment/` (book_appointment.php, submit_appointment.php, get_slots.php)
- Account pages: `Create an Account/` (login.php, signup.php)
- Doctor area: `doctor/`
- Patient pages: `patient/`

## 🛠️ Tech Stack
- PHP (server-side)
- MySQL / MariaDB (database)
- HTML, CSS, JavaScript (frontend)
- Optional: XAMPP or WAMP for local development on Windows

## ✅ Requirements (local development)
- PHP 7.x / 8.x
- MySQL or MariaDB
- Web server (Apache recommended via XAMPP/WAMP)
- A browser (Chrome, Edge, Firefox)

## 🧩 Setup — Windows (using XAMPP) 🇺🇸

1. Install XAMPP (https://www.apachefriends.org).
2. Copy the project folder into XAMPP's `htdocs` directory. For example:

```powershell
# Copy the project folder (adjust the paths if needed)
# Close XAMPP while copying to avoid file locks
# Example (powershell):
# Copy-Item -Path 'C:\Users\User\Downloads\css299-finalproject-main\finaldemo' -Destination 'C:\xampp\htdocs\finaldemo' -Recurse
```

3. Start Apache and MySQL via the XAMPP Control Panel.
4. Create a new MySQL database (e.g., `hospital_management`) and import the SQL dump:

```powershell
# You can use phpMyAdmin (http://localhost/phpmyadmin) or the mysql CLI.
# Using mysql CLI (adjust user/password as needed):
# mysql -u root -p
# CREATE DATABASE hospital_management; USE hospital_management;
# SOURCE "C:/xampp/htdocs/finaldemo/hospital_management (2).sql";
```

Tip: If you use phpMyAdmin, open it at http://localhost/phpmyadmin → create the database → Import → choose `hospital_management (2).sql`.

5. Update database credentials used by the app (if needed):
- Open `Admin/php/database.php` (and any `database.php` files in the codebase) and set host, username, password, and database name to match your local environment.

## ▶️ Running the app locally

1. With XAMPP running, open your browser and visit:

```
http://localhost/finaldemo/
```

2. Use the provided pages to sign up, login, and test booking flows. Use the admin area to view appointments and feedback.

## 📁 Folder structure (high level)

- `index.html` — public landing page
- `hospital_management (2).sql` — database dump (schema + seed)
- `Admin/` — admin dashboard, appointment actions, and supporting PHP
- `appointment/` — booking flow and slot management
- `Create an Account/` — login/signup and password reset
- `doctor/` — doctor dashboard and availability management
- `patient/` — patient pages and feedback
- `CSS/`, `photo/`, `Admin/css/`, etc. — styling and assets

If you plan to deploy, move sensitive files (e.g., DB credentials) out of the webroot or use environment-based configuration.

## 🔒 Security notes
- The project contains basic authentication flows. Before public deployment:
  - Use HTTPS
  - Secure database credentials and avoid committing secrets
  - Sanitize/validate user inputs to prevent SQL injection and XSS
  - Use prepared statements (PDO or mysqli with prepared statements) for DB queries if not already used

## 🧪 Troubleshooting
- Blank pages or PHP errors: enable display_errors in `php.ini` for debugging (only locally). Check Apache error logs.
- Database connection errors: verify credentials and that MySQL is running.
- Port conflicts: ensure Apache uses port 80/443 or change to free ports.

## 👤 Authors:
   • Mahabub Ahmed Kowsar <br>
     🆔 NSU ID: 2212618642<br>
     🏫 Company: North South University (Computer Science Student)<br>
     📧 Email: <a href="mailto:mahabubkowsar21@gmail.com" target="_blank">mahabubkowsar21@gmail.com</a><br><br>
   • Montasir Mahmud Saykat<br>
     🆔 NSU ID: 2212589042<br>
     🏫 Company: North South University (Computer Science Student)<br>
     📧 Email: <a href="mailto:saykatnsu2025@gmail.com" target="_blank">saykatnsu2025@gmail.com</a><br>



## 🤝 Contributing
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/my-change`.
3. Commit changes: `git commit -m "Add feature"`.
4. Open a pull request with a clear description.

## 📝 License
This project currently does not include an explicit open-source license. Add `LICENSE` if you want to define terms.

## ✉️ Contact
If you need help or want me to add more documentation (setup scripts, env examples, or deployment guidance), reply here and I can extend this README or add a small setup script. 

— MS CARE Team 💙
