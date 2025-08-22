# 🚀 Real-Time Chat App - NodeJS Backend

A powerful real-time chat application backend built with Node.js, Express, and Socket.IO. This backend provides seamless real-time messaging capabilities with robust user authentication and room management features.

![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![Socket.io](https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

## ✨ Features

- **Real-time messaging** - Instant message delivery using Socket.IO
- **User authentication** - Secure user registration and login system
- **Group chat rooms** - Create and join multiple chat rooms Will be implement later
- **RESTful API** - Clean and well-documented API endpoints

## 🛠️ Tech Stack

- **Runtime:** Node.js
- **Framework:** Express.js
- **Real-time Communication:** Socket.IO
- **Database:** MongoDB
- **Authentication:** JWT (JSON Web Tokens)
- **Password Hashing:** bcrypt
- **Environment Management:** dotenv
- **HTTP Client:** Axios (for external API calls)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/docs/manual/installation/) (Local or Atlas)
- [Git](https://git-scm.com/)

## 🚀 Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/elonerajeev/Real-Time-Chat-App-NodeJS-Backend.git
cd Real-Time-Chat-App-NodeJS-Backend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Environment Setup

Create a `.env` file in the root directory and add the following variables:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/chatapp
JWT_SECRET=your_super_secret_jwt_key
NODE_ENV=development
CORS_ORIGIN=http://localhost:3000
```

### 4. Start MongoDB

Make sure MongoDB is running on your system:

```bash
# For Windows
net start MongoDB

# For macOS (if installed via Homebrew)
brew services start mongodb-community

# For Linux
sudo systemctl start mongod
```

### 5. Run the application

```bash
# Development mode with nodemon
npm run dev

# Production mode
npm start
```

The server will start on `http://localhost:5000`

## 📁 Project Structure

```
Real-Time-Chat-App-NodeJS-Backend/
├── controllers/           # Request handlers
├── middleware/           # Custom middleware functions
├── models/              # Database models
├── routes/              # API routes
├── socket/              # Socket.IO event handlers
├── utils/               # Utility functions
├── config/              # Configuration files
├── .env.example         # Environment variables template
├── server.js            # Main server file
└── package.json         # Dependencies and scripts
```

## 🔌 API Endpoints

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/profile` - Get user profile

### Messages

- `GET /api/messages/:chatId` - Get chat messages
- `POST /api/messages/send` - Send a message
- `DELETE /api/messages/:messageId` - Delete a message

### Users

- `GET /api/users` - Get all users
- `GET /api/users/:userId` - Get user by ID
- `PUT /api/users/profile` - Update user profile

## 🔌 Socket Events

### Client to Server

- `join_room` - Join a chat room
- `leave_room` - Leave a chat room
- `send_message` - Send a message
- `typing` - User typing indicator
- `stop_typing` - Stop typing indicator

### Server to Client

- `message_received` - New message received
- `user_joined` - User joined room
- `user_left` - User left room
- `typing_indicator` - Show typing indicator
- `online_users` - List of online users

## 🧪 Testing

```bash
# Run tests
npm test

# Run tests with coverage
npm run test:coverage

# Run tests in watch mode
npm run test:watch
```

## 🐳 Docker Support

### Using Docker Compose (Recommended)

```bash
# Build and run with Docker Compose
docker-compose up --build

# Run in detached mode
docker-compose up -d
```

### Manual Docker Setup

```bash
# Build the image
docker build -t chat-app-backend .

# Run the container
docker run -p 5000:5000 --env-file .env chat-app-backend
```

## 🌐 Environment Variables

| Variable      | Description               | Default                             |
| ------------- | ------------------------- | ----------------------------------- |
| `PORT`        | Server port               | `5000`                              |
| `MONGO_URI`   | MongoDB connection string | `mongodb://localhost:27017/chatapp` |
| `JWT_SECRET`  | JWT secret key            | Required                            |
| `NODE_ENV`    | Environment mode          | `development`                       |
| `CORS_ORIGIN` | CORS origin URL           | `http://localhost:3000`             |

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Rajeev Elone**

- GitHub: [@elonerajeev](https://github.com/elonerajeev)
- LinkedIn: [Connect with me](https://linkedin.com/in/elonerajeev)

## 🙏 Acknowledgments

- Socket.IO team for the amazing real-time engine
- Express.js community for the robust web framework
- MongoDB team for the flexible database solution

## 📞 Support

If you have any questions or need help getting started, feel free to:

- Open an issue on GitHub
- Reach out via email
- Connect on LinkedIn

---

⭐ **If you found this project helpful, please give it a star!** ⭐
