#AI Train Booking System (Django)

This project is a Django-based Train Booking application that supports both **AI-based seat selection** and **Manual seat selection**.  
It exposes train data as JSON APIs and displays them using HTML, JavaScript, and Tailwind CSS.

---

##Project Structure

AI_TRAINBOOKING/
│
├── Ai_TrainBooking/ # Main Django project
│ ├── init.py
│ ├── asgi.py
│ ├── settings.py
│ ├── urls.py
│ ├── wsgi.py
│
├── Train/ # Train app
│ ├── migrations/
│ ├── templates/
│ │ ├── index.html # Home / Search page
│ │ ├── Ai.html # AI-based seat selection UI
│ │ └── manual.html # Manual seat selection UI
│ │
│ ├── init.py
│ ├── admin.py # Admin registrations
│ ├── apps.py
│ ├── models.py # Train, TrainClass, Seat models
│ ├── serializer.py # (Optional) DRF serializers
│ ├── tests.py
│ ├── urls.py # App-level URLs
│ └── views.py # Views + JSON APIs
│
├── db.sqlite3 # SQLite database
├── manage.py # Django management file
└── README.md # Project documentation




## Features

- Train listing with routes and timings
- AI-based seat selection (UI flow)
- Manual seat selection option
- Train data served as JSON API
- Frontend uses HTML + JS `fetch()`
- Styled using Tailwind CSS
- Admin panel to manage train data

---

## Application Flow

- **Home Page** → `index.html`
- **AI Mode** → `/ai-search/` → `Ai.html`
- **Manual Mode** → `/manual-search/` → `manual.html`
- **Train JSON API** → `/trains/` or `/trains-static/`



##How to Run the Project

### 1Create virtual environment (optional)


python -m venv env
env\Scripts\activate

Install dependencies
pip install django


(DRF optional if used)

pip install djangorestframework

3️Run migrations
python manage.py makemigrations
python manage.py migrate

4️Create superuser (Admin)
python manage.py createsuperuser

5️ Start the server
python manage.py runserver


Open browser:

http://127.0.0.1:8000/

Admin Panel
http://127.0.0.1:8000/admin/


Admin can manage:

Trains

Train Classes

Seats

JSON API Example
GET /trains/


Returns:

[
  {
    "id": "T001",
    "name": "Rajdhani Express",
    "from": "Chennai",
    "to": "Mumbai",
    "classes": [],
    "seats": []
  }
]

Technologies Used

Python

Django

SQLite

HTML, CSS

Tailwind CSS

JavaScript (Fetch API)

Viva Explanation (Short)

“This project demonstrates how Django can be used to build a backend API and integrate it with frontend pages for AI-based and manual train seat booking.”

 \Future Enhancements

AI recommendation logic

Seat booking POST API

User authentication

Payment integration

React Frontend


---
