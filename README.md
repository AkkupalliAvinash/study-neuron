# StudyNeuron 2.0 - Online Learning Platform

> A comprehensive full-stack web application for online course management and learning, built with modern technologies and best practices.

---

## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Project Architecture](#project-architecture)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Environment Configuration](#environment-configuration)
- [Database Schema](#database-schema)

---

## 📖 Project Overview

**StudyNeuron 2.0** is a complete learning management system (LMS) that enables educators to create and manage courses while students can enroll, learn, and track their progress. The platform includes features for course management, user authentication, payment processing, and interactive learning experiences.

### Core Purpose
- Create an accessible platform for online education
- Enable educators to share knowledge effectively
- Provide students with structured learning paths
- Facilitate course discovery and enrollment
- Track student progress and performance

---

## ✨ Key Features

### For Students
- **User Authentication**: Secure signup, login, and email verification with OTP
- **Course Discovery**: Browse and search courses by categories
- **Course Enrollment**: Seamless enrollment with payment integration (Razorpay)
- **Learning Progress Tracking**: Monitor course completion and section progress
- **Interactive Ratings & Reviews**: Rate courses and read reviews from other students
- **Course Materials**: Access lectures (videos), supplementary materials, and course notes
- **Responsive Dashboard**: View enrolled courses and personalized recommendations

### For Instructors
- **Course Creation**: Comprehensive course builder with multiple sections and subsections
- **Content Management**: Upload videos and course materials
- **Student Management**: Track enrolled students and their progress
- **Performance Analytics**: View course statistics and student engagement
- **Ratings & Feedback**: Monitor student reviews and ratings

### General Features
- **Email Notifications**: Automatic emails for OTP, enrollment, and payment confirmations
- **Payment Processing**: Secure payment gateway integration with Razorpay
- **Contact Management**: Contact form for inquiries and support
- **Responsive Design**: Mobile-friendly interface using Tailwind CSS
- **File Upload**: Cloud-based file storage with Cloudinary

---

## 🛠️ Technology Stack

### Frontend
| Technology | Purpose |
|---|---|
| **React 18** | UI library for building user interfaces |
| **Redux Toolkit** | State management |
| **React Router v6** | Client-side routing |
| **Tailwind CSS** | Utility-first CSS framework |
| **Axios** | HTTP client for API calls |
| **React Hook Form** | Form state management |
| **React Icons** | Icon library |
| **Chart.js** | Data visualization for analytics |
| **Swiper** | Touch slider carousel |

### Backend
| Technology | Purpose |
|---|---|
| **Node.js** | JavaScript runtime |
| **Express.js** | Web framework |
| **MongoDB** | NoSQL database |
| **Mongoose** | ODM (Object Document Mapper) |
| **JWT** | Authentication tokens |
| **Bcrypt** | Password hashing |
| **Nodemailer** | Email sending service |
| **Razorpay** | Payment gateway |
| **Cloudinary** | Cloud image/file storage |

### Development Tools
| Tool | Purpose |
|---|---|
| **Nodemon** | Development server auto-reload |
| **Dotenv** | Environment variable management |
| **Cookie Parser** | Cookie handling middleware |
| **CORS** | Cross-Origin Resource Sharing |
| **Express Fileupload** | File upload handling |

---

## 🏗️ Project Architecture

```
StudyNeuron2.0/
├── Client (Frontend - React)
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Page components
│   │   ├── services/        # API integration
│   │   ├── slices/          # Redux slices
│   │   ├── utils/           # Helper functions
│   │   └── hooks/           # Custom React hooks
│   └── public/              # Static files
│
└── Server (Backend - Express.js)
    ├── routes/              # API endpoints
    ├── controllers/         # Business logic
    ├── models/              # Database schemas
    ├── middleware/          # Express middleware
    ├── config/              # Configuration files
    ├── mail/                # Email templates
    └── utils/               # Utility functions
```

---

## 📋 Prerequisites

Before setting up the project, ensure you have the following installed:

- **Node.js** (v14 or higher) - [Download](https://nodejs.org/)
- **npm** or **yarn** - Package manager
- **MongoDB** - Database (local or Atlas cloud)
- **Git** - Version control

### Required Accounts & APIs
- **MongoDB Atlas** - Cloud database
- **Cloudinary** - Image/file hosting
- **Razorpay** - Payment gateway
- **Email Service** - SMTP credentials (Gmail, SendGrid, etc.)

---

## 🚀 Installation & Setup

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd StudyNeuron2.0-main
```

### Step 2: Frontend Setup
```bash
# Install frontend dependencies
npm install

# Create .env file in root directory
touch .env
```

Configure frontend `.env`:
```env
REACT_APP_BASE_URL=http://localhost:4000/api/v1
```

### Step 3: Backend Setup
```bash
# Navigate to server directory
cd server

# Install backend dependencies
npm install

# Create .env file in server directory
touch .env
```

Configure backend `.env`:
```env
PORT=4000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
MAIL_HOST=your_smtp_host
MAIL_USER=your_email
MAIL_PASS=your_email_password
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
```

---

## ▶️ Running the Application

### Development Mode

**Terminal 1 - Backend Server:**
```bash
cd server
npm run dev
# Server runs on http://localhost:4000
```

**Terminal 2 - Frontend Development Server:**
```bash
npm start
# Client runs on http://localhost:3000
```

### Production Build

**Frontend:**
```bash
npm run build
# Creates optimized production build
```

**Backend:**
```bash
cd server
npm start
```

---

## 📁 Project Structure

### Backend Controllers
| Controller | Functionality |
|---|---|
| **Auth.js** | User registration, login, OTP verification |
| **Course.js** | Course CRUD operations |
| **Section.js** | Course sections management |
| **Subsection.js** | Subsection/lesson management |
| **Category.js** | Course categories |
| **RatingandReview.js** | Student reviews and ratings |
| **courseProgress.js** | Track student progress |
| **Payments.js** | Payment processing (Razorpay) |
| **Profile.js** | User profile management |
| **ContactUs.js** | Contact form submissions |

### Backend Models
| Model | Description |
|---|---|
| **User** | User credentials and information |
| **Course** | Course details and metadata |
| **Section** | Course sections |
| **Subsection** | Lessons within sections |
| **Profile** | Extended user profile data |
| **OTP** | One-time passwords for verification |
| **Category** | Course categories |
| **RatingandReview** | Student reviews |
| **CourseProgress** | Student progress tracking |

### Frontend Components
| Folder | Components |
|---|---|
| **Auth** | Login, Signup, Verification flows |
| **HomePage** | Landing page sections |
| **Catalog** | Course browsing and search |
| **Course** | Course cards and displays |
| **Dashboard** | Student/instructor dashboard |
| **ViewCourse** | Course content viewer |
| **Common** | Shared components (Navbar, Footer, etc.) |

---

## 🔌 API Endpoints

### Authentication Routes
```
POST   /api/v1/auth/signup           - User registration
POST   /api/v1/auth/login            - User login
POST   /api/v1/auth/sendotp          - Send OTP for verification
POST   /api/v1/auth/verify-otp       - Verify OTP
POST   /api/v1/auth/change-password  - Change password
POST   /api/v1/auth/reset-password   - Reset forgotten password
```

### Course Routes
```
GET    /api/v1/course/get-all-courses      - Get all courses
GET    /api/v1/course/get-course/:id       - Get course details
POST   /api/v1/course/create-course        - Create new course
PUT    /api/v1/course/edit-course/:id      - Update course
DELETE /api/v1/course/delete-course/:id    - Delete course
POST   /api/v1/course/add-section          - Add section to course
```

### Payment Routes
```
POST   /api/v1/payment/capture-payment     - Process payment
POST   /api/v1/payment/verify-signature    - Verify payment
GET    /api/v1/payment/enrolled-courses    - Get enrolled courses
```

### Profile Routes
```
GET    /api/v1/profile/get-user-details    - Get user profile
PUT    /api/v1/profile/update-profile      - Update profile
POST   /api/v1/profile/update-password     - Change password
DELETE /api/v1/profile/delete-account      - Delete account
```

### Contact Routes
```
POST   /api/v1/reach/contact-us            - Submit contact form
```

---

## 🔐 Environment Configuration

### Required Environment Variables

| Variable | Description | Example |
|---|---|---|
| `MONGODB_URL` | MongoDB connection string | `mongodb+srv://user:pass@cluster.mongodb.net/db` |
| `JWT_SECRET` | JWT token secret key | `your_secret_key_here` |
| `PORT` | Server port | `4000` |
| `CLOUDINARY_NAME` | Cloudinary account name | `your_account` |
| `CLOUDINARY_API_KEY` | Cloudinary API key | `123456789` |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret | `secret_key` |
| `MAIL_HOST` | SMTP host | `smtp.gmail.com` |
| `MAIL_USER` | Email address | `your_email@gmail.com` |
| `MAIL_PASS` | Email password | `app_password` |
| `RAZORPAY_KEY_ID` | Razorpay key ID | `key_123456` |
| `RAZORPAY_KEY_SECRET` | Razorpay secret | `secret_123456` |

---

## 💾 Database Schema

### User Model
```javascript
{
  firstName, lastName, email, password,
  accountType, contactNumber, about,
  profileImage, courseProgress, courses
}
```

### Course Model
```javascript
{
  courseName, courseDescription, instructor,
  whatYouWillLearn, courseContent (sections),
  ratingAndReviews, price, thumbnail,
  category, createdAt, updatedAt
}
```

### Profile Model
```javascript
{
  userId, gender, dateOfBirth, about,
  contactNumber, country, state, city
}
```

---









