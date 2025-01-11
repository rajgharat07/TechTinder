# TechTinder Frontend

TechTinder is a frontend application built using React and Vite to provide an intuitive and seamless user experience for developers seeking to connect and collaborate. This README provides a step-by-step guide on setting up the project, along with the key features implemented.

---

## Table of Contents
- [Features](#features)
- [Project Setup](#project-setup)
  - [Prerequisites](#prerequisites)
  - [Steps to Setup](#steps-to-setup)
- [Folder Structure](#folder-structure)
- [Routes](#routes)
- [State Management](#state-management)
- [Additional Features](#additional-features)
- [End-to-End Testing](#end-to-end-testing)

---

## Features
- Responsive UI with Tailwind CSS and Daisy UI
- User authentication (Login, Signup, Logout)
- Protected routes with redirection to login if the token is missing
- Profile management with edit functionality
- User feed with dynamic cards for potential connections
- Connection management (View connections, send requests, accept/reject requests)
- Redux Toolkit for global state management
- API integration using Axios with proper CORS handling
- Toast notifications for user actions
- End-to-end testing

---

## Project Setup

### Prerequisites
- Node.js (v14+)
- npm or yarn
- Chrome browser with Redux DevTools extension

### Steps to Setup

1. **Create a new Vite + React application**
   ```bash
   npm create vite@latest techtinder-frontend --template react
   cd techtinder-frontend

2. **Install dependencies**
   ```bash
   npm install
   npm install tailwindcss daisyui react-router-dom axios @reduxjs/toolkit react-redux

3. **Set up Tailwind CSS**
   Follow the official Tailwind CSS setup guide and add Daisy UI.
4. **Remove unnecessary boilerplate code**
   and create a simple "Hello World" app.
5. **Add Navbar Component**
   - Create a Navbar.jsx file inside the components folder.
   - Import and use the Navbar component in App.jsx.
6. **Set up React Router**
   - Install React Router DOM : 
   ```bash
   npm install react-router-dom 
   ```
   - Create a BrowserRouter and define routes : 
   ```jsx
   <BrowserRouter>
    <Routes>
        <Route path="/" element={<Body />}>
        <Route index element={<Feed />} />
        <Route path="/login" element={<Login />} />
        <Route path="/connections" element={<Connections />} />
        <Route path="/profile" element={<Profile />} />
        </Route>
    </Routes>
   </BrowserRouter>
    ```
    - Add an Outlet in the Body component.

7. **Create Footer Component** and add it to Body.jsx.
8. **Implement Authentication (Login, Signup, Logout)** 
9. **Set up Redux Toolkit** 
10. **Protect Routes** 
   - Redirect users to the login page if the token is not present.
11. **Implement Features**
   - User Feed: Build user cards dynamically and display them in the feed.
   - Profile Management: Allow users to edit their profile and save changes with a toast notification.
   - Connections: Display all connections and implement the ability to accept/reject requests.
   - Send Requests: Enable users to send or ignore connection requests directly from the feed.

## Routes

- / - Feed (Home)
- /login - Login Page
- /connections - Connections Page
- /profile - Profile Page

## State Management

- Redux Toolkit is used to manage global state.
- User authentication and feed data are stored in the Redux store.
- Redux DevTools can be used to debug the state changes.

## Additional Features

- Toast Notifications: Show toast messages for actions like saving profile changes or sending requests.
- Refactoring: Code is refactored to include a constants file and a components folder for better maintainability.

## End-to-End Testing

- End-to-end testing (E2E) is implemented to ensure the application works as expected from the user's perspective.