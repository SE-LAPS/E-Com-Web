# 🛒 E-Commerce Web Application

A full-stack e-commerce platform built with **Next.js 15**, **React 19**, **MongoDB**, and **Material-UI** with modern UI components and comprehensive admin management system.

## ✨ Features

### 🏪 Customer Features
- **Product Browsing & Search** - Browse products by categories with advanced filtering
- **Product Details** - Detailed product pages with reviews and ratings
- **Shopping Cart** - Add/remove items, quantity management
- **Checkout Process** - Secure checkout with Razorpay payment integration
- **User Authentication** - Email verification, OTP-based login
- **Order Management** - Track orders, view order history
- **User Profile** - Manage account details, addresses
- **Product Reviews** - Rate and review purchased products
- **Coupon System** - Apply discount coupons during checkout

### 🔧 Admin Features
- **Dashboard** - Analytics and insights with charts (Recharts)
- **Product Management** - CRUD operations for products and variants
- **Category Management** - Organize products with categories
- **Order Management** - Process and track customer orders
- **Customer Management** - View and manage customer accounts
- **Coupon Management** - Create and manage discount coupons
- **Review Management** - Moderate customer reviews
- **Media Management** - Upload and manage product images (Cloudinary)
- **Data Export** - Export data to CSV format

## 🛠️ Tech Stack

### Frontend
- **Next.js 15** - React framework with App Router
- **React 19** - Latest React with concurrent features
- **Material-UI (MUI)** - Component library for consistent design
- **Radix UI** - Accessible UI primitives
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Beautiful icons
- **React Hook Form** - Form handling with validation
- **Zod** - Schema validation
- **Redux Toolkit** - State management
- **TanStack Query** - Server state management

### Backend & Database
- **Next.js API Routes** - Serverless API endpoints
- **MongoDB** - NoSQL database with Mongoose ODM
- **JWT (Jose)** - Authentication and authorization
- **bcryptjs** - Password hashing
- **Nodemailer** - Email sending functionality

### Integrations
- **Cloudinary** - Image upload and management
- **Razorpay** - Payment processing
- **Material React Table** - Advanced data tables
- **CKEditor 5** - Rich text editing
- **React Slick** - Image carousels

## 📋 Prerequisites

Before running this project, make sure you have:

- **Node.js** (v18 or higher)
- **npm** or **yarn** package manager
- **MongoDB** database (local or cloud)
- **Cloudinary** account for image management
- **Razorpay** account for payments

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone <repository-url>
cd E-Com
```

### 2. Install Dependencies
```bash
npm install
# or
yarn install
```

### 3. Environment Variables
Create a `.env.local` file in the root directory and add the following variables:

```env
# Database
MONGODB_URI=your_mongodb_connection_string

# JWT Secret
SECRET_KEY=your_jwt_secret_key

# Cloudinary
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# Razorpay
NEXT_PUBLIC_RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Email Configuration
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_app_password

# Base URL
NEXT_PUBLIC_BASE_URL=http://localhost:3000
```

### 4. Run the Development Server
```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

## 📁 Project Structure

```
E-Com/
├── app/                          # Next.js App Router
│   ├── (root)/                   # Route groups
│   │   ├── (admin)/             # Admin panel routes
│   │   │   └── admin/           # Admin dashboard pages
│   │   ├── (website)/           # Customer-facing routes
│   │   └── auth/                # Authentication pages
│   ├── api/                     # API routes
│   │   ├── auth/                # Authentication endpoints
│   │   ├── category/            # Category management
│   │   ├── product/             # Product management
│   │   ├── orders/              # Order management
│   │   └── ...                  # Other API endpoints
│   ├── globals.css              # Global styles
│   └── layout.jsx               # Root layout
├── components/                   # Reusable components
│   ├── Application/             # App-specific components
│   └── ui/                      # UI components (Radix/shadcn)
├── email/                       # Email templates
├── hooks/                       # Custom React hooks
├── lib/                         # Utility functions and configurations
│   └── column.js               # Data table column definitions
├── models/                      # MongoDB schemas
│   ├── User.model.js           # User schema
│   ├── Product.model.js        # Product schema
│   ├── Order.model.js          # Order schema
│   └── ...                     # Other models
├── public/                      # Static assets
├── routes/                      # Route constants
├── store/                       # Redux store configuration
├── middleware.js               # Next.js middleware for auth
├── next.config.mjs             # Next.js configuration
└── package.json                # Dependencies and scripts
```

## 🔐 Authentication & Authorization

The application uses JWT-based authentication with role-based access control:

- **Customers** - Access to shopping features and account management
- **Admins** - Full access to admin panel and management features

Authentication is handled via middleware that protects routes and redirects users based on their roles.

## 💾 Database Models

### Core Models
- **User** - Customer and admin accounts
- **Category** - Product categorization
- **Product** - Product information
- **ProductVariant** - Product variations (size, color, etc.)
- **Order** - Customer orders
- **Review** - Product reviews and ratings
- **Coupon** - Discount coupons
- **Media** - File uploads and management
- **Otp** - One-time passwords for verification

## 📊 Data Tables

The application includes advanced data tables with features like:
- Sorting and filtering
- Pagination
- Search functionality
- Export to CSV
- Custom cell renderers
- Responsive design

Table configurations are defined in `lib/column.js` for:
- Categories
- Products
- Product Variants
- Coupons
- Customers
- Reviews
- Orders

## 🎨 UI Components

Built with a combination of:
- **Material-UI** - Core component library
- **Radix UI** - Accessible primitives
- **Custom components** - Application-specific UI elements
- **Tailwind CSS** - Utility styling

## 🚀 Deployment

### Build for Production
```bash
npm run build
npm start
```

### Deployment Platforms
This application can be deployed on:
- **Vercel** (recommended for Next.js)
- **Netlify**
- **AWS**
- **DigitalOcean**
- Any platform supporting Node.js

## 📝 Scripts

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run lint` - Run ESLint

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support,[web](https://codeshow-lapz.web.app)  or create an issue in the repository.

## 🙏 Acknowledgments

- Next.js team for the amazing framework
- Material-UI team for the component library
- All open source contributors

---

**Happy Coding! 🚀** 
