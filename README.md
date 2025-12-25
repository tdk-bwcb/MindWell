# 🧠 MindWell — Mental Health & Wellness Platform

**MindWell** is a professional full-stack mental wellness platform designed to support users through secure authentication, personalized experiences, and scalable backend services. The system emphasizes performance, security, and clean architecture.

---

## 🚀 Key Features

- 🔐 **Secure Authentication**
  - JWT-based authentication with refresh tokens  
  - HTTP-only cookies for XSS mitigation  
  - Role-based access control (RBAC)  

- 📩 **Email & Notification System**
  - OTP-based verification for account security  
  - Automated email workflows using Nodemailer  
  - Non-blocking email pipelines ensuring zero latency impact

- 🧠 **Mental Health Support Modules**
  - User questionnaires and data collection  
  - Appointment scheduling system  
  - Scalable backend design to handle growing user data  

- 🖼️ **Media Handling**
  - Cloudinary integration for secure image uploads  
  - Optimized image delivery via CDN with asynchronous processing  

- ⚡ **Performance Optimizations**
  - Lazy-loaded React components to reduce bundle size  
  - Type-safe frontend using TypeScript Generics  
  - Clean MVC (Model-View-Controller) backend architecture  

---

## 🏗️ Technical Architecture & Design



### Backend Excellence
The backend is architected as a **Scalable REST API** using Node.js and Express. It follows the **MVC Pattern** to separate concerns:
* **Models:** Strict data modeling with Mongoose.
* **Controllers:** Business logic isolation for easier testing.
* **Middleware:** Centralized error handling and security layers.

### Security Implementation
* **Stateless JWT & Refresh Tokens:** Implemented a rotating refresh token strategy to prevent unauthorized access.
* **Cookie-based Storage:** Storing tokens in `HTTP-only` and `Secure` cookies to eliminate client-side script access (XSS).
* **Bcrypt.js:** Industry-standard password hashing for user data protection.

---

## 🛠️ Tech Stack

| Layer | Technology |
|------|------------|
| **Frontend** | React.js, TypeScript, Vite, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (NoSQL) |
| **Authentication** | JWT (Stateless), HTTP-only Cookies |
| **Media & Email** | Cloudinary (CDN), Nodemailer |

---

## ⚙️ Installation & Setup

Follow these steps to get the project running locally:

```bash
# 1. Clone the repository
git clone [https://github.com/yourusername/mindwell.git](https://github.com/yourusername/mindwell.git)
cd mindwell

# 2. Setup Environment Variables
# Create a .env file in the root directory and add:
# PORT=5000
# MONGO_URI=your_mongodb_connection_string
# JWT_SECRET=your_jwt_secret
# CLOUDINARY_URL=your_cloudinary_url
# EMAIL_USER=your_email
# EMAIL_PASS=your_app_password

# 3. Install Dependencies
# Install Backend
cd backend && npm install
# Install Frontend
cd ../frontend && npm install

# 4. Run the Application
# Start backend (from backend folder)
npm run dev
# Start frontend (from frontend folder)
npm run dev
