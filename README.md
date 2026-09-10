# Course Hub - Learning Management & Course Platform 🎓

<p align="left">
  <img src="https://img.shields.io/badge/LARAVEL-12.X-red?style=flat-square" alt="Laravel">
  <img src="https://img.shields.io/badge/PHP-8.3+-purple?style=flat-square" alt="PHP">
  <img src="https://img.shields.io/badge/BOOTSTRAP-5.3-purple?style=flat-square" alt="Bootstrap">
  <img src="https://img.shields.io/badge/MYSQL-DATABASE-blue?style=flat-square" alt="MySQL">
  <img src="https://img.shields.io/badge/VITE-BUNDLER-blueviolet?style=flat-square" alt="Vite">
</p>

Course Hub is a modern, responsive, and full-featured e-learning web application built with **Laravel 12**, **Blade**, and **Bootstrap 5**. It provides a comprehensive ecosystem tailored for three primary user roles: **Students**, **Instructors (Teachers)**, and **Administrators**.

---

## 📸 Screenshots & Application Showcase

<p align="center">
  <img src="screenshots/home-page.png" alt="Course Hub Home Page" width="100%">
</p>

---

## 🌟 Key Features & Capabilities

### 👨‍🎓 Student Experience
* **Course Discovery & Instant Enrollment**: Browse courses across various categories with detailed syllabi, instructor information, and one-click enrollment.
* **Dedicated Student Dashboard**:
  * Overview of enrolled courses with category badges and instructor tags.
  * Real-time overall progress calculation (`(completed lessons / total lessons) * 100`).
  * Quick-access "Continue Learning" actions.
* **Interactive Lesson Player**:
  * Immersive video player with course lesson outlines and navigation.
  * Lesson description, duration, and completion status.
* **Course Quizzes & Assessments**:
  * Take quizzes associated with enrolled courses.
  * Automated grading and instant percentage feedback upon submission.
* **Course Reviews & Ratings**:
  * Submit 5-star ratings and written feedback on enrolled courses.
  * Unique constraint per student per course to prevent duplicate ratings.
* **Profile Management**:
  * Update personal information (name, email, secure password changes).
  * Profile avatar upload and storage.

### 👨‍🏫 Instructor Workspace
* **Instructor Dashboard**:
  * Real-time metrics: Total created courses, total enrolled students, and dynamic aggregated average course rating.
  * Quick-manage list of all authored courses.
* **Course Management (Full CRUD)**:
  * Create, view, edit, and delete courses.
  * Upload course cover images stored safely in public storage.
  * Assign categories, set pricing, and write comprehensive descriptions.
* **Lesson Management**:
  * Add, update, and remove video lessons per course.
  * Configure video URLs, durations, and lesson notes.
  * Authorization guards ensure instructors only manage their own course lessons.
* **Student Enrollment Directory**:
  * Search enrolled students by name or email.
  * Filter enrolled students by specific course.
  * Optimized database queries using Eager Loading (`with('enrolledCourses')`).

### 🛡️ Administration & Control Center
* **System Dashboard**:
  * High-level platform analytics: Total students, instructors, courses, active enrollments, categories, and reviews.
  * Recent user registrations and latest published courses.
* **User Management**:
  * Complete user administration (create, update, view, and delete).
  * Role management: easily assign or switch user roles (`admin`, `teacher`, `student`).
* **Category Management**:
  * Create and manage course categories with custom icons and image uploads.
  * Course count tracking per category.
* **Global Course & Content Oversight**:
  * Moderate courses across all instructors.
* **Review Moderation**:
  * Monitor student feedback and remove inappropriate ratings or comments.

<p align="center">
  <img src="screenshots/admin-dashboard-overview.png" alt="Course Hub Admin Dashboard" width="100%">
</p>

---

## 🎨 Design, UI & UX Highlights
* **Dark & Light Mode**: Seamless theme switching with instantaneous persistence via `localStorage`.
* **Fully Responsive Design**: Optimized layout across mobile, tablet, and wide desktop screens.
* **Dynamic Landing Page**:
  * Eye-catching Hero section with quick call-to-actions.
  * Dynamic KPI statistics counter (live counts of students, courses, and teachers).
  * Featured courses carousel/grid.
  * Top categories showcase.
  * Student testimonials and newsletter subscription banner.
* **Modern Typography & Icons**: Integrated with FontAwesome 6, Bootstrap Icons, and clean CSS variables.

<p align="center">
  <img src="screenshots/course-details-reviews.png" alt="Course Hub Course Details" width="100%">
</p>

---

## 🔒 Security & Architecture
* **Role-Based Access Control (RBAC)**: Protected via custom `admin` middleware and controller authorization checks.
* **Anti-Tampering Safeguards**: Instructors are prevented from submitting reviews on their own courses.
* **Optimized Queries**: Leverages Laravel Eloquent relationships (`belongsTo`, `hasMany`, `belongsToMany`) with `withCount` and `withAvg` to eliminate N+1 query bottlenecks.
* **Secure File Handling**: Image uploads use Laravel Storage Disks with automated cleanup on deletion.
* **CSRF & XSS Protection**: Standard Laravel security tokens on all POST/PUT/DELETE forms.

---

## 🛠️ Technology Stack

| Component | Technology |
| :--- | :--- |
| **Backend Framework** | Laravel 12.x |
| **Language** | PHP 8.3+ |
| **Frontend Engine** | Laravel Blade Templates |
| **CSS Framework** | Bootstrap 5.3 |
| **Icons** | Font Awesome 6 & Bootstrap Icons |
| **Build Tool** | Vite |
| **Database** | MySQL / MariaDB (or SQLite) |
| **Authentication** | Laravel UI |

---

## 🚀 Installation & Setup Guide

### Prerequisites
Make sure you have the following installed on your machine:
* **PHP >= 8.2** with PDO, OpenSSL, Mbstring, and cURL extensions.
* **Composer**
* **Node.js & NPM**
* **MySQL** (e.g., via XAMPP)

### 1. Clone the Repository
```bash
git clone [https://github.com/Mariam-Mohamed5/courses-platform.git](https://github.com/Mariam-Mohamed5/courses-platform.git)
cd courses-platform
