# RezzyStyle: Online Shopping Web Application (MERN)

**BSc final-year project** · Kazi Rezwan Rashid · BSc in Computer Science and Engineering, Jahangirnagar University

RezzyStyle is a full-stack online clothing store built with the MERN stack (MongoDB, Express.js, React.js, Node.js) and Redux. It has a Bangladeshi fashion catalogue and seasonal collections (Eid, Pohela Baishakh, Gents, Girls, Kids). Customers can browse, search, review and buy products. Administrators can manage products, users and orders from a dashboard.

## Abstract

This project presents the design and implementation of a full-stack online shopping web application built with the MERN stack. Customers can register, browse and search products, read and write reviews, manage a shopping cart and place orders. Payment is handled by an integrated online payment gateway: PayPal and credit card, in sandbox mode. An administrator panel lets store managers add and update products, upload product images, track stock levels, manage users and mark orders as delivered. On the back end, a RESTful API built with Express.js and Node.js connects the React and Redux front end to a MongoDB database. The database stores user profiles, product catalogues, orders and payment results as structured documents, and JWT-based authentication protects user and admin routes.

## Features

- Product catalogue with seasonal collections (Eid, Baishakhi) and category pages (Gents, Girls, Kids)
- Product search, pagination, top-rated product carousel
- Product reviews and ratings
- Shopping cart and a multi-step checkout (shipping → payment method → place order)
- PayPal / credit card payment (sandbox)
- User registration, login (JWT), profile with order history
- Admin dashboard: product CRUD with image upload, user management, order management, mark as delivered
- Database seeder with sample products and users
## Connect with me



[![Facebook](https://img.shields.io/badge/Facebook-Follow-blue)](https://www.facebook.com/crazewan1699)
[![LinkedIn](https://www.linkedin.com/in/kazi-rezwan-rashid-043686183/skills/edit/forms/new/)
[![GitHub](https://img.shields.io/github/followers/YOUR_GITHUB_USERNAME?style=social)](https://github.com/kazirezwan)
Personal website - https://rezwanrashid.pythonanywhere.com/
## Tech stack

| Layer | Technology |
|---|---|
| Front end | React 16, Redux, React-Bootstrap, React Router |
| Back end | Node.js, Express.js, JWT, Multer (image upload) |
| Database | MongoDB with Mongoose |
| Payments | PayPal JavaScript SDK (sandbox) |

## Project structure

```
backend/
  config/        database connection
  controllers/   product, user and order logic
  data/          seed products and users
  middleware/    auth and error handling
  models/        Mongoose schemas (User, Product, Order)
  routes/        REST API routes
  seeder.js      import / destroy sample data
  server.js      Express app entry point
frontend/
  public/        static files and product images
  src/
    actions/ reducers/ constants/   Redux state
    components/                     reusable UI
    screens/                        pages (Home, Product, Cart, Checkout, Admin, Eid, Baishakhi, ...)
uploads/         product images uploaded by admins
```

## How to run it locally

### Requirements
- **Node.js 16 LTS** (recommended; the front end uses react-scripts 3.4).
  On Node 17 or newer, run `set NODE_OPTIONS=--openssl-legacy-provider` (Windows) or `export NODE_OPTIONS=--openssl-legacy-provider` (macOS/Linux) before starting.
- **MongoDB**: a local install, or a free MongoDB Atlas cluster.

### 1. Install dependencies
```bash
npm install
npm install --prefix frontend
```

### 2. Configure environment variables
Copy `.env.example` to `.env` in the project root and fill in the values:
```
NODE_ENV=development
MONGO_URI=mongodb://127.0.0.1:27017/rezzystyle
JWT_SECRET=any_long_random_string
PAYPAL_CLIENT_ID=sb
```

### 3. Load the sample data
```bash
npm run data:import
```

### 4. Start the app
```bash
npm run dev
```
- Front end: http://localhost:3000
- API: http://localhost:5000

### Test accounts (created by the seeder)
| Role | Email | Password |
|---|---|---|
| Admin | admin@example.com | 123456 |
| Customer | john@example.com | 123456 |

## Acknowledgement

This project was built on the architecture of the open-source **ProShop** MERN e-commerce project by Brad Traversy (MIT licence), from his *MERN eCommerce From Scratch* course. It was extended into RezzyStyle with a Bangladeshi clothing catalogue, seasonal and category collection pages, a custom header and new product data. The original ProShop README is kept in `PROSHOP_ORIGINAL_README.md`.
