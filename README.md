HouseHunt - House Rental Web Application

📌 Project Overview

HouseHunt is a full-stack MERN (MongoDB, Express.js, React.js, Node.js) web application designed to facilitate house rentals. The platform supports three user roles: Renters, Owners, and Admins. It allows renters to browse and book properties, owners to list and manage their properties, and admins to oversee the entire system.

🏗️ Technologies Used

Frontend: React.js, Axios, Ant Design, Bootstrap, Moment.js

Backend: Node.js, Express.js, Mongoose

Database: MongoDB

Authentication: JWT (JSON Web Tokens)

Styling: CSS, Ant Design, Bootstrap

👥 User Roles

1. Renter

Sign up and log in

Browse and search for rental properties

Book properties and view booking history

2. Owner

Sign up and log in

List new properties

View and manage bookings made by renters

3. Admin

View and manage all user accounts

Approve or reject new property listings

Monitor all bookings and listings

📁 Folder Structure

House_Hunt/
├── backend/
│   ├── config/
│   │   └── connect.js
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   └── index.js
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   └── Navbar.jsx
│   │   ├── pages/
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   └── Dashboard.jsx
│   │   ├── App.js
│   │   ├── index.js
│   │   └── App.css
│   └── public/
└── package.json

🛠️ Step-by-Step Setup Guide

Step 1: Clone the Project

git clone https://github.com/your-username/househunt.git
cd House_Hunt

Step 2: Setup the Backend

cd backend
npm install

Ensure MongoDB is running on your machine (default port: 27017).

Then start the server:

npm start

Step 3: Setup the Frontend

cd ../frontend
npm install
npm start

Open http://localhost:3000 in your browser.

🗃️ MongoDB Collections

1. users

Fields: name, email, password, role (renter/owner/admin)

2. property

Fields: title, description, location, rent, ownerId, status (approved/pending)

3. booking

Fields: propertyId, renterId, startDate, endDate, status

🔒 Authentication Flow

Upon login, the server issues a JWT token.

The token is stored in the browser's local storage.

Protected routes validate the token before granting access.

🧪 Common Errors & Fixes

White Blank Screen: Check for missing return statements or unmatched JSX tags.

MongoDB Connection Error: Ensure mongod is running and reachable.

App.css not found: Ensure the file name matches exactly including case (e.g., App.css vs app.css).

Multiple export default: A file must only contain one default export.

🚧 Deployment Notes

Use npm run build in frontend to prepare a production build.

Serve the build folder using Node.js or any static file hosting service.
