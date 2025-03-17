# AuthenticationUser
Backend Authentication & User Management API
Overview
This project is a robust and secure authentication and user management API developed using Node.js, Express.js, and MongoDB. It includes foundational authentication features like JWT-based login, user registration, and full CRUD capabilities for efficient user data management. The implementation focuses exclusively on backend processes, without any associated frontend or middleware, streamlining the workflow for user authentication and data handling.

Features
User Signup
Enable the registration of a new user by providing essential details such as username, email, and password.

JWT-Based User Login
Facilitate user authentication using email and password, generating a JWT token for secure, subsequent requests.

User Logout
Log out users by effectively invalidating the session. (Note: Since JWTs are stateless, logging out involves simply refraining from including the token in future requests.)

CRUD Operations for User Management  

Get user details: Access a user's profile using their unique identifier.
Update user details: Change user information like username and email address.
Delete user: Permanently erase a user's information from the database.
How to Run the Project
Open the project folder in your chosen code editor (e.g., VS Code).

Launch a terminal.

Navigate to the backend directory by executing:

CopyReplit
cd backend
Install the required dependencies by running:

CopyReplit
npm install
Start the server with:

CopyReplit
npm run start
This command will initiate the API server on the port specified in the .env file (default is set to port 5000).

Testing the APIs
You can use tools like Thunder Client, Postman, or any other API testing application to interact with the following endpoints.

API Endpoints
Authentication
POST /signup
Register a new user.

Request body:
CopyReplit
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "password123"
}
POST /login
Authenticate the user and receive a JWT token.

Request body:
CopyReplit
{
  "email": "john@example.com",
  "password": "password123"
}
GET /logout
Logs out the user (JWT token invalidation is handled on the client-side).

User Management
GET /user/:id
Retrieve the details of a user using their unique ID.

PUT /user/:id
Update user information (such as username and email).

Request body:
CopyReplit
{
  "username": "john_updated",
  "email": "john_updated@example.com"
}
DELETE /user/:id
Permanently delete a user from the database.
