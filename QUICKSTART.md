# 🚀 QUICK START GUIDE - Employee Management System

## ⚡ Get Running in 5 Minutes!

### Step 1: Install MongoDB

**Windows:**
- Download: https://www.mongodb.com/try/download/community
- Install and start MongoDB service

**macOS:**
```bash
brew tap mongodb/brew
brew install mongodb-community
brew services start mongodb-community
```

**Linux:**
```bash
sudo apt-get install mongodb
sudo systemctl start mongod
```

---

### Step 2: Install Dependencies

**Terminal 1 - Backend:**
```bash
cd employee-management-system/backend
npm install
```

**Terminal 2 - Frontend:**
```bash
cd employee-management-system/frontend
npm install
```

---

### Step 3: Start the Application

**Terminal 1 - Backend:**
```bash
cd backend
npm run dev
```
✅ Look for: "Server running on port 5000" and "MongoDB Connected"

**Terminal 2 - Frontend:**
```bash
cd frontend
npm run dev
```
✅ Look for: "Local: http://localhost:5173"

---

### Step 4: Access the Application

Open browser: **http://localhost:5173**

---

### Step 5: Create Admin Account

1. Click "Register here"
2. Fill in:
   - **Name:** Admin User
   - **Email:** admin@company.com
   - **Password:** admin123
   - **Confirm Password:** admin123
3. Click "Create Admin Account"

---

### Step 6: Add Your First Employee

1. You'll be on the Dashboard
2. Click "Add Employee" button
3. Fill in the form:
   ```
   Employee ID: EMP001
   First Name: John
   Last Name: Doe
   Email: john.doe@company.com
   Phone: 1234567890
   Department: IT
   Position: Software Engineer
   Salary: 75000
   Date of Joining: 2024-01-15
   Status: Active
   ```
4. Click "Add Employee"

---

## 🎯 What You Can Do Now

### ✅ Dashboard Features
- View employee statistics
- See total, active, inactive, and on-leave employees
- View employee list in a table

### ✅ Search & Filter
- **Search:** Type employee name, email, or ID
- **Filter by Department:** IT, HR, Finance, etc.
- **Filter by Status:** Active, Inactive, On Leave

### ✅ CRUD Operations
- **Create:** Add new employees
- **Read:** View employee details
- **Update:** Edit employee information (click ✏️ icon)
- **Delete:** Remove employees (click 🗑️ icon)

### ✅ Advanced Features
- Pagination (10 employees per page)
- Real-time statistics updates
- Form validation
- Responsive design

---

## 📸 For Your Internship Submission

### 1. Screenshots to Take
- ✅ Login page
- ✅ Dashboard with statistics
- ✅ Employee table with data
- ✅ Add Employee modal (filled)
- ✅ Edit Employee modal
- ✅ Search/filter functionality

### 2. GitHub Repository

```bash
cd employee-management-system
git init
git add .
git commit -m "Task 2: Employee Management System with CRUD operations"

# Create repo on GitHub, then:
git remote add origin YOUR_GITHUB_URL
git push -u origin main
```

### 3. What to Include in Submission
- 📁 GitHub repository link
- 📸 Screenshots of all features
- 📝 Brief description of:
  - CRUD operations implemented
  - Security features (authentication, validation)
  - Search and filter functionality
  - Technologies used

---

## 🔥 Key Features to Highlight

### 1. **Complete CRUD Operations**
- ✅ Create new employees
- ✅ Read/view employee list
- ✅ Update employee information
- ✅ Delete employees

### 2. **Security & Validation**
- ✅ Admin authentication with JWT
- ✅ Password hashing with bcrypt
- ✅ Protected API routes
- ✅ Email and phone validation
- ✅ Unique employee ID and email

### 3. **Advanced Features**
- ✅ Search across multiple fields
- ✅ Filter by department and status
- ✅ Pagination for large datasets
- ✅ Real-time statistics dashboard
- ✅ Responsive design

### 4. **Professional UI**
- ✅ Clean, modern interface
- ✅ Color-coded status badges
- ✅ Modal forms for add/edit
- ✅ Icons for better UX
- ✅ Loading states

---

## ❓ Common Issues & Quick Fixes

### Issue: "MongoDB connection failed"
**Fix:**
```bash
# Check if MongoDB is running
brew services list  # macOS
# or
sudo systemctl status mongod  # Linux

# Start MongoDB if stopped
brew services start mongodb-community  # macOS
```

### Issue: "Port 5000 already in use"
**Fix:**
- Change PORT in `backend/.env` to 5001
- Update proxy in `frontend/vite.config.js`

### Issue: "Cannot create employee"
**Fix:**
- Make sure you're logged in as admin
- Check all required fields are filled
- Verify Employee ID is unique
- Verify Email is unique
- Phone must be exactly 10 digits

### Issue: "Token expired"
**Fix:**
- Logout and login again
- Tokens expire after 7 days

---

## 🧪 Test Data for Quick Demo

### Sample Admin
```
Email: admin@company.com
Password: admin123
```

### Sample Employees

**Employee 1:**
```
ID: EMP001
Name: John Doe
Email: john.doe@company.com
Phone: 1234567890
Department: IT
Position: Software Engineer
Salary: 75000
Date: 2024-01-15
Status: Active
```

**Employee 2:**
```
ID: EMP002
Name: Jane Smith
Email: jane.smith@company.com
Phone: 9876543210
Department: HR
Position: HR Manager
Salary: 85000
Date: 2024-01-10
Status: Active
```

**Employee 3:**
```
ID: EMP003
Name: Bob Johnson
Email: bob.johnson@company.com
Phone: 5555555555
Department: Finance
Position: Accountant
Salary: 65000
Date: 2024-02-01
Status: On Leave
```

---

## ✅ Submission Checklist

- [ ] App runs without errors
- [ ] Can create admin account
- [ ] Can login as admin
- [ ] Can add employees
- [ ] Can view employee list
- [ ] Can search employees
- [ ] Can filter by department
- [ ] Can filter by status
- [ ] Can edit employees
- [ ] Can delete employees
- [ ] Statistics display correctly
- [ ] Pagination works
- [ ] Code pushed to GitHub
- [ ] Screenshots taken
- [ ] README.md complete

---

## 🎉 Congratulations!

You've successfully built a complete employee management system with:
- Full CRUD operations
- Secure authentication
- Advanced search and filtering
- Professional dashboard
- Real-time statistics

**Next Steps:**
- Add more employees
- Test all CRUD operations
- Take screenshots for submission
- Push to GitHub
- Submit to Prodigy!

---

**Good luck with your internship! 🚀**
