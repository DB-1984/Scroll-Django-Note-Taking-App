# Scroll

**A minimalist note-taking application built with Django 6 and PostgreSQL, featuring user authentication, Google sign-in and persistent note storage.**

Scroll is a self-directed development project designed to make capturing and returning to ideas feel simple.

The application uses a clean, deliberately restrained interface that keeps the focus on writing and organising notes rather than unnecessary visual distractions.

It was built to explore Python-based web development, Django's server-rendered architecture, relational data persistence, authentication and deployment.

**[Try the Live App](https://scroll-app.onrender.com/)**

*The application is hosted on Render and may take a minute to become available after a period of inactivity. The Supabase database may also be paused, temporarily preventing access.*

---

## Test Login

Try the app using the shared demo account:

- **Username:** Example
- **Password:** PASSWORD_password1234

*This is a shared account. Please avoid entering personal information.*

---

## Video Demonstration

[![Watch the Scroll demonstration](https://img.youtube.com/vi/86NA-kwgsw0/hqdefault.jpg)](https://www.youtube.com/watch?v=86NA-kwgsw0)

*Click the image to watch Scroll in action on YouTube.*

---

## Technology Stack

- **Python / Django 6** — Application logic, routing and server-rendered templates
- **PostgreSQL** — Relational database for persistent application data
- **Supabase** — Hosted PostgreSQL database
- **django-allauth** — Account management and authentication
- **Google OAuth** — Third-party sign-in
- **django-widget-tweaks** — Customisation of form rendering
- **HTML / CSS** — Application interface and presentation
- **Gunicorn** — Production WSGI application server
- **WhiteNoise** — Static asset serving
- **Render** — Application deployment

---

## Key Features

### Note Management

Scroll provides a straightforward interface for creating and managing personal notes.

- Persistent note storage
- User-authenticated access
- Clean, minimal writing interface
- Server-rendered pages using Django templates

The interface deliberately prioritises simplicity, allowing users to concentrate on their content.

### User Authentication

Account management is handled through `django-allauth`, providing:

- User registration and sign-in
- Google OAuth authentication
- Django-integrated account management
- Authenticated access to the application

Using an established authentication library allowed the project to focus on integrating account management with Django's application and template architecture.

### Server-Rendered Interface

Unlike my React and Next.js projects, Scroll uses Django's traditional server-rendered approach.

Django handles routing, application logic and template rendering, while `django-widget-tweaks` provides more control over form presentation without requiring a separate frontend framework.

---

## Technical Approach

### Django Application Architecture

Scroll explores Django's integrated approach to web development.

The framework provides routing, database models, views, forms and template rendering within a single Python application.

This offered an opportunity to work with a different architectural approach from the component-based JavaScript applications in my portfolio.

### Relational Data Persistence

The production application uses PostgreSQL hosted on Supabase.

Django's ORM provides an interface between the application and its database, allowing note data to be managed through Python models and queries.

For local development, the application falls back to SQLite when a PostgreSQL connection is not configured.

### Authentication Integration

The project uses `django-allauth` to handle account management and Google OAuth.

This provided practical experience integrating third-party authentication into Django's existing user and session management systems.

### Deployment and Configuration

Scroll is deployed on Render using:

- **Gunicorn** to serve the Django application
- **WhiteNoise** to serve static assets
- **Supabase PostgreSQL** for production data storage
- **Environment variables** for deployment-specific configuration

The database connection is configured through `DATABASE_URL`, allowing the same application to use PostgreSQL in production and SQLite during local development.

---

## Local Development

### Requirements

- Python and pip
- A local Django development environment
- SQLite or a PostgreSQL database
- Appropriate environment variables for any configured external services

### Installation

Clone the repository and navigate to the project directory.

Create a Python virtual environment:

```bash
python -m venv .venv
```

Activate the environment:

**macOS / Linux**

```bash
source .venv/bin/activate
```

**Windows**

```bash
.venv\Scripts\activate
```

Install the project dependencies:

```bash
pip install -r requirements.txt
```

Configure any required environment variables.

If `DATABASE_URL` is not set, the application is configured to use SQLite for local development.

Apply database migrations:

```bash
python manage.py migrate
```

Start the development server:

```bash
python manage.py runserver
```

Open http://127.0.0.1:8000 in your browser.

*Google OAuth and other external integrations may require additional credentials and local configuration.*

---

## Project Context

Scroll is a personal portfolio project developed to broaden my experience beyond JavaScript, PHP and WordPress.

Working with Django provided an opportunity to explore Python-based application development, relational persistence, authentication and server-rendered web interfaces.

The project demonstrates my ability to work across different backend ecosystems while maintaining the same emphasis on practical functionality, usability and straightforward application design.

---

## Links

- **Live Application:** https://scroll-app.onrender.com/
- **Video Demonstration:** https://www.youtube.com/watch?v=86NA-kwgsw0
- **Developer Portfolio:** https://davidbrandondev.com/
- **GitHub Profile:** https://github.com/DB-1984
