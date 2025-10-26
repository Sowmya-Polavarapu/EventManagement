# Event Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-%3E=2.0-green.svg)](https://flask.palletsprojects.com/)
[![MySQL](https://img.shields.io/badge/Database-MySQL-blue.svg)](https://www.mysql.com/)
[![Bootstrap](https://img.shields.io/badge/UI-Bootstrap-purple.svg)](https://getbootstrap.com/)
[![Code Quality](https://img.shields.io/badge/Code%20Quality-Polished-brightgreen.svg)]()
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)](CONTRIBUTING.md)

> A full-stack web application for creating, managing, and attending events with integrated user roles, ticket booking, and real-time event tracking.

---

## 🌟 Project Overview

The Event Management System is a comprehensive platform for both event organizers and attendees. Organizers can create events, manage bookings, and track statistics, while attendees can browse events, book tickets, and manage their registrations. The system features:
- Fully role-based user authentication (organizer, attendee, optional admin)
- Event creation, editing, and deletion
- Real-time ticket booking and availability tracking
- Dashboards and analytics for event performance
- Secure payment and registration flows
- Modern and responsive user interface

### Architecture & Key Components

- **Frontend**: HTML, CSS, JavaScript, Bootstrap for fast, responsive UI
- **Backend**: Python (Flask), with Flask-Login and Flask-WTF for security and forms
- **Database**: MySQL, managed via SQLAlchemy ORM
- **Authentication**: Role-based access, password hashing, session management
- **Dashboards**: Chart.js for real-time stats and analytics
- **Modular Structure**:
  ```
  EventManagementSystem/
  ├── app/
  │   ├── models.py            # ORM models for users, events, tickets, bookings
  │   ├── routes/
  │   │   ├── auth_routes.py
  │   │   ├── attendee_routes.py
  │   │   ├── organizer_routes.py
  │   │   ├── event_routes.py
  │   ├── templates/
  │   │   ├── base.html
  │   │   ├── auth/
  │   │   ├── attendee/
  │   │   ├── organizer/
  │   │   ├── admin/ (optional)
  │   ├── static/
  │       ├── css/
  │       ├── js/
  ├── migrations/
  ├── tests/
  ├── run.py
  ├── requirements.txt
  ├── README.md
  └── LICENSE
  ```

### Major Functions & Flow

**Authentication System**
- Secure registration and login for organizers/attendees
- Password hashing and session-based login with Flask-Login

**Role-Based Access**
- Decorators restrict dashboard/event management to organizers
- Attendees can register and manage their own bookings

**Event Management**
- CRUD operations for events (title, details, date/time, location, capacity, price)
- Image upload for event banners

**Ticket Booking**
- Attendees book tickets (capacity limits enforced)
- Dashboard to view/manage tickets; cancellation supported

**Dashboards**
- Organizers: track event stats, registrations, sales
- Attendees: view booked events, tickets

**Dashboard and Analytics**
- Visualize event statistics
- Track attendance and registrations
- Monitor popular event categories

**Event Listing & Filtering**
- Public event list, search, and category/date/location filters

**Optional Features**
- Downloadable tickets (PDF)
- QR code for event check-in
- Sales analytics

---

## 🚀 Installation

### Prerequisites
- Python 3.11 or higher
- MySQL (recommended: XAMPP or a standalone MySQL server)
- Modern web browser (Chrome, Firefox, Edge, etc.)

### Quick Setup

> **For detailed setup, see the [XAMPP Setup Guide for Beginners](XAMPP_SETUP_GUIDE.md).**

1. **Start MySQL database service** (via XAMPP or your preferred method)
2. **Create a database** named `event_management`
3. **Install Python dependencies**:
    ```bash
    pip install flask flask-login flask-sqlalchemy flask-wtf email-validator gunicorn mysql-connector-python werkzeug
    ```
4. **Configure the database connection** in `app.py` or `main.py`
5. **Run the application**:
    ```bash
    python main.py
    ```
6. **Open your browser** and navigate to [http://localhost:5000](http://localhost:5000)

---

## 💡 Usage Example

### Registration & Login

1. Click 'Register' on the homepage
2. Choose your user type (Organizer or Attendee)
3. Fill in the required details
4. Login using your registered email and password

### Creating Events (Organizers Only)

1. Log in as an organizer
2. Navigate to 'Create Event'
3. Enter event details (title, description, date/time, location, etc.)
4. Set event capacity and pricing
5. Submit to create your event

### Managing Events

- View all your events under 'My Events'
- Edit, delete, and track registration statistics

### Browsing & Booking (Attendees)

1. Click 'Explore Events' to view all events
2. Apply filters or search for specific events
3. Click on an event to see details
4. Register by clicking 'Get Tickets'

### Managing Tickets

- View registered events under 'My Tickets'
- See event details, ticket status
- Cancel tickets for events you cannot attend

---

## Quick Start Guide

For first-time users, we've provided a comprehensive guide to set up the application using XAMPP. Please see the [XAMPP Setup Guide for Beginners](XAMPP_SETUP_GUIDE.md) for detailed instructions.

### Prerequisites

- Python 3.11 or higher
- XAMPP (for beginners) or equivalent (MySQL, Apache)
- Modern web browser

### Running the Application

1. Start MySQL database service
2. Create a database named 'event_management'
3. Install Python dependencies:
   ```
   pip install flask flask-login flask-sqlalchemy flask-wtf email-validator gunicorn mysql-connector-python werkzeug
   ```
4. Configure the database connection in app.py
5. Run the application:
   ```
   python main.py
   ```
6. Open your browser and navigate to http://localhost:5000

## Using the Application

### Registration & Login

1. Create an account by clicking 'Register'
2. Choose your user type (Organizer or Attendee)
3. Fill in your details and submit
4. Login using your email and password

### Creating Events (Organizers Only)

Only organizers have permission to create events:

1. Click on 'Create Event' in the navigation bar
2. Fill in the event details (title, description, date/time, location, etc.)
3. Set capacity and pricing options
4. Submit the form to create your event

### Managing Events (Organizers)

1. Go to 'My Events' to see all your created events
2. Edit or delete events as needed
3. View registration statistics

### Browsing and Registering for Events (Attendees)

1. Click on 'Explore Events' to browse all available events
2. Use filters to find specific events
3. Click on an event to view details
4. Register for the event by clicking 'Get Tickets'

### Managing Tickets

1. Go to 'My Tickets' to view all your registered events
2. See event details and ticket information
3. Cancel tickets for events you can no longer attend

## 🛠 Technology Stack

- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Backend**: Python, Flask
- **Database**: MySQL (SQLAlchemy ORM)
- **Authentication**: Flask-Login
- **Forms & Validation**: Flask-WTF, Email-Validator
- **Visualization**: Chart.js

## outputs 
 **Homepage** <img width="923" height="427" alt="image" src="https://github.com/user-attachments/assets/275a9181-7cb0-4f47-9d7e-a46eddae368d" />
**Register page for Attendee and Organizer**
<img width="925" height="432" alt="image" src="https://github.com/user-attachments/assets/7cca88aa-6323-4aa0-a8f8-e0e08b42aa42" />
<img width="930" height="440" alt="image" src="https://github.com/user-attachments/assets/7b250505-4cbf-4e4c-a246-d588d07cd0f2" />

**Login page**
<img width="905" height="409" alt="image" src="https://github.com/user-attachments/assets/6b723fd4-3242-426e-8d9b-8c809befd493" />
<img width="927" height="412" alt="image" src="https://github.com/user-attachments/assets/44e82dd8-3d23-4f4b-a006-85cd4258d7d8" />
**Explore Events**
<img width="930" height="431" alt="image" src="https://github.com/user-attachments/assets/b132bd0c-2cb7-4de7-8200-b2a079978ff9" />
<img width="939" height="397" alt="image" src="https://github.com/user-attachments/assets/07f56db2-232d-49ea-9be8-4efb55c34520" />
## Login page for attendee
<img width="594" height="365" alt="image" src="https://github.com/user-attachments/assets/bc1c03d1-be6a-4492-8271-48987f35ad48" />
 **Explore events**
 <img width="856" height="377" alt="image" src="https://github.com/user-attachments/assets/f0f6c303-3163-4f27-86de-5731ac82d3d1" />
<img width="929" height="338" alt="image" src="https://github.com/user-attachments/assets/b1efd66c-1e16-4537-9289-53b74a6be670" />
<img width="912" height="410" alt="image" src="https://github.com/user-attachments/assets/29652c29-c9bb-4f2e-9c33-bd8b2d66b9a5" />
<img width="872" height="421" alt="image" src="https://github.com/user-attachments/assets/e44f6943-628d-4a39-af72-e34065fe2a10" />
-** 
**My tickets in the attendee account**
<img width="929" height="422" alt="image" src="https://github.com/user-attachments/assets/5072528f-b85b-4379-9e84-d5ed98fb2205" />
<img width="888" height="407" alt="image" src="https://github.com/user-attachments/assets/a2ea3956-f7ec-4db7-8cc7-d717f3adbec6" />
print ticekt page
<img width="547" height="421" alt="image" src="https://github.com/user-attachments/assets/05fafda6-9348-4538-80db-c0032dab8c94" />

## Login page for organizer
<img width="547" height="421" alt="image" src="https://github.com/user-attachments/assets/6dae441b-2fb9-4073-acb5-b6cf2a68539d" />
home page
<img width="745" height="332" alt="image" src="https://github.com/user-attachments/assets/6e90191d-1b29-4169-acba-97d037612249" />
**Organizer Dashboard**
<img width="874" height="358" alt="image" src="https://github.com/user-attachments/assets/a40b61da-5c73-427f-b11a-ba487e369e74" /> 
<img width="860" height="326" alt="image" src="https://github.com/user-attachments/assets/1581f2b7-48cd-4f9d-9ac8-7c8a5962bfda" />
<img width="850" height="412" alt="image" src="https://github.com/user-attachments/assets/d353227a-b39f-4c67-9d71-c58bdb3dabd8" />

-**Events details and Edit options** 
<img width="887" height="341" alt="image" src="https://github.com/user-attachments/assets/b3db5140-a625-44f5-bb62-a75c3ac655a6" />
**Events created** 
<img width="899" height="374" alt="image" src="https://github.com/user-attachments/assets/ee55a07a-4e0d-4725-a3b8-ec40c2fb1f20" />
**Upcoming events**
<img width="904" height="272" alt="image" src="https://github.com/user-attachments/assets/9c489a1d-50e5-4593-a748-21f9de8f95e0" />
on going events
<img width="924" height="278" alt="image" src="https://github.com/user-attachments/assets/61a754fc-36c8-431c-b991-47ca32437e0c" />
**Creating a New Event**
<img width="854" height="418" alt="image" src="https://github.com/user-attachments/assets/02d420cd-fb38-4906-a71f-89d31cee4a5d" />
<img width="844" height="360" alt="image" src="https://github.com/user-attachments/assets/11a65861-afef-42a9-8709-6ffdc457c32a" />
<img width="844" height="328" alt="image" src="https://github.com/user-attachments/assets/037d1f9d-8857-400f-9a7d-44662803b3dc" />
**Account details for organizer**
<img width="914" height="423" alt="image" src="https://github.com/user-attachments/assets/834ee347-13a1-4569-983b-6ae8ebd4606e" />
<img width="886" height="425" alt="image" src="https://github.com/user-attachments/assets/ff279568-6dee-4c52-bedc-13d4ab53b760" />
<img width="219" height="124" alt="image" src="https://github.com/user-attachments/assets/ea64487c-fcf5-4ae0-874b-8c1cd601a064" />
**Accoount details for Attendee**
<img width="911" height="419" alt="image" src="https://github.com/user-attachments/assets/109832d5-2833-4434-b47d-9a0e5decd7c0" />
<img width="869" height="408" alt="image" src="https://github.com/user-attachments/assets/7e024a13-e1bf-49ef-aace-628da459e416" />
<img width="383" height="419" alt="image" src="https://github.com/user-attachments/assets/f0d99371-5a48-4999-846f-917fdf49ae23" />








