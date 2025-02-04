# Node.js RESTful API (Shop API)

## Overview
This is a RESTful API for an online shop built using Node.js and Express. It allows users to browse products, manage their shopping carts, and place orders. The API follows RESTful principles and communicates via JSON.

## Technologies Used
- Node.js with Express.js
- MongoDB with Mongoose
- JWT for authentication
- Multer for file uploads
- Morgan for logging
- Bcrypt for password hashing

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/thealiqaf/API.git
   cd API
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Set up environment variables in a `.env` file:
   ```env
   PORT=3000
   MONGO_ATLAS_PW=your_mongodb_password
   JWT_SECRET=your_secret_key
   ```
4. Start the server:
   ```sh
   npm start
   ```

## API Endpoints

### Authentication
| Method | Endpoint       | Description       |
|--------|--------------|------------------|
| POST   | `/user/register` | Register a new user |
| POST   | `/user/login` | Log in and receive a token |

### Products
| Method | Endpoint        | Description        |
|--------|---------------|-------------------|
| GET    | `/products` | Get all products  |
| GET    | `/products/:id` | Get a single product by ID |
| POST   | `/products` | Create a new product (admin only) |
| PUT    | `/products/:id` | Update a product (admin only) |
| DELETE | `/products/:id` | Delete a product (admin only) |

### Orders
| Method | Endpoint        | Description        |
|--------|---------------|-------------------|
| GET    | `/orders` | Get all orders (admin only) |
| GET    | `/orders/:id` | Get a specific order |
| POST   | `/orders` | Create a new order |

## Middleware & CORS
- **Morgan** is used for logging HTTP requests.
- **Body-parser** is used to parse incoming JSON and URL-encoded data.
- **CORS Headers** allow requests from any origin (`'*'`).

## Authentication
This API uses JWT authentication. Users must include a valid JWT token in the `Authorization` header for protected routes:
```sh
Authorization: Bearer your_token_here
```

## License
This project is licensed under the ISC License.

## Contributing
Feel free to fork the repository and submit pull requests!

## Contact
For any questions, reach out to `thealiqaf` or create an issue in the repository.
