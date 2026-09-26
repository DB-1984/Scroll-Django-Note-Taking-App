# Scroll — Zen Note-taking App
**[Try the live app](https://scroll-app.onrender.com/)**
(the Render service may take a minute to wake up).

Scroll is a note-taking app designed to make capturing and returning to ideas feel simple. Its interface is clean and minimal, keeping the focus on the notes themselves.

I built it with **Django 6** and a Supabase-hosted PostgreSQL database. Django handles the application logic and server-rendered pages, while `django-allauth` provides account management and Google sign-in. I used `django-widget-tweaks` to refine how forms appear in the templates.

## Deployment

Scroll runs on Render, with Gunicorn serving the application and WhiteNoise serving its static assets. It connects to PostgreSQL through a `DATABASE_URL` environment variable and falls back to SQLite for local development when that variable is absent.

## Built with

* Django 6
* PostgreSQL hosted on Supabase
* `django-allauth` and Google OAuth
* `django-widget-tweaks`
* Gunicorn and WhiteNoise
* Render
