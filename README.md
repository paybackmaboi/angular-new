## Collaborative Development of a Full-Stack Application: Group 6

##  Project Description
This project is a full-stack web application designed to provide user authentication, role-based access control, profile management, and email verification. It consists of:
- **Backend:** Node.js + MySQL API
- **Frontend:** Angular 19
- **Testing:** Fake backend for initial testing, real API for integration.

The application allows users to register, log in, and manage their profiles securely with authentication and role-based access control.

---

##  Setup Instructions

### **Prerequisites**
Before setting up the project, ensure you have the following installed:
- **Node.js** (v16+)
- **MySQL** (Latest Version)
- **Angular CLI** (v19+)
- **Git** (Latest Version)

### **Backend Setup (Node.js + MySQL)**
1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/groupX-fullstack-app.git
   cd backend
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Configure the environment variables:**
   Create a `.env` file and add:
   ```plaintext
   DB_HOST=localhost
   DB_USER=root
   DB_PASS=yourpassword
   JWT_SECRET=your_secret_key
   SMTP_HOST=smtp.mailtrap.io
   SMTP_USER=your_username
   SMTP_PASS=your_password
   ```
4. **Run the database migrations:**
   ```bash
   npm run migrate
   ```
5. **Start the backend server:**
   ```bash
   npm start
   ```

### **Frontend Setup (Angular 19)**
1. **Navigate to the frontend directory:**
   ```bash
   cd frontend
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Run the Angular app:**
   ```bash
   ng serve
   ```
4. **Using the Fake Backend:**
   - Open `app.module.ts`
   - Ensure `fakeBackendProvider` is included in the `providers` array:
   ```typescript
   providers: [fakeBackendProvider]
   ```
   - This allows testing without connecting to the real API.

---

## API Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|---------|-------------|--------------|
| `POST`   | `/api/auth/register` | Register a new user | No |
| `POST`   | `/api/auth/login` | Login user | No |
| `GET`    | `/api/users/me` | Get current user details | Yes |
| `PUT`    | `/api/users/update` | Update user profile | Yes |
| `POST`   | `/api/auth/forgot-password` | Request password reset | No |

### **Request & Response Example**
#### **User Login Request**
```json
{
  "email": "user@example.com",
  "password": "password123"
}
```
#### **User Login Response**
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI..."
}
```

---

## Frontend Features
- **User Authentication**: Register, Login, Logout
- **Profile Management**: Update profile details
- **Role-Based Access**: Different UI for Admin and Users
- **Email Verification & Password Reset**
- **Fake Backend for Testing**

---

## Testing Instructions

### **Frontend Testing**
1. **Fake Backend Testing:**  
   - Enable `fakeBackendProvider` in `app.module.ts`.  
   - Test UI interactions (login, register, etc.).

2. **Real API Testing:**  
   - Disable the fake backend, connect frontend to the real API.
   - Verify that all features work as expected.

---

## Contributors

| Name | Role |
|------|------|
| Lourd Angelo Bufete | Backend Developer |
| Romy A. Formentera Jr. | Frontend Developer |
| Roy P. Estorco | Tester & DevOps Lead |
| Raquel Pacure | Documentation Specialist (FrontEnd) |
| Ly Ann Kate Candido | Documentation Specialist (BackEnd) |
| Jade Steve Molejon | Frontend Developer |

