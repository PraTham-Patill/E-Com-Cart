# Mock E-Com Cart

## Description
A full-stack shopping cart application built for Vibe Commerce screening. This project demonstrates UI, API, and database integration for e-commerce flows including add/remove items, totals calculation, and mock checkout functionality (no real payment processing).

## Author
**Pratham Patil**

## Features
- **Product Listing**: Display 5-10 mock products with details
- **Shopping Cart**: Add, remove, and update product quantities
- **Cart Calculations**: Real-time total price calculation
- **Mock Checkout**: Order placement with receipt generation (name, email, total, timestamp)
- **User Authentication**: Secure login and registration using JWT
- **Admin Dashboard**: Manage products, orders, and users
- **Responsive Design**: Optimized for both desktop and mobile devices
- **Search and Filter**: Find products easily with search functionality
- **Reviews and Ratings**: Product review system
- **Database Persistence**: MongoDB integration for data storage

## Technologies Used
- **Frontend**: React.js, Redux, React Router, Axios, Vite
- **Backend**: Node.js, Express.js, JWT for authentication
- **Database**: MongoDB, Mongoose
- **Image Hosting**: Cloudinary
- **Payment Gateway**: Stripe (mock mode)
- **Version Control**: Git

## Installation and Setup

1. **Clone the repository**:
    ```bash
    git clone https://github.com/PraTham-Patill/E-Com-Cart.git
    cd E-Com-Cart
    ```

2. **Install all dependencies**:
    ```bash
    npm install
    ```

3. **Install frontend dependencies**:
    ```bash
    cd frontend
    npm install
    cd ..
    ```

4. **Configure Environment Variables**:
    Create a `.env` file in the root directory with the following variables:
    ```
    PORT=4000
    MONGO_URI=your_mongodb_connection_string
    STRIPE_API_KEY=your_stripe_api_key
    STRIPE_SECRET_KEY=your_stripe_secret_key
    JWT_SECRET=your_jwt_secret
    JWT_LIFETIME=7d
    JWT_COOKIE_EXPIRE=7
    SMTP_SERVICE=gmail
    SMTP_MAIL=your_email@gmail.com
    SMTP_PASSWORD=your_email_password
    SMTP_HOST=smtp.gmail.com
    SMTP_PORT=465
    CLOUDINARY_NAME=your_cloudinary_name
    CLOUDINARY_API_KEY=your_cloudinary_api_key
    CLOUDINARY_API_SECRET=your_cloudinary_api_secret
    ```

5. **Start the development servers**:
    ```bash
    npm run dev
    ```

## API Endpoints (Assignment Requirements)

- **GET /api/products**: Retrieve 5-10 mock products
- **POST /api/cart**: Add item to cart `{productId, qty}`
- **DELETE /api/cart/:id**: Remove item from cart
- **GET /api/cart**: Get cart items with total
- **POST /api/checkout**: Mock checkout `{cartItems}` → receipt with total and timestamp

## Usage

1. Open your browser and navigate to **http://localhost:5173** to access the frontend
2. Browse products and add them to cart
3. View cart with totals and manage quantities
4. Complete checkout with name/email to receive mock receipt
5. Admin dashboard available at `/admin` for product/order management

## Project Structure

```
├── backend/
│   ├── controllers/     # Request handlers
│   ├── middleware/      # Authentication & authorization
│   ├── modals/          # MongoDB schemas
│   ├── routes/          # API routes
│   └── Utils/           # Helper functions
├── frontend/
│   ├── src/
│   │   ├── Components/  # Reusable UI components
│   │   ├── Pages/       # Page components
│   │   ├── Admin/       # Admin panel components
│   │   ├── actions/     # Redux actions
│   │   └── reducers/    # Redux reducers
│   └── public/
└── package.json
```

## Author
Pratham Patil - [GitHub](https://github.com/PraTham-Patill)

## License
ISC
