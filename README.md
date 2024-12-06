# E-Commerce Website Backend  

This project is a backend implementation for an e-commerce platform built using **Node.js**. It provides functionality for user authentication, product management, cart handling, and order processing. The backend is designed to be robust, secure, and efficient, with a RESTful API architecture.  

## Features  

- **User Authentication**  
  - Registration and login functionality with secure password hashing.  
  - JSON Web Tokens (JWT) for session management.  

- **Product Management**  
  - Add, update, view, and delete product details.  
  - Fetch product lists with pagination and search options.  

- **Cart Functionality**  
  - Add and remove products from the cart.  
  - View the cart's current contents and total price.  

- **Order Processing**  
  - Create and manage user orders.  
  - View past order history.  

## Tech Stack  

- **Backend Framework:** Node.js  
- **API Design:** RESTful APIs  
- **Security:** JSON Web Tokens (JWT), bcrypt for password hashing  
- **Development Tools:** Postman for API testing  

## Prerequisites  

To run this project locally, ensure you have the following installed:  
- Node.js (v14 or above)  
- npm (v6 or above)  

## Installation  

1. Clone the repository:  
   ```bash  
   git clone https://github.com/your-username/ecommerce-backend.git  
   cd ecommerce-backend  
   ```  

2. Install dependencies:  
   ```bash  
   npm install  
   ```  

3. Create a `.env` file in the root directory with the following variables:  
   ```env  
   PORT=5000  
   JWT_SECRET=your_secret_key  
   ```  

4. Start the server:  
   ```bash  
   npm start  
   ```  

5. Access the API at `http://localhost:5000/`.  

## API Endpoints  

### User Authentication  
- **POST** `/api/auth/register` - Register a new user.  
- **POST** `/api/auth/login` - Login for existing users.  

### Product Management  
- **GET** `/api/products` - Fetch a list of products.  
- **POST** `/api/products` - Add a new product (Admin only).  
- **PUT** `/api/products/:id` - Update product details (Admin only).  
- **DELETE** `/api/products/:id` - Delete a product (Admin only).  

### Cart Management  
- **POST** `/api/cart` - Add a product to the cart.  
- **GET** `/api/cart` - Get the current cart.  
- **DELETE** `/api/cart/:productId` - Remove a product from the cart.  

### Order Processing  
- **POST** `/api/orders` - Create a new order.  
- **GET** `/api/orders` - Fetch the user's order history.  

## Folder Structure  

```plaintext  
ecommerce-backend/  
├── controllers/          # Logic for handling API requests  
├── middleware/           # Middleware functions for authentication and validation  
├── models/               # Data models for users, products, and orders  
├── routes/               # API route definitions  
├── utils/                # Utility functions  
├── .env                  # Environment variables  
├── server.js             # Entry point for the application  
├── package.json          # Project metadata and dependencies  
```  

## Future Enhancements  

- Add a database to persist data (e.g., MongoDB, PostgreSQL).  
- Integrate payment gateways.  
- Implement role-based access control (RBAC).  
- Add unit and integration tests for APIs.  

## License  

This project is open-source and available under the MIT License.  
