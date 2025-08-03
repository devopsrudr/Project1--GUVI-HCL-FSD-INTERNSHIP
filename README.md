# 🚀 InternPro - Modern Full Stack (React.js+ Python) Internship Discovery Platform

> A beautiful, Apple-inspired React frontend for connecting students with their dream internships

https://www.loom.com/share/4ad1af3355e24ecca8aecb4238f2d5fc?sid=c73436c3-a583-4e13-a611-d4c5c2a5fd5d

## 📁 Project Structure

```
src/
├── components/           # Reusable UI components
│   ├── common/          # Shared components (Header, Footer, Loading)
│   ├── forms/           # Form components
│   └── ui/              # Basic UI elements
├── pages/               # Page components
│   ├── auth/            # Authentication pages
│   ├── internships/     # Internship-related pages
│   ├── companies/       # Company pages
│   └── Home.tsx         # Landing page with animations
├── hooks/               # Custom React hooks
├── services/            # API service functions
├── contexts/            # React Context providers
├── data/                # Mock data and constants
├── utils/               # Utility functions
├── types/               # TypeScript type definitions
└── styles/              # Global styles
```

## 🎨 Key Components

### 🏠 **Homepage (`src/pages/Home.tsx`)**
The crown jewel of the application featuring:
- **Full-screen hero section** with animated gradient backgrounds
- **Interactive mouse parallax** effects
- **Animated statistics** with spring physics
- **Featured internships** with hover animations
- **How it works** section with staggered reveals
- **Call-to-action** sections with premium button animations

### 💼 **Internship Discovery**
- **Advanced filtering system** with multiple criteria
- **Search functionality** with real-time results
- **Card-based layout** with hover effects
- **Pagination** for large datasets
- **Save/bookmark** functionality

### 🏢 **Company Directory**
- **Company profiles** with detailed information
- **Industry and size filtering**
- **Location-based search**
- **Statistics dashboard**
- **Interactive company cards**

### 🔐 **Authentication**
- **Modern login/register forms** with validation
- **Error handling** with user-friendly messages
- **Password strength indicators**
- **Social login integration** ready

## 🎭 Animation Highlights

### **Hero Section Animations**

### **Button Animations**

### **Staggered List Animations**



# Internship Portal Backend

A Django REST API backend for an internship portal with MongoDB database integration.

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
