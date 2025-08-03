# 🚀 InternPro - Modern Full Stack (React.js+ Python Django) Internship Discovery Platform

> A beautiful, Apple-inspired React frontend for connecting students with their dream internships


### Internship Portal Backend

A Django REST API backend for an internship portal with MongoDB database integration.

https://www.loom.com/share/e9caccb4ef32412e90fd13e5fca0e232?sid=2936f19f-a2fd-4fab-9842-fd0787835286
## Features

- User authentication (Students, Companies, Admins)
- Company profiles and management
- Internship posting and application system
- Student profiles and resume management
- Admin panel for management
- MongoDB database integration
- REST API endpoints

## Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Set up environment variables in `.env` file

3. Run migrations:
```bash
python manage.py migrate
```

4. Create superuser:
```bash
python manage.py createsuperuser
```

5. Run the server:
```bash
python manage.py runserver
```

## API Endpoints

- `/api/auth/` - Authentication endpoints
- `/api/users/` - User management
- `/api/companies/` - Company profiles
- `/api/internships/` - Internship listings
- `/api/applications/` - Application management
- `/admin/` - Django admin panel

## Models

- User (Students, Companies, Admins)
- Company Profile
- Student Profile
- Internship
- Application

**Made with ❤️ by Rudra Banerjee**



