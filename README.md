# **Knowledge Nest**

**Knowledge Nest** is an innovative full-stack web application for online learning and course management. It bridges the gap between students and instructors by providing a secure platform where students can explore and enroll in courses, and instructors can create, manage, and analyze their course offerings with ease. The platform is designed to prioritize seamless user experiences and robust security through advanced ***authentication, authorization, and role-based access control (RBAC)***.

At the core of Knowledge Nest lies a secure and scalable authentication and authorization system. It uses **JWT (JSON Web Tokens)** for verifying user sessions and **bcrypt.js** for hashing passwords, ensuring data integrity and security. ***The application employs Role-Based Access Control (RBAC) to define specific permissions for two distinct user roles:***  **- students and instructors**.

- **Students** can explore the course catalog, enroll in courses, and manage their learning progress. They gain access to exclusive course content and detailed course information.
- **Instructors** have advanced capabilities to create, manage, and analyze courses. They can monitor key metrics such as student enrollment numbers and revenue, both at the individual course level and across all their offerings via an analytics dashboard.
- By implementing **protected routes**, Knowledge Nest ensures that users can only access features appropriate for their roles. For instance, ***instructors are restricted from accessing student-specific routes and vice versa***. This makes the system both secure and intuitive.

---
## **Features**

### **Authentication System**
- Secure user registration, login, and logout functionality.
- Passwords are encrypted using **bcrypt.js** to prevent unauthorized access.
- User sessions are managed through **JWT**, ensuring a seamless and secure user experience.

### **Role-Based Access Control (RBAC)**

#### **Students:**
- Access the course catalog and enroll in courses.
- Manage their enrolled courses and view detailed course information.

#### **Instructors:**
- Create, update, and delete courses with ease.
- View a dashboard featuring key insights:
  - Total number of students enrolled.
  - Revenue generated from courses.
  - Details of enrolled students and their course progress.

#### **Granular Route Protection:**
- Routes like `/instructor` are restricted to authenticated instructors.
- Routes like `/home`, `/courses`, or `/course/details/:id` are accessible only to authenticated students.

### **Protected Routes**
- Critical routes are protected based on authentication and authorization.
- Instructors are granted exclusive access to manage courses and view analytics.
- Students are restricted to learning-related functionalities, maintaining a clear separation of privileges.

### **Payment Integration**
- **PayPal** payment gateway ensures secure and hassle-free payments for course enrollment.

### **Media Storage**
- **Cloudinary** integration provides a reliable solution for uploading and storing course-related media, including images and videos.


---

## **Libraries and Packages**

### **Backend**
- **express**: Web framework for Node.js.
- **mongoose**: MongoDB object modeling for Node.js.
- **jsonwebtoken**: JWT implementation for authentication.
- **bcryptjs**: Library for hashing and validating passwords.
- **cloudinary**: API for media file storage.
- **paypal-rest-sdk**: Integration with PayPal's payment gateway.

### **Frontend**
- **axios**: HTTP client for making API requests.
- **react-router-dom**: For navigation and routing.

---


## **Tech Stack**
- **Frontend**: React.js
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT, bcrypt.js
- **Payment**: PayPal REST SDK
- **File Storage**: Cloudinary

---
## **Project Walkthrough**

### Common Sign UP and Sign IN Page
- SING UP
[![SING UP](./assests/img1.png)](./assets/img2.png)
- SING IN
[![SING IN](./assests/img2.png)](./assets/img2.png)

### STUDENTS VIEW
- HOME PAGE
[![Home Page](./assests/img3.png)](./assets/img3.png)
[![Home Page](./assests/img4.png)](./assets/img4.png)
- COURSES PAGE
[![SING UP](./assests/img5.png)](./assets/img5.png)
- FILTERED SEARCH
[![SING UP](./assests/img6.png)](./assets/img6.png)
[![SING UP](./assests/img7.png)](./assets/img7.png)
[![SING UP](./assests/img8.png)](./assets/img8.png)
- COURSE DETAILS PAGE
[![SING UP](./assests/img10.png)](./assets/img10.png)
- MY COURSE PAGE
[![SING UP](./assests/img11.png)](./assets/img11.png)
- COURSE PROGRESS PAGE
[![SING UP](./assests/img12.png)](./assets/img12.png)
[![SING UP](./assests/img13.png)](./assets/img13.png)

### **INSTRUCTORS VIEW**
- DASHBOARD FOR COURSE ANALYTICS (eg, Revenue Earned)
[![SING UP](./assests/img14.png)](./assets/img14.png)
- CREATE, VIEW, EDIT, DELETE COURSES
[![SING UP](./assests/img15.png)](./assets/img15.png)
[![SING UP](./assests/img16.png)](./assets/img16.png)
[![SING UP](./assests/img17.png)](./assets/img17.png)
[![SING UP](./assests/img18.png)](./assets/img18.png)



---

## **Installation and Setup (To run Locally)**

### **Prerequisites**
1. Install **Node.js** and **npm**.
2. Set up **MongoDB** (local instance or MongoDB Atlas).
3. Create accounts on **Cloudinary** and **PayPal Developer Portal** to get API credentials.

### **Clone the Repository**
```bash
git clone https://github.com/Divas-Sagta/Knowledge-Nest.git
cd knowledge-nest
```
### **Backend Setup**
1. Navigate to the server directory
   ```bash 
   cd server
2. Install dependencies:
   ```bash
   npm install
3. Create a .env file in the server directory with the following environment variables:
   ```bash
   PORT= backend_server_port
   MONGO_URI= your_mongodb_connection_string
   CLIENT_URL= url_where_frontend_is_running
   CLOUDINARY_CLOUD_NAME= your_cloud_name
   CLOUDINARY_API_KEY= your_api_key
   CLOUDINARY_API_SECRET= your_api_secret
   PAYPAL_CLIENT_ID= your_paypal_client_id
   PAYPAL_CLIENT_SECRET= your_paypal_client_secret

4. Start Backend Server
   ```bash
   npm run dev


### **Frontend Set Up**

1. Navigate to the client directory:
   ```bash
   cd client
2. Install dependencies:
   ```bash
   npm install
3. Create a .env file in the client directory with the following variable:
   ```bash
   VITE_API_URL=http://localhost:${backend_server_port}

3. Start the frontend server:
   ```bash
   npm run dev
   ```










