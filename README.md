# 👥 Employee Management System

A comprehensive full-stack web application for managing employee records with complete CRUD operations, authentication, and role-based access control.

**Created for Prodigy Internship - Task 2**

---

## 🌟 Features

### Core Features
- ✅ **Complete CRUD Operations** - Create, Read, Update, Delete employees
- ✅ **Admin Authentication** - Secure login system for administrators
- ✅ **Advanced Search & Filter** - Search by name, email, ID, department, or status
- ✅ **Pagination** - Efficient data handling with pagination
- ✅ **Real-time Statistics** - Dashboard with employee stats and metrics
- ✅ **Data Validation** - Comprehensive validation on both frontend and backend
- ✅ **Responsive Design** - Works perfectly on all devices

### Security Features
- 🔐 **Password Hashing** - Bcrypt encryption for secure password storage
- 🔐 **JWT Authentication** - Token-based session management
- 🔐 **Protected API Routes** - All employee operations require authentication
- 🔐 **Input Validation** - Prevents SQL injection and XSS attacks
- 🔐 **Email Uniqueness** - Prevents duplicate employee emails
- 🔐 **Employee ID Validation** - Ensures unique employee IDs

### Employee Management
- 📋 **Detailed Employee Records** - Track comprehensive employee information
- 📋 **Department Management** - Organize by IT, HR, Finance, Marketing, etc.
- 📋 **Status Tracking** - Active, Inactive, On Leave
- 📋 **Salary Information** - Secure salary data management
- 📋 **Address Management** - Complete address information
- 📋 **Date Tracking** - Joining date and creation timestamps

---

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **bcryptjs** - Password hashing
- **jsonwebtoken** - JWT authentication
- **express-validator** - Input validation

### Frontend
- **React** - UI library
- **Vite** - Build tool
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **Tailwind CSS** - Styling
- **React Icons** - Icon library
- **Context API** - State management

---

## 📋 Prerequisites

