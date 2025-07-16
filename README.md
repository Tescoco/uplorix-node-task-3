# Task Management API Assignment

## Overview

Build a RESTful API for a task management system using Node.js, Express, and MongoDB. This assignment will test your understanding of backend development fundamentals, database operations, authentication, and API design.

## Learning Objectives

- Implement CRUD operations with Express.js
- Work with MongoDB and Mongoose ODM
- Implement JWT-based authentication
- Handle file uploads and processing
- Write unit tests and API documentation
- Apply input validation and error handling
- Implement middleware for logging and security

## Requirements

### Core Features

#### 1. User Authentication

- User registration with email verification
- User login with JWT token generation
- Password reset functionality
- Role-based access control (Admin, User)

#### 2. Task Management

- Create, read, update, delete tasks
- Task categories and tags
- Task priorities (Low, Medium, High)
- Task status tracking (Todo, In Progress, Done)
- Due date management with notifications

#### 3. File Management

- Upload task attachments (images, documents)
- File size and type validation
- Serve uploaded files securely

#### 4. Advanced Features

- Search and filter tasks
- Task statistics and analytics
- Email notifications for due tasks
- Export tasks to CSV/JSON

### Technical Requirements

#### Database Schema

Design MongoDB collections for:

- Users (name, email, password, role, verified)
- Tasks (title, description, category, priority, status, dueDate, assignedTo, attachments)
- Categories (name, description, createdBy)

#### API Endpoints

Implement the following routes:

**Authentication:**

- `POST /api/auth/register`
- `POST /api/auth/login`
- `POST /api/auth/verify-email`
- `POST /api/auth/forgot-password`
- `POST /api/auth/reset-password`

**Users:**

- `GET /api/users/profile`
- `PUT /api/users/profile`
- `GET /api/users` (Admin only)

**Tasks:**

- `GET /api/tasks`
- `GET /api/tasks/:id`
- `POST /api/tasks`
- `PUT /api/tasks/:id`
- `DELETE /api/tasks/:id`
- `POST /api/tasks/:id/attachments`

**Categories:**

- `GET /api/categories`
- `POST /api/categories`
- `PUT /api/categories/:id`
- `DELETE /api/categories/:id`

**Analytics:**

- `GET /api/analytics/dashboard`
- `GET /api/analytics/export`

#### Middleware Implementation

- Authentication middleware
- Authorization middleware
- Request logging middleware
- Error handling middleware
- Rate limiting middleware
- File upload middleware

#### Validation & Error Handling

- Input validation using Joi or express-validator
- Proper HTTP status codes
- Consistent error response format
- Async error handling

#### Testing

- Unit tests for utility functions
- Integration tests for API endpoints
- Test coverage minimum 70%
- Use Jest or Mocha

#### Documentation

- API documentation using Swagger/OpenAPI
- Setup and installation instructions
- Environment configuration guide

### Environment Setup

#### Required Dependencies

```
express
mongoose
jsonwebtoken
bcryptjs
multer
nodemailer
joi
helmet
cors
dotenv
jest
supertest
```

#### Environment Variables

```
NODE_ENV=development
PORT=3000
MONGODB_URI=mongodb://localhost:27017/taskmanager
JWT_SECRET=your-jwt-secret
JWT_EXPIRES_IN=7d
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
UPLOAD_PATH=./uploads
```

### Project Structure

```
src/
├── controllers/
├── models/
├── routes/
├── middleware/
├── utils/
├── config/
├── tests/
├── uploads/
└── app.js
```

## Evaluation Criteria

### Functionality (40%)

- All required endpoints working correctly
- Proper CRUD operations
- Authentication and authorization
- File upload functionality

### Code Quality (25%)

- Clean, readable code
- Proper error handling
- Input validation
- Security best practices

### Database Design (15%)

- Well-structured schema
- Proper relationships
- Efficient queries
- Data validation

### Testing (10%)

- Comprehensive test coverage
- Both unit and integration tests
- Test organization and clarity

### Documentation (10%)

- Clear API documentation
- Setup instructions
- Code comments where necessary

## Bonus Features

- Real-time notifications using Socket.IO
- Task collaboration features
- Advanced search with full-text indexing
- API versioning
- Docker containerization
- CI/CD pipeline setup

## Submission Guidelines

1. Create a GitHub repository
2. Include comprehensive README with setup instructions
3. Provide sample environment file
4. Include Postman collection for API testing
5. Submit repository link

## Time Allocation

- **Recommended duration:** 3-4 days
- **Setup and planning:** 4 hours
- **Core development:** 20 hours
- **Testing and documentation:** 8 hours
- **Bonus features:** 4 hours

## Getting Started

1. Initialize npm project and install dependencies
2. Set up MongoDB connection
3. Create basic Express server
4. Implement authentication system
5. Build task management features
6. Add file upload functionality
