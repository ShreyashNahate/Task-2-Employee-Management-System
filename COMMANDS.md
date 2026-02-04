# 📋 COPY-PASTE COMMANDS

Simple copy-paste commands to get started!

---

## 🎯 TERMINAL 1 - Backend Setup

### 1. Navigate to backend
```bash
cd employee-management-system/backend
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start backend server
```bash
npm run dev
```

✅ **Success:** You should see:
```
Server running in development mode on port 5000
MongoDB Connected: localhost
```

🔴 **Keep this terminal running!**

---

## 🎯 TERMINAL 2 - Frontend Setup

### 1. Open NEW terminal, navigate to frontend
```bash
cd employee-management-system/frontend
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start frontend
```bash
npm run dev
```

✅ **Success:** You should see:
```
VITE v5.0.8  ready in XXX ms

  ➜  Local:   http://localhost:5173/
```

🔴 **Keep this terminal running!**

---

## 🌐 Open in Browser

```
http://localhost:5173
```

---

## 👤 Create First Admin

1. Click "Register here"
2. Fill in:
   - **Name:** Admin User
   - **Email:** admin@company.com
   - **Password:** admin123
   - **Confirm:** admin123
3. Click "Create Admin Account"

---

## 👥 Add Sample Employees

### Employee 1:
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

### Employee 2:
```
Employee ID: EMP002
First Name: Jane
Last Name: Smith
Email: jane.smith@company.com
Phone: 9876543210
Department: HR
Position: HR Manager
Salary: 85000
Date of Joining: 2024-01-10
Status: Active
```

### Employee 3:
```
Employee ID: EMP003
First Name: Bob
Last Name: Johnson
Email: bob.johnson@company.com
Phone: 5555555555
Department: Finance
Position: Accountant
Salary: 65000
Date of Joining: 2024-02-01
Status: On Leave
```

---

## 🛑 To Stop the App

Press `Ctrl + C` in both terminal windows.

---

## 🔄 To Restart Later

**Terminal 1:**
```bash
cd employee-management-system/backend
npm run dev
```

**Terminal 2:**
```bash
cd employee-management-system/frontend
npm run dev
```

---

## 📸 GitHub Setup

### 1. Initialize Git
```bash
cd employee-management-system
git init
git add .
git commit -m "Initial commit: Employee Management System - Prodigy Task 2"
```

### 2. Create GitHub Repository
- Go to github.com
- Click "New Repository"
- Name: `prodigy-task2-employee-management`
- Don't initialize with README
- Click "Create"

### 3. Push to GitHub
```bash
git remote add origin https://github.com/YOUR_USERNAME/prodigy-task2-employee-management.git
git branch -M main
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username!

---

## 🧪 Test All Features

### ✅ CRUD Operations
1. **Create:** Add employee using "Add Employee" button
2. **Read:** View employees in the table
3. **Update:** Click edit icon (✏️) and modify data
4. **Delete:** Click delete icon (🗑️) and confirm

### ✅ Search & Filter
1. **Search:** Type in search box
2. **Filter Department:** Select from dropdown
3. **Filter Status:** Select Active/Inactive/On Leave

### ✅ Pagination
1. Add more than 10 employees
2. Use Previous/Next buttons

---

## 📱 Quick Commands Reference

### Check if MongoDB is running (macOS)
```bash
brew services list
```

### Start MongoDB (macOS)
```bash
brew services start mongodb-community
```

### Check MongoDB status (Linux)
```bash
sudo systemctl status mongod
```

### Start MongoDB (Linux)
```bash
sudo systemctl start mongod
```

### Kill process on port 5000 (if needed)
```bash
# macOS/Linux
lsof -ti:5000 | xargs kill

# Windows
netstat -ano | findstr :5000
taskkill /PID <PID_NUMBER> /F
```

---

## ✅ That's It!

Your Employee Management System is running!

Ready to submit to Prodigy! 🎉