- **Node.js** (v14 or higher) - [Download](https://nodejs.org/)
- **MongoDB** (v4 or higher) - [Download](https://www.mongodb.com/try/download/community)
- **npm** or **yarn** - Comes with Node.js

---

## 🚀 Installation & Setup

### Step 1: Clone the Repository

```bash
git clone <your-repo-url>
cd employee-management-system
```

### Step 2: Setup Backend

```bash
cd backend
npm install
```

The `.env` file is already configured with default settings:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/employee-management-db
JWT_SECRET=employee_management_secure_jwt_secret_key_2024
JWT_EXPIRE=7d
NODE_ENV=development
```

### Step 3: Setup Frontend

```bash
cd ../frontend
npm install
```

### Step 4: Start MongoDB

Ensure MongoDB is running:

```bash
# macOS (Homebrew)
brew services start mongodb-community

# Windows (as administrator)
net start MongoDB

# Linux
sudo systemctl start mongod
```

### Step 5: Run the Application

**Terminal 1 - Backend:**
```bash
cd backend
npm run dev
```
Backend runs on `http://localhost:5000`

**Terminal 2 - Frontend:**
```bash
cd frontend
npm run dev
```
Frontend runs on `http://localhost:5173`

---

## 🎯 Usage Guide

### 1. Admin Registration
- Open `http://localhost:5173`
- Click "Register here" or navigate to `/register`
- Create admin account with:
  - Full Name
  - Email
  - Password (min 6 characters)

### 2. Login
- Use your registered admin credentials
- You'll be redirected to the dashboard

### 3. Dashboard Overview
View real-time statistics:
- Total Employees
- Active Employees
- Inactive Employees
- Employees On Leave

### 4. Add Employee
1. Click "Add Employee" button
2. Fill in the form:
   - **Required Fields:**
     - Employee ID (unique)
     - First Name & Last Name
     - Email (unique)
     - Phone (10 digits)
     - Department
     - Position
     - Salary
     - Date of Joining
     - Status
   - **Optional Fields:**
     - Address (Street, City, State, Zip, Country)
3. Click "Add Employee"

### 5. Search & Filter
- **Search:** Type in search box to find by name, email, or ID
- **Filter by Department:** Select from dropdown
- **Filter by Status:** Active, Inactive, or On Leave

### 6. Edit Employee
1. Click the edit icon (✏️) next to any employee
2. Update the information
3. Click "Update Employee"

### 7. Delete Employee
1. Click the delete icon (🗑️) next to any employee
2. Confirm deletion

### 8. Pagination
- Use "Previous" and "Next" buttons to navigate pages
- 10 employees per page

---

## 📁 Project Structure

```
employee-management-system/
├── backend/
│   ├── config/
│   │   └── db.js                    # Database connection
│   ├── controllers/
│   │   ├── adminController.js       # Admin auth logic
│   │   └── employeeController.js    # Employee CRUD operations
│   ├── middleware/
│   │   └── auth.js                  # JWT verification
│   ├── models/
│   │   ├── Admin.js                 # Admin schema
│   │   └── Employee.js              # Employee schema
│   ├── routes/
│   │   ├── admin.js                 # Admin routes
│   │   └── employees.js             # Employee routes
│   ├── .env                         # Environment variables
│   ├── package.json
│   └── server.js                    # Entry point
│
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── EmployeeModal.jsx    # Add/Edit employee form
    │   │   ├── Navbar.jsx           # Navigation bar
    │   │   └── PrivateRoute.jsx     # Route protection
    │   ├── context/
    │   │   └── AuthContext.jsx      # Authentication state
    │   ├── pages/
    │   │   ├── Dashboard.jsx        # Main dashboard
    │   │   ├── Login.jsx            # Admin login
    │   │   └── Register.jsx         # Admin registration
    │   ├── App.jsx                  # Main app component
    │   ├── main.jsx                 # Entry point
    │   └── index.css                # Tailwind CSS
    ├── package.json
    └── vite.config.js
```

---

## 🌐 API Endpoints

### Admin Authentication

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| POST | `/api/admin/register` | Register new admin | Public |
| POST | `/api/admin/login` | Login admin | Public |
| GET | `/api/admin/me` | Get current admin | Private |

### Employee Management

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| POST | `/api/employees` | Create employee | Private |
| GET | `/api/employees` | Get all employees (with filters) | Private |
| GET | `/api/employees/:id` | Get single employee | Private |
| PUT | `/api/employees/:id` | Update employee | Private |
| DELETE | `/api/employees/:id` | Delete employee | Private |
| GET | `/api/employees/stats/overview` | Get statistics | Private |

### Query Parameters for GET /api/employees

- `page` - Page number (default: 1)
- `limit` - Items per page (default: 10)
- `search` - Search term (searches name, email, employeeId)
- `department` - Filter by department
- `status` - Filter by status

**Example:**
```
GET /api/employees?page=1&limit=10&department=IT&status=Active&search=john
```

---

## 🧪 API Testing

### Create Employee
```http
POST http://localhost:5000/api/employees
Authorization: Bearer YOUR_JWT_TOKEN
Content-Type: application/json

{
  "employeeId": "EMP001",
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@company.com",
  "phone": "1234567890",
  "department": "IT",
  "position": "Software Engineer",
  "salary": 75000,
  "dateOfJoining": "2024-01-15",
  "status": "Active",
  "address": {
    "street": "123 Main St",
    "city": "New York",
    "state": "NY",
    "zipCode": "10001",
    "country": "USA"
  }
}
```

### Get All Employees
```http
GET http://localhost:5000/api/employees?page=1&limit=10
Authorization: Bearer YOUR_JWT_TOKEN
```

### Update Employee
```http
PUT http://localhost:5000/api/employees/EMPLOYEE_ID
Authorization: Bearer YOUR_JWT_TOKEN
Content-Type: application/json

{
  "position": "Senior Software Engineer",
  "salary": 85000
}
```

### Delete Employee
```http
DELETE http://localhost:5000/api/employees/EMPLOYEE_ID
Authorization: Bearer YOUR_JWT_TOKEN
```

---

## 🔒 Security Features

### Password Security
- Passwords hashed with bcrypt (salt rounds: 10)
- Never stored in plain text
- Password validation (minimum 6 characters)

### Authentication
- JWT tokens with 7-day expiration
- Token stored in localStorage
- Automatic token validation on protected routes

### Data Validation
- Email format validation
- Phone number validation (10 digits)
- Unique constraints on employeeId and email
- Required field validation
- Salary must be non-negative

### Authorization
- All employee operations require admin authentication
- Invalid tokens are rejected
- Expired tokens require re-login

---

## 🎨 UI Features

### Dashboard Statistics
- Real-time employee count
- Active/Inactive/On Leave breakdown
- Department-wise distribution

### Advanced Table
- Sortable columns
- Status badges with colors
- Hover effects
- Responsive design

### Modal Form
- Clean, user-friendly interface
- Real-time validation
- Error handling
- Loading states

### Search & Filter
- Instant search results
- Multiple filter options
- Reset filters easily

---

## 🚢 Deployment

### Backend (Railway/Render)
1. Push code to GitHub
2. Connect repository to Railway/Render
3. Set environment variables
4. Deploy!

### Frontend (Vercel/Netlify)
1. Push code to GitHub
2. Connect repository
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Deploy!

### Environment Variables for Production

**Backend:**
```env
PORT=5000
MONGODB_URI=your_mongodb_atlas_uri
JWT_SECRET=your_production_secret_key
JWT_EXPIRE=7d
NODE_ENV=production
```

**Frontend:**
Update axios base URL in production or use proxy

---

## 📝 Database Schema

### Admin Collection
```javascript
{
  _id: ObjectId,
  name: String,
  email: String (unique),
  password: String (hashed),
  role: String (default: "admin"),
  createdAt: Date
}
```

### Employee Collection
```javascript
{
  _id: ObjectId,
  employeeId: String (unique),
  firstName: String,
  lastName: String,
  email: String (unique),
  phone: String,
  department: String (enum),
  position: String,
  salary: Number,
  dateOfJoining: Date,
  address: {
    street: String,
    city: String,
    state: String,
    zipCode: String,
    country: String
  },
  status: String (enum: Active, Inactive, On Leave),
  createdBy: ObjectId (ref: Admin),
  createdAt: Date,
  updatedAt: Date
}
```

---

## 🐛 Troubleshooting

### MongoDB Connection Error
- Ensure MongoDB is running: `brew services list` (macOS)
- Check connection string in `.env`
- Verify port 27017 is not in use

### Port Already in Use
- Change PORT in backend `.env`
- Update CORS origin in `server.js`

### Authentication Errors
- Clear localStorage and login again
- Check if token is expired (7 days)
- Verify JWT_SECRET is set correctly

### Employee Not Created
- Check required fields are filled
- Verify employeeId is unique
- Ensure email is unique
- Check phone number is 10 digits

---

## ✅ Testing Checklist

- [ ] Admin can register
- [ ] Admin can login
- [ ] Admin can logout
- [ ] Can create new employee
- [ ] Can view all employees
- [ ] Can search employees
- [ ] Can filter by department
- [ ] Can filter by status
- [ ] Can edit employee
- [ ] Can delete employee
- [ ] Statistics display correctly
- [ ] Pagination works
- [ ] Form validation works
- [ ] Error messages display
- [ ] Responsive on mobile

---

## 🎓 Learning Outcomes

This project demonstrates:
- Full-stack application architecture
- RESTful API design
- CRUD operations implementation
- Authentication & authorization
- Database modeling with Mongoose
- React state management
- Form handling and validation
- API integration with Axios
- Responsive UI design
- Error handling strategies

---

## 📞 Support

For issues or questions:
1. Check the troubleshooting section
2. Verify all dependencies are installed
3. Ensure MongoDB is running
4. Check console for error messages

---

## 📚 Additional Features to Add

- [ ] Export employees to CSV/Excel
- [ ] Import employees from CSV
- [ ] Employee profile pictures
- [ ] Email notifications
- [ ] Attendance tracking
- [ ] Leave management
- [ ] Performance reviews
- [ ] Salary history
- [ ] Document management
- [ ] Advanced analytics

---

## 📄 License

MIT License - Feel free to use for learning purposes.

---

## 👨‍💻 Author

Created as part of **Prodigy Internship - Full Stack Web Development**

**Task 2:** Employee Management System with CRUD Operations

---

**Happy Coding! 🎉**
