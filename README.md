# Game Store Full Stack

A full-stack web application for an online game store built with **Node.js/Express** backend and a modern frontend. This application provides features for browsing, purchasing, and managing games.

## 🎮 Project Overview

Game Store Full Stack is a complete e-commerce solution for digital games. It combines a robust backend API with a responsive frontend to deliver a seamless shopping experience for gamers.

### Key Features

- **User Authentication**: Secure user registration and login with bcrypt password hashing
- **Game Catalog**: Browse and search games available in the store
- **Shopping Cart**: Add and manage games in your shopping cart
- **Secure Transactions**: Payment processing with secure backend handling
- **User Profiles**: Manage user accounts and purchase history
- **Responsive Design**: Works across desktop, tablet, and mobile devices

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.0.0 or higher)
- **npm** (v6.0.0 or higher)
- **MySQL** (v5.7 or higher)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/mAbdullah02-bit/Game-Store-Full-Stack.git
cd Game-Store-Full-Stack
```

### 2. Backend Setup

Navigate to the backend directory and install dependencies:

```bash
cd backend
npm install
```

### 3. Frontend Setup

Navigate to the frontend directory and install dependencies:

```bash
cd frontend
npm install
```

## 🔧 Configuration

### Backend Configuration

1. Create a `.env` file in the `backend` directory with the following variables:

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=game_store
NODE_ENV=development
```

2. Ensure your MySQL server is running and the database `game_store` is created.

### Frontend Configuration

Update your frontend API endpoints to match your backend URL (typically `http://localhost:5000`).

## 📦 Running the Application

### Start the Backend Server

```bash
cd backend
npm start
# Or for development with auto-reload
npx nodemon
```

The backend server will run on `http://localhost:5000`

### Start the Frontend

```bash
cd frontend
npm start
```

The frontend will typically run on `http://localhost:3000` (or the next available port)

## 📁 Project Structure

```
Game-Store-Full-Stack/
├── backend/                 # Express.js backend server
│   ├── routes/             # API route definitions
│   ├── controllers/        # Request handlers
│   ├── models/             # Database models
│   ├── middleware/         # Custom middleware
│   ├── package.json        # Backend dependencies
│   └── server.js           # Main server file
├── frontend/               # Frontend application
│   ├── public/            # Static assets
│   ├── src/               # React source code
│   ├── components/        # Reusable components
│   ├── pages/             # Page components
│   └── package.json       # Frontend dependencies
└── README.md              # This file
```

## 🛠️ Technologies Used

### Backend
- **Express.js** - Web application framework
- **MySQL2** - MySQL database driver
- **bcryptjs** - Password hashing
- **CORS** - Cross-Origin Resource Sharing middleware
- **body-parser** - Request body parsing
- **nodemon** - Development server with auto-reload

### Frontend
- **React** - UI library
- **JavaScript** - Programming language

## 📝 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Games
- `GET /api/games` - Get all games
- `GET /api/games/:id` - Get a specific game
- `POST /api/games` - Create a new game (admin only)
- `PUT /api/games/:id` - Update a game (admin only)
- `DELETE /api/games/:id` - Delete a game (admin only)

### Cart
- `GET /api/cart` - Get user's cart
- `POST /api/cart` - Add item to cart
- `DELETE /api/cart/:gameId` - Remove item from cart

### Orders
- `GET /api/orders` - Get user's orders
- `POST /api/orders` - Create a new order
- `GET /api/orders/:id` - Get order details

## 🔐 Security Features

- **Password Hashing**: Passwords are hashed using bcryptjs
- **CORS**: Configured to allow only authorized origins
- **Input Validation**: Server-side validation of all inputs
- **SQL Injection Protection**: Parameterized queries with MySQL2

## 📊 Database Schema

The application uses the following main tables:

- **users** - User accounts and authentication
- **games** - Game catalog information
- **orders** - Purchase orders
- **order_items** - Individual items in orders
- **cart** - User shopping carts

## 🐛 Troubleshooting

### Port Already in Use
If port 5000 is already in use, change the `PORT` environment variable in your `.env` file.

### Database Connection Error
Ensure your MySQL server is running and credentials in the `.env` file are correct.

### CORS Errors
Check that your frontend is making requests to the correct backend URL and that CORS is properly configured.

## 📈 Future Enhancements

- [ ] Payment gateway integration (Stripe, PayPal)
- [ ] Admin dashboard for game management
- [ ] User reviews and ratings
- [ ] Wishlist functionality
- [ ] Game recommendations engine
- [ ] Multi-language support
- [ ] Dark mode theme
- [ ] Advanced search filters

## 📜 License

This project is licensed under the ISC License - see the LICENSE file for details.

## 👤 Author

**mAbdullah02-bit**

- GitHub: [@mAbdullah02-bit](https://github.com/mAbdullah02-bit)

## 🤝 Contributing

Contributions are welcome! If you'd like to contribute to this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

If you encounter any issues or have questions, please:
- Open an issue on GitHub
- Contact the author

---

**Happy Gaming! 🎮**
