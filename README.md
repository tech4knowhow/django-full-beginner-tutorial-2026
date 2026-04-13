![Python](https://img.shields.io/badge/Python-3.x-blue)
![Django](https://img.shields.io/badge/Django-Framework-green)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Project-Beginner%20Friendly-brightgreen)

# django-full-beginner-tutorial-2026
Full Django tutorial for beginners – Learn Python Django step by step, build an Employee Management System, and connect to SQL Server (2026 Guide)

This repository contains a complete **Django beginner guide project** that walks you through installing Python, setting up Django, and building a fully functional web application with an **Employee Management System**.

## 📌 Overview

This project is designed for beginners who want to learn Django step by step, including:

- Python installation & setup
- Django installation
- Creating projects and apps
- Understanding Django structure
- Admin panel customization
- User authentication & permissions
- Employee management system (HR module)
- SQL Server integration

## 🧠 What is Django?

Django is a **high-level Python web framework** that enables rapid development, security, and scalability. It is free and open-source.


## ⚙️ Features

✔ User Authentication (Login, Admin)  
✔ Group & Permission Management  
✔ Employee Registration System  
✔ Django Admin Customization  
✔ SQLite (default) + SQL Server support  
✔ Clean project structure  

## 🏗️ Project Structure

demoapp/
│── demoapp/
│   ├── **init**.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│
│── appone/
│   ├── models.py
│   ├── admin.py
│
│── db.sqlite3
│── manage.py


## 🛠️ Installation Guide

### 1️⃣ Install Python
Download and install Python (64-bit recommended)

✔ Make sure to:
- Add Python to PATH
- Run installer as administrator

### 2️⃣ Create Virtual Environment (Optional but Recommended)

python -m venv venv
venv\Scripts\activate

### 3️⃣ Install Django

pip install django

### 4️⃣ Create Project

django-admin startproject demoapp
cd demoapp

### 5️⃣ Run Server

python manage.py runserver

Open in browser:
http://127.0.0.1:8000/

## 📦 Create App

python manage.py startapp appone

Add to `settings.py`:
INSTALLED_APPS = [
    'appone',
]

## 🧾 Models (Employee System)

class Employee(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    employee_id = models.CharField(max_length=20, unique=True)
    department = models.CharField(max_length=100)
    designation = models.CharField(max_length=100)
    phone = models.CharField(max_length=15)
    address = models.TextField()
    date_joined = models.DateField()
    is_active = models.BooleanField(default=True)

## 🔐 Admin Configuration

* User Management
* Group & Permissions
* Employee Registration

## 🗄️ Database Setup
### Default (SQLite)

Works out of the box.
### SQL Server Configuration

DATABASES = {
    'default': {
        'ENGINE': 'mssql',
        'NAME': 'demoappdb',
        'HOST': 'YOUR_SERVER_NAME',
        'PORT': '1433',
        'USER': 'sa',
        'PASSWORD': '',
        'OPTIONS': {
            'driver': 'ODBC Driver 18 for SQL Server',
            'Encrypt': 'no',
            'extra_params': 'TrustServerCertificate=yes;',
            'host_is_server': True,
        },
    }
}

## 🔄 Run Migrations
python manage.py makemigrations
python manage.py migrate

## 👤 Create Admin User
python manage.py createsuperuser

## ▶️ Run Project
python manage.py runserver

Access admin panel:
http://127.0.0.1:8000/admin/

## 🎨 Customize Admin Panel

admin.site.site_header = "Tech4knowhow | DEMOAPP"
admin.site.site_title = "Tech4knowhow Admin Portal"
admin.site.index_title = "Welcome to Admin Area"

## 🎥 YouTube Tutorial
👉 Watch full tutorial here: *(https://www.youtube.com/@tech4knowhow)*

## 📈 Future Improvements

* REST API integration (Django REST Framework)
* Frontend (React / Vue)
* Deployment (Docker, Cloud)
* Advanced authentication (JWT)

## 🤝 Contributing
Contributions are welcome! Feel free to fork and submit pull requests.

## 📜 License
This project is open-source and available under the MIT License.

## ⭐ Support

If you like this project:
* ⭐ Star the repository
* 🔔 Subscribe on YouTube
* 👍 Share with others


![Django Tutorial Thumbnail](django-full-tutorial-beginners-2026-python-installation-first-project.jpg

