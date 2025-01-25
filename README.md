# Learning Management System (LMS)

This is a MERN stack-based Learning Management System (LMS) platform with two user roles:
- **Candidates:** Can view or purchase courses.
- **Instructors:** Can add, edit, and remove courses.

## Features

### For Candidates
- Browse available courses.
- Purchase courses securely.
- Track course progress.
- View enrolled courses.

### For Instructors
- Add new courses.
- Edit existing course details.
- Remove courses.
- View enrolled students.

### General Features
- User authentication (Context API-based login/signup).
- Secure payment gateway integration.
- Responsive UI with React.
- RESTful API backend.

## Tech Stack

**Frontend:**
- React.js
- React Router
- Context API (for state management)
- TailwindCSS / Bootstrap (for styling)

**Backend:**
- Node.js
- Express.js
- MongoDB (Mongoose ODM)
- JWT Authentication

**Other Tools & Libraries:**
- Cloudinary / Firebase (for file uploads, if used)
- Stripe / PayPal (for payments, if used)
- Nodemailer (for email notifications)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mern-lms.git
   cd mern-lms
   ```

2. Install dependencies for both client and server:
   ```bash
   cd server
   npm install
   cd ../client
   npm install
   ```

3. Set up environment variables:
   - Create a `.env` file in the `server` directory with the following:
     ```env
     MONGO_URI=your_mongo_db_connection_string
     JWT_SECRET=your_secret_key
     STRIPE_SECRET_KEY=your_stripe_key (if used)
     ```

4. Start the development servers:
   ```bash
   # Server
   cd server
   npm run dev
   
   # Client
   cd client
   npm start
   ```

5. Open the application in your browser:
   ```
   http://localhost:3000
   ```

## Folder Structure

```
mern-lms/
│-- server/
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   ├── config/
│   ├── middleware/
│   ├── server.js
│   ├── package.json
│
│-- client/
│   ├── src/
│   ├── components/
│   ├── pages/
│   ├── context/
│   ├── App.js
│   ├── package.json
│
│-- .gitignore
│-- README.md
│-- package.json
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user

### Courses
- `GET /api/courses` - Get all courses
- `POST /api/courses` - Add a new course (Instructor only)
- `PUT /api/courses/:id` - Update a course (Instructor only)
- `DELETE /api/courses/:id` - Delete a course (Instructor only)

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes.
4. Push to your fork and submit a pull request.

## License

This project is licensed under the MIT License.

---

Feel free to open an issue for any suggestions or improvements!

