<div align="center">
<img src="https://img.icons8.com/fluency/96/home--v1.png" alt="HouseHunt Logo" width="96"/>
  
#  HouseHunt — Finding Your Perfect Rental Home
 
**A modern full-stack web application to search, list, and discover rental properties with ease.**
 
[![JavaScript](https://img.shields.io/badge/JavaScript-92%25-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CSS](https://img.shields.io/badge/CSS-7.4%25-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![HTML](https://img.shields.io/badge/HTML-0.4%25-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home?style=for-the-badge&color=yellow)](https://github.com/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home/stargazers)
 
[ Documentation](#table-of-contents) &nbsp;•&nbsp; [🐛 Report Bug](https://github.com/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home/issues) &nbsp;•&nbsp; [ Request Feature](https://github.com/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home/issues)
 
</div>
---
 
##  Table of Contents
 
- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Screenshots](#screenshots)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
---
 
##  About the Project
 
**HouseHunt** is a full-stack rental home finder platform designed to bridge the gap between property owners and tenants. Whether you're a landlord looking to list your property or a tenant searching for your next home, HouseHunt provides a seamless, intuitive experience.
 
>  **Goal:** Make the rental home search process simple, fast, and transparent.
 
---
 
##  Features
 
-  **3-Role System** — Separate flows for Admin, Property Owners, and Tenants
-  **Auth System** — Register, Login, Forgot Password with JWT & bcryptjs
-  **Property Management** — Owners can add, update, delete, and view their listings
-  **Image Uploads** — Property photos uploaded via Multer
-  **Booking System** — Tenants book properties; Owners approve or reject
-  **Admin Panel** — Admins manage users, grant/revoke Owner access, view all data
-  **Protected Routes** — JWT middleware guards all sensitive endpoints
-  **Availability Tracking** — Property status auto-updates on booking approval
-  **Responsive Design** — Optimized for mobile, tablet, and desktop
---
 
##  Tech Stack
 
### Frontend
| Technology | Purpose |
|---|---|
| React.js | UI Component Library |
| CSS3 | Styling & Responsive Design |
| Axios | HTTP Client for API calls |
 
### Backend
| Technology | Purpose |
|---|---|
| Node.js | Runtime Environment |
| Express.js | Web Framework |
| MongoDB | NoSQL Database |
| Mongoose | ODM for MongoDB |
| JWT (jsonwebtoken) | Authentication tokens |
| bcryptjs | Password hashing |
| Multer | Property image uploads |
| dotenv | Environment variable management |
| cors | Cross-Origin Resource Sharing |
| nodemon | Auto-restart during development |
 
---
 
##  Project Structure
 
```
HouseHunt-Finding-Your-Perfect-Rental-Home/
│
├──  frontend/                # React frontend application
│   ├── public/                 # Static assets
│   └── src/
│       ├── components/         # Reusable UI components
│       ├── pages/              # Page-level components
│       ├── services/           # API service calls
│       └── App.js              # Root component
│
├──  backend/                 # Node.js + Express backend
│   ├── controllers/            # Route handlers
│   ├── models/                 # Mongoose data models
│   ├── routes/                 # API routes
│   ├── middleware/             # Auth & error handling middleware
│   └── server.js              # Server entry point
│
├──  ProjectDocumentation/    # Project docs and references
│
└── README.md
```
 
---
 
##  Getting Started
 
### Prerequisites
 
Make sure you have the following installed:
 
- [Node.js](https://nodejs.org/) (v16 or above)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) (local or [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))
### Installation
 
1. **Clone the repository**
```bash
git clone https://github.com/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home.git
cd HouseHunt-Finding-Your-Perfect-Rental-Home
```
 
2. **Install Backend Dependencies**
```bash
cd backend
npm install
```
 
3. **Install Frontend Dependencies**
```bash
cd ../frontend
npm install
```
 
4. **Set up Environment Variables**
Create a `.env` file in the `backend/` folder:
 
```env
PORT=8001
MONGO_DB=your_mongodb_connection_string
JWT_KEY=your_jwt_secret_key
```
 
### Running the App
 
**Start the Backend Server**
 
```bash
cd backend
npm start
```
 
**Start the Frontend (in a new terminal)**
 
```bash
cd frontend
npm start
```
 
The app will be live at `http://localhost:3000` 🎉
 
---
 
##  Screenshots
 

 
| Home Page | Property Listing | Search Results |
|---|---|---|
| _(<img width="1895" height="915" alt="Screenshot 2026-04-26 133010" src="https://github.com/user-attachments/assets/9a5975d8-997c-4033-8fcb-b6a3d2500029" />
)_ | _(<img width="1898" height="912" alt="Screenshot 2026-04-26 133056" src="https://github.com/user-attachments/assets/e489ec26-963c-4d96-8d61-bae619933052" />
)_ | _(<img width="1919" height="915" alt="Screenshot 2026-04-26 133108" src="https://github.com/user-attachments/assets/6a64f478-3c29-4dc5-b2b3-48ab14bb0464" />
)_ |
 
---
 
##  API Endpoints
 
###  User Routes (`/api/user`)
| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `POST` | `/api/user/register` | ❌ | Register as Tenant or Owner |
| `POST` | `/api/user/login` | ❌ | Login and receive JWT token |
| `POST` | `/api/user/forgotpassword` | ❌ | Reset account password |
| `POST` | `/api/user/getuserdata` | ✅ | Get logged-in user profile |
| `GET` | `/api/user/getAllProperties` | ❌ | Fetch all available listings |
| `POST` | `/api/user/bookinghandle/:propertyid` | ✅ | Book a property |
| `GET` | `/api/user/getallbookings` | ✅ | Get tenant's own bookings |
 
###  Owner Routes (`/api/owner`)
| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `POST` | `/api/owner/postproperty` | ✅ | Add a new property listing |
| `GET` | `/api/owner/getallproperties` | ✅ | Get owner's own properties |
| `PATCH` | `/api/owner/updateproperty/:propertyid` | ✅ | Update a property |
| `DELETE` | `/api/owner/deleteproperty/:propertyid` | ✅ | Delete a property |
| `GET` | `/api/owner/getallbookings` | ✅ | View bookings for owner's properties |
| `POST` | `/api/owner/handlebookingstatus` | ✅ | Approve or reject a booking |
 
###  Admin Routes (`/api/admin`)
| Method | Endpoint | Auth | Description |
|--------|----------|------|-------------|
| `GET` | `/api/admin/getallusers` | ✅ | Get all registered users |
| `POST` | `/api/admin/handlestatus` | ✅ | Grant/revoke Owner access |
| `GET` | `/api/admin/getallproperties` | ✅ | View all properties platform-wide |
| `GET` | `/api/admin/getallbookings` | ✅ | View all bookings platform-wide |
 
---
 
##  Contributing
 
Contributions are what make the open-source community such an amazing place! Any contributions you make are **greatly appreciated**.
 
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
---
 
##  License
 
Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.
 
---
 
##  Contact
 
**Suresh** — [@Suresh-1116](https://github.com/Suresh-1116)
 
Project Link: [https://github.com/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home](https://github.com/Suresh-1116/HouseHunt-Finding-Your-Perfect-Rental-Home)
 
---
 
<div align="center">
Made with ❤️ by <a href="https://github.com/Suresh-1116">Suresh</a>
 
 Star this repo if you found it helpful!
 
</div>
 
