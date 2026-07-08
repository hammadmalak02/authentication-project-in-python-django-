# Django Learning Projects

This repository contains two Django projects for learning Django fundamentals and advanced concepts.

## Projects Overview

### 1. Authentication Project
A Django application demonstrating user authentication and authorization with login/logout functionality.

**Features:**
- User authentication system
- Login page with username and password
- Protected pages (redirects to login if not authenticated)
- Logout functionality
- Session management

**Credentials for Testing:**
```
Superuser: (make one for yourself)

Test User: (make one for yourself)

### 2. Hello Project
A multi-page Django application demonstrating the MVT (Model View Template) architecture.

**Features:**
- Home page
- About page
- Services page
- Contact page with form submission
- Contact form data storage in database
- Dynamic routing and URL handling

**Credentials for Testing:**
```
Superuser: (make one for yourself)

## Project Structure

```
authentication-project-in-python-(django)/
├── authenticationproject/          # Authentication Django Project
│   ├── authenticationproject/       # Project configuration
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
│   ├── home/                        # Main application
│   │   ├── views.py                 # Views (Login, Logout, Index)
│   │   ├── urls.py
│   │   ├── models.py
│   │   ├── migrations/
│   │   └── templates/
│   │       ├── index.html
│   │       └── login.html
│   ├── static/
│   ├── manage.py
│   └── db.sqlite3
│
└── Hello/                           # General Purpose Django Project
    ├── Hello/                       # Project configuration
    │   ├── settings.py
    │   ├── urls.py
    │   ├── asgi.py
    │   └── wsgi.py
    ├── home/                        # Main application
    │   ├── views.py                 # Views (Index, About, Services, Contact)
    │   ├── models.py                # Contact model
    │   ├── urls.py
    │   ├── migrations/
    │   └── templates/
    │       ├── base.html
    │       ├── index.html
    │       ├── about.html
    │       ├── services.html
    │       └── contact.html
    ├── static/
    ├── manage.py
    └── db.sqlite3
```

## Installation & Setup

### Prerequisites
- Python 3.8+
- Django 6.0.6+
- pip

### Steps

1. **Clone the repository:**
```bash
git clone <repository-url>
cd authentication-project-in-python-(django)
```

2. **Install Django (if not installed):**
```bash
pip install django
```

3. **Run Authentication Project:**
```bash
cd authenticationproject
python manage.py runserver
```
Visit: `http://127.0.0.1:8000`

4. **Run Hello Project:**
```bash
cd Hello
python manage.py runserver
```
Visit: `http://127.0.0.1:8000`

## Key Concepts Demonstrated

### Authentication Project
- Django User Model
- Authentication middleware
- Session management
- Login/Logout views
- Conditional rendering based on user authentication

### Hello Project
- **MVT Architecture**: Model → View → Template pattern
- **URL Routing**: Dynamic URL patterns
- **Form Handling**: POST requests for contact form
- **Database Models**: Contact model with CharField and TextField
- **Templates**: HTML templates with Django template syntax

## Models

### Hello Project - Contact Model
```python
class Contact(models.Model):
    name = CharField(max_length=122)
    email = CharField(max_length=122)
    phone = CharField(max_length=122)
    desc = TextField()
    date = DateField()
```

## Usage Examples

### Authentication Project
- Access `/` → Redirects to `/login` if not authenticated
- Access `/login` → Login form
- Access `/logout` → Logs out user

### Hello Project
- `/` → Home page
- `/about` → About page
- `/services` → Services page
- `/contact` → Contact form with submission

## Views Overview

### Authentication Project
- `index()` - Protected home page
- `loginUser()` - Handle user authentication
- `logoutUser()` - Handle user logout

### Hello Project
- `index()` - Home page
- `about()` - About page
- `services()` - Services page
- `contact()` - Contact form with database storage

## Django Admin Access

Both projects use Django's built-in admin interface:
```
Admin URL: http://127.0.0.1:8000/admin
```
Use the superuser credentials.

## Technologies Used

- **Django 6.0.6** - Web framework
- **SQLite** - Database
- **Python 3** - Programming language
- **HTML/CSS** - Frontend templates

## Future Improvements

- Add form validation and error handling
- Implement email notifications for contact form
- Add user registration functionality
- Implement password reset feature
- Add search functionality
- Implement pagination
- Add user profiles
- Deploy to production

## Notes

- Both projects use SQLite database (db.sqlite3)
- DEBUG mode is enabled - disable for production
- ALLOWED_HOSTS should be updated for production
- SECRET_KEY should be kept secure for production

## License
This is an educational project.

## Author
Created as part of Django learning from Code With Harry tutorials.
