# International Payments Portal - Secure Employee Portal

## Project Overview
A secure international payments portal built with the MERN stack (MongoDB, Express.js, React, Node.js) that allows employees to create and manage international payments with enterprise-level security features.

## 🚀 Quick Start Guide

### Prerequisites
- Node.js (v14 or higher)
- MongoDB Atlas account
- Modern web browser (Chrome, Firefox, Safari)

### Installation & Setup

#### Backend Setup:
1. Navigate to the BACKEND folder:
     cd BACKEND


2. Install dependencies:
     npm install

3. Set up environment variables in .env file:
     MONGODB_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret_key
     PORT=3001

4. Seed the database with pre-created users:
     npm run seed

5. Start the backend server:
     npm run dev


##### Frontend Setup:

1. Navigate to the FRONTEND folder:
     cd frontend
  
2. Install dependencies:
     npm install

3. Start the React application:
     npm start

###### Test Credentials
Admin Account:
Username: admin_user
Password: Admin123!@#
Role: Administrator (full access)

Employee Accounts:
Username: john_doe
Password: SecurePass123!
Role: Employee

Username: jane_smith
Password: AnotherSecure456!
Role: Employee

###### Accessing the Application

1. Open your web browser and go to: http://localhost:3000

2. Login using any of the credentials above

3. Navigate through the payment portal features


###### Functionality Testing Guide

Test 1: Login & Authentication
1. Go to http://localhost:3000
2. Try invalid credentials (should show error)
3. Login with valid credentials (should redirect to payments dashboard)

Test 2: View Payment History
1. After login, view the payment dashboard
2. See sample payments with details (recipient, amount, status)

Test 3: Create New Payment
1. Click "New Payment" button
2. Fill in payment form with valid data:

Recipient Name: "Test Company Ltd"
IBAN: "US12345678901234567890"
SWIFT/BIC: "BOFAUS3N"
Amount: "1000.00"
Currency: "USD"

3. Submit form (should show success message)

Test 4: Input Validation Testing
1. Try submitting invalid data:

Invalid IBAN format
Invalid SWIFT code
Negative amounts
Special characters in recipient name

2. All should show appropriate error messages

Test 5: Security Features
1. Try accessing /payments without logging in (should redirect to login)
2. Test rate limiting with multiple failed login attempts
3. Verify JWT token expiration