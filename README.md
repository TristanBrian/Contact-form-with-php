# 📬 Contact Form with Email & Database Storage

A full-featured PHP contact form application that **sends email notifications** via PHP's mail function and **stores all submissions** in a MySQL database. Includes an admin panel to view, manage, and delete messages — perfect for small business websites, portfolios, or any site needing a reliable way to capture visitor inquiries.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1?logo=mysql&logoColor=white)

## ✨ Features
- User-friendly contact form (HTML/CSS/PHP)
- **Email notifications** sent to site owner using PHP's `mail()` function
- **MySQL database storage** for all submissions
- **Admin panel** to view, manage, and delete messages
- Secure credential handling and SQL injection protection
- Responsive design (adjust styling as needed)

## 📚 Table of Contents
1. [Requirements](#-requirements)
2. [Installation](#-installation)
3. [Configuration](#-configuration)
4. [Running the Application](#-running-the-application)
5. [Admin Panel Access](#-admin-panel-access)
6. [Troubleshooting](#-troubleshooting)
7. [Screenshots (Optional)](#-screenshots)
8. [Contributing & Support](#-contributing--support)

## 📋 Requirements
Before you begin, ensure your system has:
- **XAMPP** (Apache + PHP + MySQL) or any other web server like WAMP, LAMP, or MAMP.
- PHP (version 7.0 or higher recommended).
- MySQL database server.

## 🛠️ Installation

1.  **Download the Project:**
    - Download the zip file from the repository.
    - Alternatively, clone it using Git: `git clone https://github.com/TristanBrian/Contact-form-with-php.git`

2.  **Extract and Copy:**
    - Extract the zip file.
    - Copy the `contactform` folder.
    - Paste it into your web server's root directory:
        - **XAMPP:** `C:\xampp\htdocs\`
        - **WAMP:** `C:\wamp64\www\`
        - **LAMP:** `/var/www/html/`

3.  **Set Up the Database:**
    - Open **phpMyAdmin** (usually `http://localhost/phpmyadmin`).
    - Create a new database named `contactdb`.

4.  **Import the Database Schema:**
    - In phpMyAdmin, select your `contactdb` database.
    - Click the **Import** tab.
    - Choose the file `contactdbfile.sql` (located in the `sql` folder of the downloaded zip package).
    - Click **Go** to import the database structure and sample data.

5.  **Configure Database Connection (if required):**
    - Locate the database configuration file (e.g., `config.php` or `db.php`).
    - Update the connection settings to match your local environment:
        ```php
        $host = 'localhost';
        $username = 'root';      // Your MySQL username
        $password = '';          // Your MySQL password (empty by default for XAMPP)
        $database = 'contactdb'; // The database you created

        ```markdown
# 📬 Contact Form with Email & Database Storage

A full-featured PHP contact form application that **sends email notifications** via PHP's mail function and **stores all submissions** in a MySQL database. Includes an admin panel to view, manage, and delete messages — perfect for small business websites, portfolios, or any site needing a reliable way to capture visitor inquiries.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1?logo=mysql&logoColor=white)

## ✨ Features
- User-friendly contact form (HTML/CSS/PHP)
- **Email notifications** sent to site owner using PHP's `mail()` function
- **MySQL database storage** for all submissions
- **Admin panel** to view, manage, and delete messages
- Secure credential handling and SQL injection protection
- Responsive design (adjust styling as needed)

## 📚 Table of Contents
1. [Requirements](#-requirements)
2. [Installation](#-installation)
3. [Configuration](#-configuration)
4. [Running the Application](#-running-the-application)
5. [Admin Panel Access](#-admin-panel-access)
6. [Troubleshooting](#-troubleshooting)
7. [Screenshots (Optional)](#-screenshots)
8. [Contributing & Support](#-contributing--support)

## 📋 Requirements
Before you begin, ensure your system has:
- **XAMPP** (Apache + PHP + MySQL) or any other web server like WAMP, LAMP, or MAMP.
- PHP (version 7.0 or higher recommended).
- MySQL database server.

## 🛠️ Installation

1.  **Download the Project:**
    - Download the zip file from the repository.
    - Alternatively, clone it using Git: `git clone https://github.com/TristanBrian/Contact-form-with-php.git`

2.  **Extract and Copy:**
    - Extract the zip file.
    - Copy the `contactform` folder.
    - Paste it into your web server's root directory:
        - **XAMPP:** `C:\xampp\htdocs\`
        - **WAMP:** `C:\wamp64\www\`
        - **LAMP:** `/var/www/html/`

3.  **Set Up the Database:**
    - Open **phpMyAdmin** (usually `http://localhost/phpmyadmin`).
    - Create a new database named `contactdb`.

4.  **Import the Database Schema:**
    - In phpMyAdmin, select your `contactdb` database.
    - Click the **Import** tab.
    - Choose the file `contactdbfile.sql` (located in the `sql` folder of the downloaded zip package).
    - Click **Go** to import the database structure and sample data.

5.  **Configure Database Connection (if required):**
    - Locate the database configuration file (e.g., `config.php` or `db.php`).
    - Update the connection settings to match your local environment:
        ```php
        $host = 'localhost';
        $username = 'root';      // Your MySQL username
        $password = '';          // Your MySQL password (empty by default for XAMPP)
        $database = 'contactdb'; // The database you created
        ```

## 🚀 Running the Application

1.  **Start your local server:**
    - **XAMPP:** Start the Apache and MySQL services.
    - **WAMP:** Click the WAMP icon and ensure Apache & MySQL are running.

2.  **Access the Contact Form:**
    - Open your browser and go to:
      `http://localhost/contactform`

3.  **Submit a Test Message:**
    - Fill in the contact form with sample details and submit.
    - You should receive an email notification (check your spam folder if it doesn't appear).
    - The submission will be stored in your `contactdb` database.

## 🔑 Admin Panel Access

The admin panel allows you to view, manage, and delete all submitted messages.

1.  **Access the Admin Panel:**
    - Go to `http://localhost/contactform/admin` in your browser.

2.  **Login Credentials:**
    - **Username:** `admin`
    - **Password:** `Test@123`

> **🔐 Security Reminder:** For production use, change the default password immediately after your first login. You can do this by updating the `admin_users` table in your `contactdb` database.

3.  **What you can do:**
    - View all incoming messages in a table.
    - Read individual message details.
    - Delete spam or outdated submissions.

## 🔍 Troubleshooting

**Emails are not being sent.**
- Ensure your local server (XAMPP/WAMP) has mail configuration enabled.
- Check your spam/junk folder — many local environments won't actually send emails, but errors should be logged.
- For production, consider using **PHPMailer** or **SMTP** instead of the basic `mail()` function for better reliability.

**500 Internal Server Error.**
- Check your PHP error logs.
- Verify file permissions (folders should be 755, files 644).
- Make sure your `php.ini` settings are correct.

**Cannot log in to admin panel.**
- Double-check the admin credentials: `admin` / `Test@123`.
- If you changed the password, ensure the database table `admin_users` (or similar) has the correct hash.
- Try re-importing the `contactdbfile.sql` to reset the admin user.

**Form submits but data not stored in database.**
- Check your database connection settings in `config.php`.
- Verify that the database `contactdb` exists and the `contacts` table is present.

## 🤝 Contributing & Support

- Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
- Found a bug? [Open an issue](https://github.com/TristanBrian/Contact-form-with-php/issues) on GitHub.
- For questions, feel free to reach out via the repository's discussions.

## 📜 License

This project is open-source and available for anyone to use and modify.
```