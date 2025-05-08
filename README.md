# HIRRD

## Table of Contents

* [Introduction](#introduction)
* [Features](#features)
* [Technology Stack](#technology-stack)
* [Installation](#installation)
* [Folder Structure](#folder-structure)
* [API Documentation](#api-documentation)
* [Frontend Details](#frontend-details)
* [Backend Details](#backend-details)
* [Database Schema](#database-schema)
* [Testing](#testing)
* [Deployment](#deployment)
* [Future Enhancements](#future-enhancements)
* [Contributing](#contributing)

---

## Introduction

The Full Stack Job Portal is a web application built using modern tools and technologies to connect job seekers and employers. It features a robust and user-friendly interface and offers seamless interaction for job postings, applications, and profile management. This project leverages **React.js**, **Tailwind CSS**, **Supabase**, **Clerk**, and **Shadcn UI** to provide an elegant, scalable, and feature-rich solution.

---

## Features

### For Job Seekers:

* **User Registration and Authentication** with Clerk
* **Search and Filter Jobs** by title, location, or keywords
* **Apply for Jobs** with a single click
* **Save Favorite Jobs** for later
* **Profile Management** (upload resumes, add skills, etc.)

### For Employers:

* **Employer Signup and Login**
* **Post Job Listings** with rich descriptions
* **Manage Applications**
* **Search for Candidates** using filters like skills and experience

### General Features:

* **Responsive Design** using Tailwind CSS
* **Role-Based Access Control** (Admin, Job Seeker, Employer)
* **Real-Time Notifications** for job applications and updates
* **Modern UI/UX** with Shadcn UI components

---

## Technology Stack

### Frontend:

* **React.js** for building interactive UIs
* **Tailwind CSS** for responsive and customizable design
* **Shadcn UI** for modern UI components
* **Clerk** for authentication and user management

### Backend:

* **Supabase** for database and authentication services
* **Node.js** for server-side logic (if needed for custom APIs)



---

## Installation

### Prerequisites:

* Node.js
* Supabase Account
* Clerk Account


### Steps:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/fullstack-job-portal.git
   cd fullstack-job-portal
   ```

2. **Install Dependencies:**

   ```bash
   npm install
   ```

3. **Set Environment Variables:**
   Create a `.env` file in the root directory with the following:

   ```env
   REACT_APP_SUPABASE_URL=<your-supabase-url>
   REACT_APP_SUPABASE_ANON_KEY=<your-supabase-anon-key>
   REACT_APP_CLERK_FRONTEND_API=<your-clerk-frontend-api>
   ```

4. **Start the Application:**

   ```bash
   npm start
   ```

5. **Access the Application:**
   Open your browser and navigate to `http://localhost:3000`.

---

## Folder Structure

```
fullstack-job-portal/
  |-- src/
  |   |-- components/
  |   |-- pages/
  |   |-- hooks/
  |   |-- utils/
  |   |-- App.js
  |-- public/
  |-- .env
  |-- package.json
```

---



## Frontend Details

* Built with **React.js** for dynamic and modular development.
* **Shadcn UI** components ensure a modern, cohesive design.
* **Tailwind CSS** simplifies styling and responsiveness.
* **React Query** efficiently handles data fetching and caching.

### Key Pages:

1. **Home Page:** Displays featured jobs and search functionality.
2. **Job Details Page:** Provides comprehensive job information and an "Apply Now" button.
3. **Profile Page:** Allows users to manage their details, upload resumes, and track applications.
4. **Employer Dashboard:** Enables employers to post and manage jobs.

---

## Backend Details

### Supabase:

* Used as the primary database and authentication provider.
* Implements role-based access control and server-side operations for security.

### Key Tables:

* **Users:** Stores user information and roles.
* **Jobs:** Stores job postings.
* **Applications:** Tracks job applications.

### Custom Backend (Optional):

If additional functionality is needed, a custom backend with **Node.js** and **Express.js** can be implemented.

---

## Database Schema

### Users:

```json
{
  "id": "uuid",
  "name": "string",
  "email": "string",
  "role": "string", // 'job_seeker' or 'employer'
  "profile": {
    "resume_url": "string",
    "skills": ["string"]
  }
}
```

### Jobs:

```json
{
  "id": "uuid",
  "title": "string",
  "description": "string",
  "company": "string",
  "location": "string",
  "posted_by": "uuid",
  "created_at": "timestamp"
}
```

### Applications:

```json
{
  "id": "uuid",
  "job_id": "uuid",
  "user_id": "uuid",
  "applied_at": "timestamp"
}
```

---

## Testing

* **Frontend:** Tested with **Jest** and **React Testing Library**.
* **Database:** Query testing using Supabase SQL interface.

---


## Contributing

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:

   ```bash
   git commit -m "Add feature-name"
   ```
4. Push to the branch:

   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---


