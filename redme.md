# Shopfinity

Shopfinity is a modern full-stack e-commerce platform built with **Next.js 15**, **Node.js**, **Express**, **PostgreSQL**, and **Prisma**. It offers a seamless shopping experience with secure authentication, robust product and cart management, order processing, coupon support, and PayPal integration for payments.

## Features

- **Modern UI**: Built with Next.js 15 and Tailwind CSS for a fast, responsive, and accessible user experience.
- **Authentication**: Secure JWT-based authentication with role-based access (user, super admin).
- **Product Management**: Admin panel for managing products, categories, inventory, and images (Cloudinary integration).
- **Cart & Checkout**: Persistent cart, address management, and smooth checkout flow.
- **Order Processing**: Real-time order creation, status updates, and order history for users and admins.
- **Coupons**: Create and apply discount coupons with usage limits and expiry.
- **Payments**: Integrated PayPal payment gateway for secure transactions.
- **API**: RESTful API built with Express and Prisma ORM.
- **Database**: PostgreSQL for reliable and scalable data storage.

## Tech Stack

- **Frontend**: Next.js 15, React, Tailwind CSS, Zustand
- **Backend**: Node.js, Express, Prisma ORM
- **Database**: PostgreSQL
- **Authentication**: JWT, cookies
- **Payments**: PayPal
- **Cloud Storage**: Cloudinary (for product images)
- **Dev Tools**: Docker, ESLint, Prettier

## Getting Started

### Prerequisites

- Node.js (v18+)
- npm or yarn
- PostgreSQL database
- [Cloudinary](https://cloudinary.com/) account (for image uploads)
- [PayPal Developer](https://developer.paypal.com/) account

### Clone the Repository

```sh
git clone https://github.com/mdsaifalidev/Shopfinity.git
cd shopfinity
```

### Environment Variables

Set up your environment variables in `.env` files for both `client` and `server`.  
Example for `server/.env`:

```
NODE_ENV=development
PORT=8080
DATABASE_URL=your_postgres_connection_string
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

### Install Dependencies

#### Server

```sh
cd server
npm install
```

#### Client

```sh
cd ../client
npm install
```

### Database Migration

```sh
cd ../server
npx prisma migrate dev
```

### Running the App

#### Start the Server

```sh
cd server
npm run dev
```

#### Start the Client

```sh
cd ../client
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

## License

This project is licensed under the MIT License.

---

**Shopfinity** – A modern, scalable, and secure e-commerce solution.