# 🏨 Hotel Management System

A simple Hotel Management System built with **Django** to demonstrate the fundamentals of web application development. The system provides basic hotel management functionality using Django's built-in features and an SQLite database.

---

## 📌 Features

- User authentication
- Hotel room management
- Customer management
- Booking management
- Django Admin dashboard
- SQLite database integration

---

## 🛠️ Technologies Used

- Python
- Django
- SQLite3
- PowerShell (for running the project)

---

## 📁 Project Structure

```
HotelManagementSystem/
│
├── core/              # Main Django application
├── HotelManagement/   # Project configuration
│   ├── settings.py    # Project settings
│   ├── urls.py        # URL routing
│   ├── wsgi.py
│   └── asgi.py
│         
├── db.sqlite3         # SQLite database
├── manage.py          # Django management utility
└── requirements.txt   # Project dependencies (optional)
```

---

## ⚙️ Important Files

| File | Purpose |
|------|---------|
| **manage.py** | Runs Django commands such as starting the server and migrations. |
| **settings.py** | Stores project configurations including installed apps, database settings and templates. |
| **db.sqlite3** | Default SQLite database containing project data. |
| **core/** | Main application containing models, views, URLs and business logic. |

---

## ▶️ Running the Project

Open **PowerShell** inside the project folder.

### Activate the virtual environment

```powershell
.\venv\Scripts\Activate
```

### Apply migrations

```powershell
python manage.py migrate
```

### Run the development server

```powershell
python manage.py runserver
```

Visit:

```
http://127.0.0.1:8000/
```

---

## 🚀 Future Improvements

- Online room reservations
- Payment integration
- Email booking confirmations
- Search and filter rooms
- Customer booking history
- Responsive mobile-friendly interface
- Reporting and analytics

---

## 👨‍💻 Author

**Daniela Wakhu**

Designed and developed as a Django learning project to demonstrate basic hotel management concepts and web development skills.
