# Task Management Application

A full-stack task management application built with **React**, **Node.js**, **Express**, **MongoDB**, and **JWT authentication**. Users can register, login, and manage their daily tasks with complete CRUD functionality.

![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Installation & Setup](#-installation--setup)
- [Project Structure](#-project-structure)
- [Running the Application](#-running-the-application)
- [License](#-license)

---

## 🚀 Features

### User Authentication
- ✅ User Registration with validation
- ✅ Secure Login with JWT tokens
- ✅ Password hashing using bcrypt
- ✅ Protected routes and API endpoints
- ✅ Persistent authentication (localStorage)
- ✅ Automatic token expiration handling

### Task Management
- ✅ Create new tasks with title, description, and status
- ✅ View all tasks in a responsive dashboard
- ✅ Edit existing tasks
- ✅ Delete tasks with confirmation
- ✅ Toggle task status (Pending/Completed)
- ✅ Filter tasks by status (All, Pending, Completed)
- ✅ User-specific tasks (users can only see their own tasks)

### UI/UX Features
- ✅ Fully responsive design (mobile, tablet, desktop)
- ✅ Clean and modern interface with Tailwind CSS
- ✅ Real-time task statistics dashboard
- ✅ Loading states and spinners
- ✅ Success and error notifications
- ✅ Form validation with error messages
- ✅ Smooth animations and transitions
- ✅ Empty state handling

### Security Features
- ✅ Password hashing 
- ✅ JWT-based stateless authentication
- ✅ Protected API routes
- ✅ Input validation and sanitization
- ✅ CORS configuration
- ✅ Error handling middleware

---

## 🛠️ Tech Stack

### Frontend
| Technology |  Purpose |
|-----------|---------|
| React |  UI library |
| React Router DOM | Client-side routing |
| Axios |  HTTP client |
| Tailwind CSS | Utility-first CSS framework |

### Backend
| Technology |  Purpose |
|-----------|---------|
| Node.js |  Runtime environment |
| Express.js |  Web framework |
| MongoDB |  NoSQL database |
| Mongoose |  MongoDB ODM |
| JWT |  Authentication tokens |
| Bcrypt.js |  Password hashing |
| Express Validator |  Input validation |
| CORS |  Cross-origin requests |
| dotenv |  Environment variables |


---

## 🔧 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/<username>/task-management-app.git
cd task-management-app
```

### 2. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create .env file from example
cp .env.example .env
```

**Edit the `backend/.env` file:**
```env
PORT=5000
MONGODB_URI=mongodb+srv://username:password@cluster0.xxxxx.mongodb.net/taskmanager?retryWrites=true&w=majority
JWT_SECRET=your_super_secret_jwt_key_change_this_in_production_12345
JWT_EXPIRE=7d
NODE_ENV=development
CLIENT_URL=http://localhost:3000
```

**Start the backend server:**
```bash
npm run dev
```

✅ Backend server will start on `http://localhost:5000`

### 3. Frontend Setup

Open a **new terminal window**:

```bash
# Navigate to frontend directory (from project root)
cd frontend

# Install dependencies
npm install

# Create .env file from example
cp .env.example .env
```

**Edit the `frontend/.env` file:**
```env
REACT_APP_API_URL=http://localhost:5000/api
```

**Start the frontend development server:**
```bash
npm start
```

✅ Frontend application will open automatically at `http://localhost:3000`

---

## 📁 Project Structure

```
task-management-app/
│
├── backend/                          # Backend Node.js/Express application
│   ├── config/
│   │   └── db.js                    # MongoDB connection configuration
│   │
│   ├── controllers/
│   │   ├── authController.js        # Authentication logic (register, login)
│   │   └── taskController.js        # Task CRUD operations logic
│   │
│   ├── middleware/
│   │   ├── auth.js                  # JWT authentication middleware
│   │   └── errorHandler.js          # Global error handling middleware
│   │
│   ├── models/
│   │   ├── User.js                  # User mongoose schema
│   │   └── Task.js                  # Task mongoose schema
│   │
│   ├── routes/
│   │   ├── authRoutes.js            # Authentication routes
│   │   └── taskRoutes.js            # Task CRUD routes
│   │
│   ├── utils/
│   │   └── validators.js            # Input validation rules
│   │
│   ├── .env.example                 # Example environment variables
│   ├── .gitignore                   # Git ignore file
│   ├── package.json                 # Backend dependencies
│   └── server.js                    # Express server entry point
│
├── frontend/                         # Frontend React application
│   ├── public/
│   │   └── index.html               # HTML template
│   │
│   ├── src/
│   │   ├── components/
│   │   │   ├── Layout.jsx           # Main layout with header/navigation
│   │   │   ├── TaskCard.jsx         # Individual task card component
│   │   │   ├── TaskModal.jsx        # Create/Edit task modal
│   │   │   └── ProtectedRoute.jsx   # Route protection wrapper
│   │   │
│   │   ├── context/
│   │   │   └── AuthContext.jsx      # Global authentication state
│   │   │
│   │   ├── pages/
│   │   │   ├── Login.jsx            # Login page
│   │   │   ├── Register.jsx         # Registration page
│   │   │   └── DashBoard.jsx        # Main dashboard with tasks
│   │   │
│   │   ├── services/
│   │   │   └── api.js               # Axios API service layer
│   │   │
│   │   ├── App.jsx                  # Main App component with routing
│   │   ├── index.js                 # React entry point
│   │   └── index.css                # Global styles with Tailwind
│   │
│   ├── .env.example                 # Example environment variables
│   ├── .gitignore                   # Git ignore file
│   ├── package.json                 # Frontend dependencies
│   ├── tailwind.config.js           # Tailwind CSS configuration
│   └── postcss.config.js            # PostCSS configuration
│
└── README.md                         # Project documentation
```



---

## 🚀 Running the Application

### Development Mode



1. **Start Backend Server** (Terminal 1):
```bash
cd backend
npm run dev
```
Output: `Server running in development mode on port 5000`

2. **Start Frontend Server** (Terminal 2):
```bash
cd frontend
npm start
```
Output: Opens browser at `http://localhost:3000`

### Production Build

**Backend:**
```bash
cd backend
npm start
```

**Frontend:**
```bash
cd frontend
npm run build
# Serve the build folder using a static server
```
---

---
## 📝 Additional Notes

### Code Quality
- ✅ Clean code structure with separation of concerns
- ✅ Consistent naming conventions
- ✅ Comprehensive error handling
- ✅ Input validation on both frontend and backend
- ✅ Secure authentication implementation

### Performance Optimizations
- Database indexing for faster queries
- Efficient React re-renders
- Lazy loading components (can be added)
- API response caching (can be added)

### Future Enhancements
- [ ] Task categories/tags
- [ ] Task priority levels
- [ ] Due dates and reminders
- [ ] Task search functionality
- [ ] Dark mode theme
- [ ] Email notifications
- [ ] Task sharing between users
- [ ] File attachments
- [ ] Activity log
- [ ] Export tasks to CSV/PDF

### Known Limitations
- No forgot password feature
- No email verification
- No profile picture upload
- No real-time updates (WebSocket)

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Author

**Deepanshu Pant**

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## ⭐ Show Your Support

Give a ⭐️ if you like this project!

---

## 🙏 Acknowledgments

- [React Documentation](https://react.dev/)
- [Express.js Documentation](https://expressjs.com/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Tailwind CSS Documentation](https://tailwindcss.com/)
- [JWT.io](https://jwt.io/)


---

**Made with ❤️ using React, Node.js, Express, and MongoDB**
