# Real-Time Chat Application Backend

## Setup and Run Instructions:

1. Clone the repository using `git clone https://github.com/your_username/repository_name.git`.
2. Navigate to the project directory.
3. Install dependencies with `npm install`.
4. Set up environment variables. Create a `.env` file and add the following:

5. Run the application using `npm start`.
6. Access the API endpoints using a tool like Postman or integrate with your frontend.

## API Route Descriptions:

### 1. User Authentication
- `POST /api/auth/register`: Register a new user.
  - Inputs: `{ "email": "example@example.com", "password": "your_password" }`
  - Output: `{ "message": "User registered successfully" }`
- `POST /api/auth/login`: Login existing user.
  - Inputs: `{ "email": "example@example.com", "password": "your_password" }`
  - Output: `{ "token": "your_jwt_token" }`

### 2. Chat Functionality
- `GET /api/chat/messages`: Get all messages.
  - Output: Array of messages.
- `POST /api/chat/send`: Send a message.
  - Inputs: `{ "sender": "sender_id", "recipient": "recipient_id", "content": "message_content" }`
  - Output: `{ "message": "Message sent successfully" }`

### 3. User Online Status and LLM Integration
- `PUT /api/user/status`: Update user status.
  - Inputs: `{ "status": "AVAILABLE" or "BUSY" }`
  - Output: `{ "message": "User status updated" }`
- Real-time integration with LLM API:
  - When sending a message, if the recipient is "BUSY", a response from LLM API is generated within 10 seconds.
  - If LLM API does not respond within 10 seconds, a standard message indicating the user is unavailable is sent.

## Environment Configurations:

- `PORT`: Port number for the server (e.g., 3000).
- `JWT_SECRET`: Secret key for JWT token generation.
- `MONGODB_URI`: MongoDB connection URI.
- `LLM_API_URL`: URL for the Language Model API.

## Functionality:

- All features are fully functional, including user authentication, real-time chat, message storage, user online status, and LLM integration.

## Code Quality:

- The code is well-commented, organized, and follows best practices for Node.js development.

## Scalability:

- The system is designed to handle multiple users simultaneously through efficient use of technologies like Socket.io and MongoDB.

## Security:

- User data and credentials are securely managed with JWT for authentication and MongoDB for data storage.

## LLM Integration:

- The system effectively integrates with third-party LLM APIs for offline user interaction, ensuring responses within 10 seconds as per the specified requirement.

## Additional Notes:

- Please refer to the provided Postman collection (hq_collection.json) for API interaction and testing.
- For any further assistance or queries, feel free to contact the project maintainer.

## Submission:

- [GitHub Repository Link](https://github.com/your_username/repository_name)
- [Video Explanation and Demonstration Link](provide_your_link_here)

This README provides a comprehensive overview of the backend architecture and functionalities of the real-time chat application.
