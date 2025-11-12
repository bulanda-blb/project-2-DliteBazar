# DLiteBazar

Small Django 5 marketplace where creators upload and sell photos while customers browse, buy, and download licensed images.

## Structure

- `dlitebazar/` – project settings and URLs
- `admin_panel/` – admin dashboards, moderation, finance tooling
- `profile_dashboard/` – user dashboards, uploads, transactions
- `user_registration/`, `user_login/` – auth & onboarding flows
- `static/`, `templates/`, `media/` – assets and uploaded files

## Prerequisites

- Python 3.10+ with `venv`
- MySQL 8 (or compatible) database
- SMTP account with app password (e.g., Gmail)

## Steps to Run

1. `python -m venv myenv && myenv\Scripts\activate`
2. `python -m pip install --upgrade pip`
3. `pip install -r requirements.txt`
4. Provision the database: `CREATE DATABASE dlitebazar CHARACTER SET utf8mb4;`
5. Set secrets (PowerShell example):  
   `setx DJANGO_SECRET_KEY "<your-django-secret>"`  
   `setx EMAIL_HOST_USER "<your-email-address>"`  
   `setx EMAIL_HOST_PASSWORD "<your-email-app-password>"`
6. Restart the shell (loads env vars) and run `python manage.py migrate`
7. `python manage.py createsuperuser` (optional)
8. `python manage.py runserver`

Update the environment values with your own credentials before running the server.
