# Tour Management System

A full-stack **Tour Management System (TMS)** developed as an academic **DBMS project**. The system provides a centralized web interface for managing tour packages, customers, bookings, payments, reviews, tour guides, locations, hotels, and analytics.

The application follows a practical client–server architecture with a **FastAPI REST API**, **Vanilla JavaScript + Bootstrap frontend**, and **MySQL/MariaDB database**.

## ✨ Key Features

- 📊 Interactive dashboard with operational statistics
- 🧑‍🤝‍🧑 Customer management with full CRUD operations
- 🗺️ Tour package management
- 🧾 Booking and traveler-detail management
- 💳 Payment management with multiple payment methods
- ⭐ Review and rating management
- 🧑‍💼 Tour guide management with multilingual information
- 📍 Location management
- 🏨 Hotel management
- 📈 Analytics dashboard with Chart.js visualizations
- 🔌 RESTful API with FastAPI
- 📚 Interactive Swagger/OpenAPI documentation
- 🗄️ MySQL/MariaDB relational database
- 📱 Responsive SPA-style dashboard interface

## 🏗️ System Architecture

```text
┌─────────────────────────────┐
│     Web Frontend            │
│ HTML + CSS + Bootstrap + JS │
│        + Chart.js           │
└──────────────┬──────────────┘
               │ HTTP / JSON
               ▼
┌─────────────────────────────┐
│       FastAPI Backend       │
│ REST API + Pydantic Models  │
│        + API Routers        │
└──────────────┬──────────────┘
               │ SQL
               ▼
┌─────────────────────────────┐
│       MySQL / MariaDB       │
│   Relational Database       │
└─────────────────────────────┘
```

## 🧩 Main Modules

| Module | Functionality |
|---|---|
| Dashboard | Operational statistics and recent activity |
| Customers | Create, read, update and delete customer records |
| Tour Packages | Manage packages and related resources |
| Bookings | Manage bookings and traveler details |
| Payments | Track booking payments and payment methods |
| Reviews | Manage ratings and customer feedback |
| Tour Guides | Manage guides and supported languages |
| Locations | Manage destinations and seasonal information |
| Hotels | Manage hotels, ratings and locations |
| Analytics | SQL-driven performance and business insights |

## 🗄️ Database

The project uses a relational **MySQL/MariaDB** database and includes the complete database dump in:

```text
database/tourmanagementsystem.sql
```

The database covers entities and relationships for customers, bookings, tour packages, payments, reviews, guides, locations, hotels, and traveler details.

The SQL dump contains **sample/demo data** for academic testing and demonstration.

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | HTML5, CSS3, Bootstrap 5.3, Vanilla JavaScript |
| Visualization | Chart.js |
| Backend | Python 3.10+, FastAPI, Uvicorn |
| Validation | Pydantic |
| Database | MySQL / MariaDB |
| Database Driver | mysql-connector-python |
| Configuration | python-dotenv |
| API Style | RESTful JSON API |
| Documentation | Swagger / OpenAPI |

## 📁 Project Structure

```text
Tour-Management-System/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── requirements.txt
│   ├── .env.example
│   └── routers/
│       ├── __init__.py
│       ├── analytics.py
│       ├── bookings.py
│       ├── customers.py
│       ├── hotels.py
│       ├── locations.py
│       ├── payments.py
│       ├── reviews.py
│       ├── tourguides.py
│       └── tourpackages.py
├── database/
│   └── tourmanagementsystem.sql
├── frontend/
│   ├── index.html
│   └── assets/
│       ├── css/
│       │   └── style.css
│       └── js/
│           ├── utils.js
│           └── pages/
│               ├── analytics.js
│               ├── bookings.js
│               ├── customers.js
│               ├── dashboard.js
│               ├── hotels.js
│               ├── locations.js
│               ├── payments.js
│               ├── reviews.js
│               ├── tourguides.js
│               └── tourpackages.js
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Python **3.10+**
- MySQL or MariaDB
- XAMPP is recommended for local MySQL/phpMyAdmin setup

### 1. Clone the repository

```bash
git clone https://github.com/Fazle240102/Tour-Management-System.git
cd Tour-Management-System
```

### 2. Set up the database

Start MySQL through XAMPP, then open phpMyAdmin and create a database named:

```text
tourmanagementsystem
```

Import:

```text
database/tourmanagementsystem.sql
```

### 3. Configure the backend

```bash
cd backend
```

Create a local environment file from the provided template:

```bash
# Windows
copy .env.example .env

# macOS / Linux
cp .env.example .env
```

Update the database credentials in `.env` if necessary.

### 4. Create a virtual environment

```bash
python -m venv venv
```

Windows:

```bash
venv\Scripts\activate
```

macOS / Linux:

```bash
source venv/bin/activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Start the FastAPI server

```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

Backend:

```text
http://localhost:8000
```

Interactive API documentation:

```text
http://localhost:8000/docs
```

### 7. Run the frontend

From the project root:

```bash
cd frontend
python -m http.server 5500
```

Then open:

```text
http://localhost:5500
```

The frontend communicates with the FastAPI backend through the configured API base URL.

## 🔌 API Resources

The backend exposes REST endpoints for:

- `/api/customers`
- `/api/tourpackages`
- `/api/bookings`
- `/api/payments`
- `/api/reviews`
- `/api/tourguides`
- `/api/locations`
- `/api/hotels`
- `/api/analytics`

Each resource supports the relevant CRUD or analytics operations implemented by its router.

## 📊 Analytics

The analytics module provides SQL-driven insights including:

- Dashboard statistics
- Top-performing tours
- Revenue by tour
- Tour guide performance
- Location popularity
- Monthly booking trends

Results are visualized through **Chart.js** in the frontend dashboard.

## 🔐 Configuration & Security

- Environment-specific database credentials are stored through `.env`.
- `.env.example` is included as a configuration template.
- Actual `.env` files should remain local and should never be committed.
- The included SQL data is intended for academic/demo purposes.

## 🎓 Academic Context

- **Project:** Tour Management System (TMS)
- **Project Type:** Academic DBMS / Full-Stack Web Application
- **Institution:** Daffodil International University
- **Team:** Team Adrenaline

## 👥 Team

Developed collaboratively by **Team Adrenaline** at **Daffodil International University**.

## 📌 Project Status

Completed academic project demonstrating relational database design, REST API development, CRUD-based web application architecture, and analytics-driven dashboard functionality.
