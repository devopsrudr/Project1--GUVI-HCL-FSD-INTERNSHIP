# Internship Portal API Documentation

## Base URL
```
http://127.0.0.1:8000/api/
```

## Authentication
Most endpoints require authentication using Token Authentication.
Include the token in the Authorization header:
```
Authorization: Token your_token_here
```

## API Endpoints

### Authentication Endpoints

#### Register User
- **POST** `/api/auth/register/`
- **Body:**
```json
{
    "username": "john_doe",
    "email": "john@example.com",
    "password": "securepassword123",
    "password_confirm": "securepassword123",
    "first_name": "John",
    "last_name": "Doe",
    "user_type": "student",
    "phone": "+1234567890"
}
```

#### Login
- **POST** `/api/auth/login/`
- **Body:**
```json
{
    "username": "john_doe",
    "password": "securepassword123"
}
```

#### Logout
- **POST** `/api/auth/logout/`
- **Headers:** `Authorization: Token your_token`

#### User Profile
- **GET/PUT** `/api/auth/profile/`
- **Headers:** `Authorization: Token your_token`

#### Student Profile
- **GET/PUT** `/api/auth/student-profile/`
- **Headers:** `Authorization: Token your_token`

#### List Students
- **GET** `/api/auth/students/`
- **Headers:** `Authorization: Token your_token` (Company/Admin only)

### Company Endpoints

#### List Companies
- **GET** `/api/companies/`
- **Query Parameters:** `industry`, `company_size`, `city`, `country`, `search`

#### Company Detail
- **GET** `/api/companies/{id}/`

#### Company Profile (Own)
- **GET/PUT** `/api/companies/profile/`
- **Headers:** `Authorization: Token your_token` (Company user only)

#### Create Company Profile
- **POST** `/api/companies/create/`
- **Headers:** `Authorization: Token your_token` (Company user only)

### Internship Endpoints

#### List Internships
- **GET** `/api/internships/`
- **Query Parameters:** `employment_type`, `experience_level`, `company__industry`, `location`, `is_remote`, `is_featured`, `search`

#### Internship Detail
- **GET** `/api/internships/{id}/`

#### Featured Internships
- **GET** `/api/internships/featured/`

#### Internship Statistics
- **GET** `/api/internships/stats/`

#### Company's Internships
- **GET/POST** `/api/internships/my-internships/`
- **Headers:** `Authorization: Token your_token` (Company user only)

#### Company's Internship Detail
- **GET/PUT/DELETE** `/api/internships/my-internships/{id}/`
- **Headers:** `Authorization: Token your_token` (Company user only)

### Application Endpoints

#### Student's Applications
- **GET/POST** `/api/applications/my-applications/`
- **Headers:** `Authorization: Token your_token` (Student only)

#### Student's Application Detail
- **GET** `/api/applications/my-applications/{id}/`
- **Headers:** `Authorization: Token your_token` (Student only)

#### Company's Received Applications
- **GET** `/api/applications/received/`
- **Headers:** `Authorization: Token your_token` (Company only)

#### Company's Application Detail
- **GET/PUT** `/api/applications/received/{id}/`
- **Headers:** `Authorization: Token your_token` (Company only)

#### Interviews
- **GET/POST** `/api/applications/interviews/`
- **Headers:** `Authorization: Token your_token`

#### Interview Detail
- **GET/PUT/DELETE** `/api/applications/interviews/{id}/`
- **Headers:** `Authorization: Token your_token`

#### Application Statistics
- **GET** `/api/applications/stats/`
- **Headers:** `Authorization: Token your_token`

## Sample Data

The database has been populated with sample data:

### Sample Users
- **Students:** john_doe, jane_smith, mike_johnson (password: password123)
- **Companies:** tech_corp, innovate_inc, finance_pro (password: password123)
- **Admin:** rudra (your created password)

### Sample Companies
- TechCorp Solutions (Technology)
- Innovate Inc (Technology) 
- FinancePro LLC (Finance)

### Sample Internships
Each company has 2 internships with various roles like:
- Software Development Intern
- Data Science Intern
- Marketing Intern
- Product Management Intern

### Sample Applications
Each student has applied to 2-4 internships with different statuses.

## Admin Panel

Access the Django admin panel at:
```
http://127.0.0.1:8000/admin/
```

Use the superuser credentials you created to access all models and manage the system.

## Testing the API

You can test the API using tools like:
- Postman
- curl
- Django REST Framework browsable API (when logged in)

### Example: Login and Get Token
```bash
curl -X POST http://127.0.0.1:8000/api/auth/login/ \
  -H "Content-Type: application/json" \
  -d '{"username": "john_doe", "password": "password123"}'
```

### Example: Get Internships
```bash
curl -X GET http://127.0.0.1:8000/api/internships/ \
  -H "Content-Type: application/json"
```

### Example: Apply for Internship (as student)
```bash
curl -X POST http://127.0.0.1:8000/api/applications/my-applications/ \
  -H "Content-Type: application/json" \
  -H "Authorization: Token your_token_here" \
  -d '{"internship": 1, "cover_letter": "I am very interested in this position..."}'
```
