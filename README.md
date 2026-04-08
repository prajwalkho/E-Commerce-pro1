# 🛒 E-Commerce Project

[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen)](https://nodejs.org/)
[![React Version](https://img.shields.io/badge/react-18.3.1-blue)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-8.10.1-green)](https://www.mongodb.com/)

A modern, full-stack e-commerce platform built with cutting-edge technologies. This application empowers users to seamlessly register, authenticate, browse a diverse catalog of products, manage shopping carts, and perform comprehensive CRUD operations on products. Designed for scalability and user experience, it combines a robust Node.js backend with a dynamic React frontend.

## ✨ Features

- **🔐 Secure User Authentication**: JWT-based login/registration with bcrypt password hashing for maximum security.
- **📦 Comprehensive Product Management**: Full CRUD operations (Create, Read, Update, Delete) with advanced search functionality.
- **🛍️ Intuitive Shopping Cart**: Add, view, and manage cart items with real-time updates.
- **📱 Responsive Design**: Mobile-first UI built with TailwindCSS for a seamless experience across devices.
- **🔗 RESTful API**: Well-structured endpoints for efficient frontend-backend communication.
- **⚡ Fast Development**: Powered by Vite for lightning-fast builds and hot module replacement.
- **🎨 Modern UI Components**: Enhanced with Lucide React icons for a polished interface.

## 🛠️ Tech Stack

### Backend
- **Node.js** - Server-side JavaScript runtime
- **Express.js** - Fast, unopinionated web framework
- **MongoDB** - NoSQL database for flexible data storage
- **Mongoose** - Elegant MongoDB object modeling
- **JWT (jsonwebtoken)** - Secure token-based authentication
- **bcrypt** - Password hashing for security
- **CORS** - Cross-origin resource sharing
- **Morgan** - HTTP request logger for debugging

### Frontend
- **React 18** - Declarative UI library with hooks
- **Vite** - Next-generation frontend tooling
- **React Router** - Declarative routing for React
- **TailwindCSS** - Utility-first CSS framework
- **Lucide React** - Beautiful & consistent icon toolkit

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **MongoDB** (Community Edition) - [Download here](https://www.mongodb.com/try/download/community)
- **npm** or **yarn** package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/e-commerce-project.git
   cd e-commerce-project
   ```

2. **Set up the backend**
   ```bash
   cd backend
   npm install
   ```

3. **Set up the frontend**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Configure MongoDB**
   - Install and start MongoDB locally
   - Ensure it's running on `mongodb://127.0.0.1:27017/ecommerceShop`
   - Alternatively, update the connection string in `backend/app.js` for a different setup

5. **Environment Variables** (Optional)
   - Create `.env` files in both `backend/` and `frontend/` directories if needed
   - Backend: Add `PORT=3000`, `JWT_SECRET=your-secret-key`
   - Frontend: Add `VITE_API_BASE_URL=http://localhost:3000`

### Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   npm start
   ```
   Server will run on `http://localhost:3000`

2. **Start the frontend development server**
   ```bash
   cd frontend
   npm run dev
   ```
   App will be available at `http://localhost:5173`

## 📖 Usage

1. **Access the application** at `http://localhost:5173`
2. **Create an account** or **log in** with existing credentials
3. **Explore products** on the home page
4. **Add items to cart** and manage your shopping list
5. **Perform product operations** (add, edit, delete) as an authenticated user
6. **Search products** using the search functionality

### API Reference

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/register` | Register a new user | ❌ |
| POST | `/login` | User login | ❌ |
| GET | `/products` | Retrieve all products | ❌ |
| POST | `/add-product` | Create a new product | ✅ |
| GET | `/product/:id` | Get product by ID | ❌ |
| PATCH | `/product/edit/:id` | Update product | ✅ |
| DELETE | `/product/delete/:id` | Delete product | ✅ |
| GET | `/product/search/:keyword` | Search products | ❌ |
| GET | `/cart` | Get user's cart | ✅ |
| POST | `/cart/add` | Add items to cart | ✅ |
| DELETE | `/cart/product/delete` | Remove item from cart | ✅ |

**Example API Usage:**
```bash
# Register a user
curl -X POST http://localhost:3000/register \
  -H "Content-Type: application/json" \
  -d '{"email":"user@example.com","password":"password123","name":"John Doe"}'

# Get all products
curl http://localhost:3000/products
```

## 📁 Project Structure

```
e-commerce-project/
├── backend/
│   ├── app.js                 # Express server setup & routes
│   ├── package.json           # Backend dependencies & scripts
│   └── models/                # MongoDB schemas
│       ├── User.js            # User model
│       ├── Product.js         # Product model
│       └── Cart.js            # Shopping cart model
├── frontend/
│   ├── public/                # Static assets
│   ├── src/
│   │   ├── api/               # API service functions
│   │   ├── components/        # Reusable React components
│   │   ├── Context/           # React Context for state management
│   │   ├── Pages/             # Route components
│   │   ├── App.jsx            # Main app component
│   │   ├── main.jsx           # React entry point
│   │   └── index.css          # Global styles
│   ├── package.json           # Frontend dependencies & scripts
│   ├── vite.config.js         # Vite configuration
│   └── eslint.config.js       # ESLint configuration
├── README.md                  # Project documentation
└── .gitignore                 # Git ignore rules
```

## 🧪 Testing

- **Backend**: Run tests with `npm test` (if implemented)
- **Frontend**: Run linting with `npm run lint`
- **Manual Testing**: Use tools like Postman for API testing

## 🚀 Deployment

### Backend Deployment
- Use platforms like Heroku, Railway, or Vercel
- Set environment variables for production
- Configure MongoDB Atlas for cloud database

### Frontend Deployment
- Build with `npm run build`
- Deploy to Netlify, Vercel, or GitHub Pages
- Update API base URL for production

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow ESLint rules
- Write clear, concise commit messages
- Test your changes thoroughly
- Update documentation as needed

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 🙋 Support

If you have any questions or need help:
- Open an issue on GitHub
- Check the documentation
- Contact the maintainers

## 📸 Screenshots

*(Add actual screenshots here)*

### Landing Page
![Landing Page](screenshots/landing-page.png)

### Product Catalog
![Product Listing](screenshots/product-listing.png)

### Shopping Cart
![Cart View](screenshots/cart-view.png)

### Product Management
![Add Product](screenshots/add-product.png)

---

**Made with ❤️ by [ppk]**

