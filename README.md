# RESTful API for Posts

## Overview
This project is a RESTful API built with **Node.js** and **Express.js** for managing posts and users. It provides functionality for user authentication, post creation, updating, deletion, and real-time updates using **Socket.IO**. The API is secured with JSON Web Tokens (JWT) and validates inputs to ensure robust and error-free operations.

---

## Features
- User authentication (signup, login, user status management).
- CRUD operations for posts (create, read, update, delete).
- Real-time updates via **Socket.IO**.
- File uploads (image management).
- Input validation with **express-validator**.
- Pagination support for fetching posts.
- Secure API with JWT authentication.

---

## Technologies Used
- **Node.js**
- **Express.js**
- **Mongoose** (MongoDB ODM)
- **Socket.IO** (real-time updates)
- **JWT** (JSON Web Tokens for authentication)
- **Multer** (file uploads)
- **bcryptjs** (password hashing)
- **express-validator** (input validation)

---

## Installation

### Prerequisites
- Node.js (v14 or later)
- MongoDB (local or cloud instance)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Adihakanyan7/Restfull-API-Posts.git
   cd Restfull-API-Posts
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file and configure the following variables:
   ```env
   MONGO_URI=<Your MongoDB connection string>
   JWT_SECRET=somesupersecretsecret
   ```

4. Run the server:
   ```bash
   npm start
   ```

5. The server will run on `http://localhost:3000`.

---

## API Endpoints

### **Authentication**
| Method | Endpoint           | Description                        |
|--------|--------------------|------------------------------------|
| PUT    | `/auth/signup`     | Register a new user               |
| POST   | `/auth/login`      | Login a user and get a JWT token  |
| GET    | `/auth/status`     | Get the logged-in user's status   |
| PATCH  | `/auth/status`     | Update the logged-in user's status|

### **Feed**
| Method | Endpoint           | Description                        |
|--------|--------------------|------------------------------------|
| GET    | `/feed/posts`      | Fetch all posts (paginated)       |
| POST   | `/feed/post`       | Create a new post                 |
| GET    | `/feed/post/:id`   | Fetch details of a specific post  |
| PUT    | `/feed/post/:id`   | Update a specific post            |
| DELETE | `/feed/post/:id`   | Delete a specific post            |

---

## Folder Structure
```
Restfull-API-Posts
├── controllers
│   ├── auth.js          # Handles user authentication
│   ├── feed.js          # Handles post-related operations
├── models
│   ├── post.js          # Mongoose schema for posts
│   ├── user.js          # Mongoose schema for users
├── routes
│   ├── auth.js          # Authentication routes
│   ├── feed.js          # Feed-related routes
├── middleware
│   ├── is-auth.js       # JWT authentication middleware
├── app.js               # Main application file
├── package.json         # Project metadata and dependencies
├── package-lock.json    # Exact dependency versions
└── Procfile             # Deployment configuration (Heroku)
```

---

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a Pull Request.

---

## License
This project is licensed under the MIT License.
