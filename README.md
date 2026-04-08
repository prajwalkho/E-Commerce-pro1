# E-Commerce Project

A full-stack e-commerce application built with Node.js, Express, MongoDB for the backend and React, Vite for the frontend. This project allows users to register, login, browse products, manage their cart, and perform CRUD operations on products.

## Features

- **User Authentication**: Secure registration and login with JWT tokens and password hashing using bcrypt.
- **Product Management**: Add, view, edit, delete, and search products.
- **Shopping Cart**: Add products to cart, view cart contents, and manage cart items.
- **Responsive UI**: Built with React and styled using TailwindCSS for a modern, responsive design.
- **API Integration**: RESTful API endpoints for seamless frontend-backend communication.

## Tech Stack

### Backend
- **Node.js**: JavaScript runtime for server-side development.
- **Express.js**: Web framework for building APIs.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: ODM for MongoDB.
- **JWT**: For secure token-based authentication.
- **bcrypt**: For password hashing.
- **CORS**: For handling cross-origin requests.
- **Morgan**: HTTP request logger.

### Frontend
- **React**: JavaScript library for building user interfaces.
- **Vite**: Fast build tool and development server.
- **React Router**: For client-side routing.
- **TailwindCSS**: Utility-first CSS framework for styling.
- **Lucide React**: Icon library for UI elements.

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (running locally on port 27017)
- npm or yarn

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/e-commerce-project.git
   cd e-commerce-project
   ```

2. **Install backend dependencies**:
   ```bash
   cd backend
   npm install
    npm start
   ```

3. **Install frontend dependencies**:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

4. **Start MongoDB**:
   Ensure MongoDB is running on `mongodb://127.0.0.1:27017/ecommerceShop`.

5. **Start the backend server**:
   ```bash
   cd backend
   npm start
   ```
   The backend will run on `http://localhost:3000` (assuming default Express port).

6. **Start the frontend development server**:
   ```bash
   cd frontend
   npm run dev
   ```
   The frontend will run on `http://localhost:5173` (default Vite port).

## Usage

1. Open your browser and navigate to `http://localhost:5173`.
2. Register a new account or login with existing credentials.
3. Browse products on the home page.
4. Add products to your cart.
5. View and manage your cart.
6. As an authenticated user, add, edit, or delete products.

### API Endpoints

- `POST /register`: Register a new user.
- `POST /login`: Login user.
- `GET /products`: Get all products.
- `POST /add-product`: Add a new product (requires auth).
- `GET /product/:id`: Get product by ID.
- `PATCH /product/edit/:id`: Edit product (requires auth).
- `DELETE /product/delete/:id`: Delete product (requires auth).
- `GET /product/search/:keyword`: Search products.
- `GET /cart`: Get user's cart (requires auth).
- `POST /cart/add`: Add products to cart (requires auth).
- `DELETE /cart/product/delete`: Remove product from cart (requires auth).

## Folder Structure

```
e-commerce-project/
├── backend/
│   ├── app.js                 # Main server file
│   ├── package.json           # Backend dependencies and scripts
│   └── models/
│       ├── User.js            # User model
│       ├── Product.js         # Product model
│       └── Cart.js            # Cart model
├── frontend/
│   ├── public/                # Static assets
│   ├── src/
│   │   ├── api/               # API service functions
│   │   ├── components/        # Reusable UI components
│   │   ├── Context/           # React context for auth
│   │   ├── Pages/             # Page components
│   │   ├── App.jsx            # Main app component
│   │   ├── main.jsx           # Entry point
│   │   └── index.css          # Global styles
│   ├── package.json           # Frontend dependencies and scripts
│   ├── vite.config.js         # Vite configuration
│   └── eslint.config.js       # ESLint configuration
└── README.md                  # Project documentation
```

## Contributing

1. Fork the repository.
2. Create a new branch for your feature.
3. Commit your changes.
4. Push to the branch.
5. Open a pull request.

## License

This project is licensed under the ISC License.

