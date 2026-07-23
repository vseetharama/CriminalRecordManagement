# Police Crime Record Management System

A web-based Police Crime Record Management System developed to help police departments securely manage officer accounts and criminal records. The system provides authentication, crime record management, and a user-friendly interface for efficient record handling.

## 📌 Project Overview

The Police Crime Record Management System is designed to digitize criminal record management. It allows authorized police personnel to register, log in securely, and manage criminal records using a web application.

This project consists of:
- **Frontend:** Next.js (React)
- **Backend:** Flask (Python)
- **Database:** MongoDB
- **Authentication:** Bcrypt Password Hashing

---

## 🛠 Technologies Used

### Frontend
- Next.js
- React.js
- Tailwind CSS
- Flowbite React
- JavaScript
- HTML5
- CSS3

### Backend
- Python
- Flask
- Flask-CORS
- PyMongo
- python-dotenv
- bcrypt

### Database
- MongoDB

---

## 📂 Project Structure

```
Project
│
├── DBMS_mini_project-master/      # Frontend
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── POLICE_APP_backend-main/       # Backend
│   ├── app.py
│   ├── .env
│   ├── requirement.txt
│   └── ...
```

---

## ✨ Features

- Police Officer Registration
- Secure Login Authentication
- Password Encryption using Bcrypt
- Criminal Record Management
- Add and View Criminal Records
- REST API Communication
- MongoDB Database Integration
- Responsive User Interface

---

## ⚙️ Backend Working

The backend is developed using **Flask** and exposes REST APIs for communication with the frontend.

### Main Functions
- Receives requests from the frontend.
- Validates user inputs.
- Connects to MongoDB.
- Performs CRUD operations.
- Sends JSON responses back to the frontend.

### API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | `/` | Check API status |
| POST | `/register` | Register a police officer |
| POST | `/login` | Authenticate police officer |

---

## 💾 Database

The application uses **MongoDB** as the database.

### Collections

### police
Stores police officer information:
- policeId
- policeName
- department
- policeAddress
- designation
- password (encrypted)
- createdAt

### criminal_record
Stores criminal record details used by the application.

---

## 🔗 Frontend and Backend Connection

The frontend communicates with the Flask backend using HTTP requests.

### Workflow

1. User enters information in the web application.
2. Frontend sends a request to the Flask API.
3. Flask processes the request.
4. Backend connects to MongoDB using PyMongo.
5. Data is stored or retrieved from MongoDB.
6. Backend returns a JSON response.
7. Frontend displays the result.

### System Architecture

```
+------------------+
| Next.js Frontend |
+------------------+
         |
         | HTTP Requests (GET/POST)
         |
         ▼
+------------------+
| Flask Backend    |
+------------------+
         |
         | PyMongo
         |
         ▼
+------------------+
| MongoDB Database |
+------------------+
         |
         ▼
JSON Response → Frontend
```

---

## 🔒 Security

- Passwords are encrypted using **bcrypt** before storing in the database.
- MongoDB connection string is stored securely in the `.env` file.
- Flask-CORS enables secure communication between frontend and backend.

---

## ▶️ Installation

### Clone the Repository

```bash
git clone <repository-url>
```

### Frontend

```bash
cd DBMS_mini_project-master
npm install
npm run dev
```

### Backend

```bash
cd POLICE_APP_backend-main
pip install -r requirement.txt
python app.py
```

---

## 🔑 Environment Variables

Create a `.env` file inside the backend folder.

```env
MONGODB_URI=your_mongodb_connection_string
```

---

## 🚀 Future Enhancements

- JWT-based Authentication
- Role-Based Access Control
- Crime Analytics Dashboard
- FIR PDF Generation
- Search and Filter Records
- Email Notifications
- Image Upload Support

---

## 📄 License

This project is developed for educational purposes as a DBMS Mini Project.
