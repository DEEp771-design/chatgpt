# ChatGPT Clone

A full-stack ChatGPT-like application built with React, Node.js, and MongoDB. Chat with AI, manage credits, and explore a community of users.

## 🚀 Live Demo

**Frontend:** [https://chatgpt-frontend-six-teal.vercel.app/](https://chatgpt-frontend-six-teal.vercel.app/)

## ✨ Features

- 💬 **AI Chat Interface** - Chat with OpenAI API
- 👤 **User Authentication** - Secure login and registration with JWT
- 💳 **Credit System** - Purchase and manage credits for API calls
- 🖼️ **Image Handling** - Upload and process images with ImageKit
- 📱 **Responsive Design** - Works seamlessly on all devices
- 🎨 **Code Syntax Highlighting** - Beautiful code rendering with Prism.js
- 🌐 **Community Features** - Connect with other users
- 🔐 **Secure Payments** - Stripe integration for credit purchases

## 🛠️ Tech Stack

### Frontend
- **React 19** - UI library
- **Vite** - Fast build tool
- **Tailwind CSS** - Utility-first CSS framework
- **Axios** - HTTP client
- **React Router** - Navigation
- **React Markdown** - Markdown rendering
- **React Hot Toast** - Notifications
- **Moment.js** - Date/time handling
- **Prism.js** - Code syntax highlighting

### Backend
- **Node.js** - Runtime
- **Express.js** - Web framework
- **MongoDB & Mongoose** - Database
- **OpenAI API** - AI chat integration
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Stripe** - Payment processing
- **ImageKit** - Image management
- **Svix** - Webhooks

## 📁 Project Structure

```
.
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/         # Page components
│   │   ├── context/       # React context
│   │   └── assets/        # Static assets
│   └── package.json
└── server/                 # Express backend
    ├── controllers/       # Route controllers
    ├── models/           # MongoDB schemas
    ├── routes/           # API routes
    ├── middlewares/      # Custom middleware
    ├── configs/          # Configuration files
    └── server.js         # Main server file
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- OpenAI API Key
- Stripe Account (optional, for payments)
- ImageKit Account (optional, for images)

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd chatgpt
```

2. **Install client dependencies**
```bash
cd client
npm install
```

3. **Install server dependencies**
```bash
cd ../server
npm install
```

### Configuration

1. **Create `.env` file in server directory:**
```
MONGODB_URI=your_mongodb_connection_string
OPENAI_API_KEY=your_openai_api_key
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
```

2. **Create `.env` file in client directory:**
```
VITE_API_URL=http://localhost:5000
```

### Running the Application

**Development Mode:**

Terminal 1 - Start Backend:
```bash
cd server
npm run server
```

Terminal 2 - Start Frontend:
```bash
cd client
npm run dev
```

The application will be available at `http://localhost:5173`

## 📦 Building

**Frontend:**
```bash
cd client
npm run build
```

**Frontend Preview:**
```bash
cd client
npm run preview
```

## 📝 API Routes

### User Routes
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile

### Chat Routes
- `POST /api/chat` - Create new chat
- `GET /api/chat` - Get all chats
- `GET /api/chat/:id` - Get specific chat

### Credits Routes
- `GET /api/credits` - Get credit balance
- `POST /api/credits/purchase` - Purchase credits

### Message Routes
- `POST /api/message` - Send message
- `GET /api/message/:chatId` - Get chat messages

## 🔐 Authentication

The application uses JWT (JSON Web Tokens) for secure authentication. Tokens are stored in HTTP-only cookies for security.

## 💳 Payment Integration

Stripe integration allows users to purchase credits which are used for API calls.

## 📸 Image Handling

ImageKit is integrated for efficient image upload, storage, and delivery.

## 🔄 Webhooks

Svix webhooks are configured for handling payment and user events.

## 📜 License

This project is licensed under the ISC License - see the LICENSE file for details.

## 👤 Author

Created by DEEp771-design

## 🤝 Contributing

Contributions are welcome! Feel free to open issues and submit pull requests.

---

**Deploy your own version:** This project is configured for deployment on Vercel. Follow Vercel's deployment guide to deploy both frontend and backend.
