# 🚀 CodePulse - Personalized Coding Progress Tracker

<div align="center">

</div>

<br />



<br />

CodePulse Tracker is a dynamic, personalized study planner designed to help developers and students master coding problems for interviews and skill-building. It generates a tailored, day-by-day study schedule based on your skill level, desired timeline, and specific topics of interest. Track your progress, take detailed notes, and stay on top of your goals with an intuitive and feature-rich interface.
- **[Live Demo](https://codepulsetracker.vercel.app/authentication)** - Try the application
---
![screencapture-codepulse-progress-tracker-vercel-app-track-2025-06-08-11_58_50](https://github.com/user-attachments/assets/3846cfe1-b676-45cb-9523-ce3f40a9073f)
![screencapture-codepulse-progress-tracker-vercel-app-track-2025-06-08-12_03_58](https://github.com/user-attachments/assets/9dc40810-3192-4f3d-a7b5-bd911167b1dd)
![screencapture-codepulse-progress-tracker-vercel-app-track-2025-06-08-12_05_37](https://github.com/user-attachments/assets/849e9b68-81ff-4c20-93fe-86db0a704695)

---

## ✨ Key Features

This application is packed with features to provide a comprehensive and personalized study experience.

#### 🧠 Plan Generation & Customization
* **Personalized Study Plan:** Generates a unique study plan based on your self-assessed skill level (Beginner, Intermediate, Pro), the duration you want to study for, and the topics you want to focus on.
* **🎯 Topic Selection:** Choose from a wide range of essential topics like Arrays, Graphs, Dynamic Programming, and more. Or leave it blank for a well-rounded, comprehensive curriculum.
* **🗓️ Flexible Duration:** Select a preset duration (e.g., 2 Weeks, 1 Month) or input a custom number of days for your study plan.
* **➕ Add Custom Problems:** Easily add your own problems to the schedule, complete with a name, difficulty, topic, and a link to the problem statement.

#### 📊 Productivity & Tracking
* **Interactive Dashboard:** Visualize your progress at a glance. The dashboard features stats on total problems, completed tasks, overall completion percentage, and a progress bar.
* **🔔 Spaced Repetition:** When you complete a problem, the app automatically schedules it for review at increasing intervals to reinforce learning. The dashboard shows how many problems are due for review.
* **📋 Daily Task Manager:** View your problems organized by day. Each day is marked as 'Past', 'Today', or 'Future' with clear visual cues.
* **✅ Progress Tracking:** Mark problems as complete with a single click. The UI updates instantly, striking through the problem name and updating your daily and overall progress.

#### 📝 Enhanced Note-Taking
* **Rich Text Notes:** For every problem, you can add, view, and edit detailed notes with an editor designed for technical documentation.
* **💻 Built-in Code Blocks:** Directly embed code snippets into your notes with syntax highlighting. A toolbar allows you to insert code blocks for various languages (JavaScript, Python, Java, C++).
* **🚀 Note Templates:** Speed up your note-taking with pre-defined templates for `Approach`, `Complexity Analysis`, and `Edge Cases`.
* **🔗 External Links:** Each problem card includes a direct link to its LeetCode page or a custom URL for quick access.

#### 🎨 User Experience
* **🌗 Dark & Light Mode:** Toggle between a sleek dark mode and a clean light mode. Your preference is saved in your browser for a consistent experience.
* **📱 Fully Responsive Design:** The interface is optimized for all screen sizes, from mobile phones to desktops.
* **👤 User Authentication:** A simple and clean authentication page to manage user sessions, with the header displaying the logged-in user's profile.
* **💡 Intuitive UI:** Built with modern design principles and helpful icons from `lucide-react` to make navigation feel natural.
* **🔒 Guided Setup:** A user-friendly modal prevents navigation to the dashboard or tasks before a study plan is generated, guiding the user through the setup process.

---

## 🛠️ Tech Stack

This project is built using a modern and efficient frontend stack.

| Category          | Technology                                                                                                  |
| ----------------- | ----------------------------------------------------------------------------------------------------------- |
| **Core Framework** | [**React.js**](https://reactjs.org/)                                                                        |
| **Styling** | [**Tailwind CSS**](https://tailwindcss.com/)                                                                |
| **Icons** | [**Lucide React**](https://lucide.dev/)                                                                     |
| **Language** | **JavaScript (ES6+)** |
| **State Management**| **React Hooks** (`useState`, `useEffect`)                                                                 |
| **Data Source** | Local `problems.json`                                                                                       |
| **Persistence** | `localStorage` API                                                                                          |

---

## 📂 Project Structure

The project is organized into modular components for better maintainability and readability.

| Path                  | Description                                                                 |
| --------------------- | --------------------------------------------------------------------------- |
| `src/`                | Main source directory.                                                      |
| `src/components/`     | Contains all reusable React components.                                     |
| `src/data/`           | Holds the `problems.json` data file.                                        |
| `src/App.js`          | Main application component, handles routing and high-level layout.          |
| `src/StudyPlanner.js` | The core component that manages all application state, logic, and views.    |
| `src/index.js`        | The entry point of the React application.                                   |


---
# Backend API Documentation

This document outlines the backend API endpoints tested via Postman, providing details on each request and its expected response.

## 1. User Authentication

### 1.1. User Signup

This endpoint allows new users to register an account.

**Endpoint:** `/api/auth/signup`  
**Method:** `POST`

**Request Body (JSON):**
```json
{
  "name": "Prakhar Sinha",
  "email": "workspace.prakhar@gmail.com",
  "password": "password123"
}
```

**Response Body (JSON):**
```json
{
  "jwt": "g6h17uwu5sTXEPbBACCKWv3IKIawvCPLK16Na2iczQ",
  "user": {
    "id": 1,
    "name": "Prakhar Sinha"
  }
}
```
![signup](https://github.com/user-attachments/assets/19f0da5a-33b1-46d3-aa8b-c6fbc7d2a29f)

**Status Code:** `201 Created`

**Description:** Creates a new user account. Returns a JWT (JSON Web Token) for authentication and basic user information upon successful registration.


### 1.2. User Login

This endpoint allows existing users to log in and obtain an authentication token.

**Endpoint:** `/api/auth/login`  
**Method:** `POST`

**Request Body (JSON):**
```json
{
  "email": "workspace.prakhar@gmail.com",
  "password": "password123"
}
```

**Response Body (JSON):**
```json
{
  "jwt": "eyJhbGciIoiJIUzI1NiJ9.eyJzdWllbJo3b3JjczBhY2hJha2hhnhkBNBWFPbc5jb2llcJIc2vySwQIQjESImlndCI6MTc0OTM3Mjc4NIzwIxhjoxNzQ5NDU5MTg2fQ.ZXJhaKunlJAUie0hvggSlbx9vbb9uPaUicYyxNVPHVpU",
  "user": {
    "id": 1,
    "name": "Prakhar Sinha",
    "email": "workspace.prakhar@gmail.com",
    "avatarUrl": "https://ui-avatars.com/api/?name=Prakhar+Sinha&background=3b82f6&color=ffffff"
  }
}
```
![login](https://github.com/user-attachments/assets/cd6409a3-6376-4e62-9122-7bef461bdb7d)

**Status Code:** `200 OK`

**Description:** Authenticates a user with provided credentials. Returns a JWT and user details on successful login. This JWT should be used in subsequent authenticated requests (e.g., in the Authorization header).

## 2. Problem Management

### 2.1. Generate Study Plan

This endpoint generates a study plan based on specified criteria.

**Endpoint:** `/api/study-plan`  
**Method:** `POST`

**Request Body (JSON):**
```json
{
  "level": "beginner",
  "days": 14,
  "topics": ["Array", "String"]
}
```

**Response Body (JSON):**
```json
[
  {
    "day": 1,
    "date": "Sun, Jun 08, 25",
    "problems": [
      {
        "id": 54,
        "name": "3Sum",
        "difficulty": "Medium",
        "topic": "Array"
      }
    ]
  }
  
]
```
![studyplan](https://github.com/user-attachments/assets/b716a49d-d46c-437c-9ff4-81e36c5527c3)

**Status Code:** `200 OK`

**Description:** Creates a study plan tailored to the user's selected level, duration, and topics. The response includes a list of days, each with a date and a list of problems to be solved on that day.

### 2.2. Add Custom Problem

This endpoint allows users to add their own custom problems to their list.

**Endpoint:** `/api/problems/custom`  
**Method:** `POST`

**Request Body (JSON):**
```json
{
  "name": "Two Sum",
  "topic": "Arrays",
  "difficulty": "Easy",
  "leetcodeId": "1",
  "customLink": "https://leetcode.com/problems/two-sum/"
}
```

**Response Body (JSON):**
```json
{
  "id": 191,
  "name": "Two Sum",
  "topic": "Arrays",
  "difficulty": "Easy",
  "status": "pending",
  "leetcodeId": "1",
  "customLink": "https://leetcode.com/problems/two-sum/",
  "custom": true
}
```
![add custom problem](https://github.com/user-attachments/assets/5c9a4212-ceaf-43dc-b4d1-6a166388e1be)

**Status Code:** `200 OK`

**Description:** Adds a new custom problem entry for the authenticated user. The problem is initially set to "pending" status.

### 2.3. Toggle Problem Status

This endpoint updates the status of a specific problem.

**Endpoint:** `/api/problems/{id}/status`  
**Method:** `PATCH`

**Path Parameter:**  
`id`: The ID of the problem to update (e.g., 6 in `/api/problems/6/status`).

**Request Body (JSON):**
```json
{
  "status": "completed"
}
```

**Response Body (JSON):**
```json
{
  "id": 6,
  "name": "Maximum Subarray",
  "difficulty": "Easy",
  "topic": "Array",
  "status": "completed",
  "leetcodeId": "53",
  "customLink": null,
  "notes": null,
  "custom": false
}
```
![toggle problem status](https://github.com/user-attachments/assets/50ad12d4-edbd-47a9-b15b-eb81b3409fbc)
**Status Code:** `200 OK`

**Description:** Toggles or updates the status of a problem (e.g., from "pending" to "completed"). The response reflects the updated problem details.

### 2.4. Get Dashboard Statistics

This endpoint retrieves overall statistics for the user's problem-solving progress.

**Endpoint:** `/api/problems/dashboard-stats`  
**Method:** `GET`

**Request Body:** None

**Response Body (JSON):**
```json
{
  "total": 34,
  "completed": 0,
  "percentage": 0,
  "easy": {
    "total": 18,
    "completed": 0,
    "percentage": 0
  },
  "medium": {
    "total": 12,
    "completed": 0,
    "percentage": 0
  },
  "hard": {
    "total": 4,
    "completed": 0,
    "percentage": 0
  }
}
```
![getdashboard stats](https://github.com/user-attachments/assets/1ee0bf47-e79b-44d9-a403-5447f0eeedf0)

**Status Code:** `200 OK`

**Description:** Provides an overview of problems, including total problems, completed problems, and completion percentages, broken down by difficulty level.

---


## ✍️ Author

**Prakhar Sinha**

* **GitHub:** [@prakhar3125](https://github.com/prakhar3125)
* **LinkedIn:** [Prakhar Sinha](https://www.linkedin.com/in/prakhar3125/)
