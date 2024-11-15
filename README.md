
# E-commerce Backend API

This is the backend for an e-commerce platform, built with **Node.js**, **Express**, and **MongoDB**. It provides RESTful API endpoints for managing products, orders, users, and authentication. This backend connects with a React frontend, styled with Tailwind CSS, to create a full-stack e-commerce application.

---

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [License](#license)

---

## Features

- **User Authentication**: Sign up, login, JWT-based authentication.
- **User Authorization**: Role-based access control for admin and customer functionalities.
- **Product Management**: CRUD operations for products.
- **Order Processing**: Create, view, and update orders.
- **Cart Management**: Add and manage cart items.
- **Payment Integration**: Placeholder setup for payment gateway (e.g., Stripe, PayPal).

---

## Tech Stack

- **Node.js** - JavaScript runtime for building the backend server.
- **Express** - Web framework for Node.js.
- **MongoDB** - NoSQL database to store product, user, and order data.
- **JWT (JSON Web Tokens)** - Secure user authentication.
- **bcrypt** - Password hashing for secure authentication.

---

## Getting Started

### Prerequisites

- **Node.js** and **npm** installed on your machine.
- **MongoDB** instance (local or cloud) for storing data.

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/ecommerce-backend.git
   cd ecommerce-backend
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Set Up Environment Variables**

   Create a `.env` file in the root directory and add the following environment variables:

   ```plaintext
   PORT=5000
   MONGO_URI=<your-mongodb-uri>
   JWT_SECRET=<your-secret-key>
   ```

4. **Run the Application**
   ```bash
   npm start
   ```

   The server will start on `http://localhost:5000`.

### Environment Variables

| Variable        | Description                          |
| --------------- | ------------------------------------ |
| `PORT`          | Port on which the server will run    |
| `MONGO_URI`     | MongoDB connection string            |
| `JWT_SECRET`    | Secret key for signing JWT tokens    |

---

## API Endpoints

Here’s a list of key API endpoints:

### Authentication

- **POST** `/api/auth/register` - Register a new user
- **POST** `/api/auth/login` - Log in a user

### User

- **GET** `/api/users/:id` - Get user details (admin only)
- **DELETE** `/api/users/:id` - Delete a user (admin only)

### Products

- **GET** `/api/products` - Retrieve all products
- **POST** `/api/products` - Add a new product (admin only)
- **PUT** `/api/products/:id` - Update product details (admin only)
- **DELETE** `/api/products/:id` - Delete a product (admin only)

### Cart

- **POST** `/api/cart` - Add items to the cart
- **GET** `/api/cart` - View cart items

### Orders

- **POST** `/api/orders` - Place a new order
- **GET** `/api/orders/:id` - View a specific order (admin only)
- **GET** `/api/orders/user/:userId` - View user’s orders

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Future Enhancements

- **Payment Gateway Integration**: Integrate Stripe or PayPal for processing payments.
- **Review & Rating System**: Allow users to leave reviews and rate products.
- **Wishlist**: Add functionality for users to save favorite items.

---

Happy coding! If you have any questions or run into issues, please feel free to open an issue on this repository.
