# 🚀 Pro Backend Developer Code Files

> A comprehensive collection of real-world backend projects and modules built with Node.js — covering authentication, file handling, payments, social features, and e-commerce.

[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express.js-4.x-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Passport.js](https://img.shields.io/badge/Passport.js-Auth-34E27A?logo=passport&logoColor=white)](https://www.passportjs.org/)
[![Razorpay](https://img.shields.io/badge/Razorpay-Payments-02042B?logo=razorpay&logoColor=white)](https://razorpay.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

---

## 📁 Project Structure

```
pro-backend-developer/
├── formsandimages/         # Form handling & image upload with Multer
├── imagesT/                # Image processing & transformation
├── lcoauthsystem/          # Custom JWT-based authentication system
├── lcopassportgoogle/      # Google OAuth 2.0 with Passport.js
├── mydocslco/              # Document management system
├── razorpay/               # Razorpay payment gateway integration
├── socialapp/              # Social media app (posts, likes, follows)
├── tshirtstore/            # E-commerce store for T-shirts
└── README.md
```

---

## 📦 Modules Overview

### 📝 Forms & Images — `formsandimages/`

Handles HTML form submissions and file/image uploads using **Multer**.

**Key Features:**
- Multipart form data parsing
- Single & multiple file uploads
- File type and size validation
- Local & cloud storage support

```bash
cd formsandimages
npm install && npm start
```

---

### 🖼️ Images T — `imagesT/`

Image handling and transformation pipeline for processing uploaded media.

**Key Features:**
- Image resizing and compression
- Format conversion (JPEG, PNG, WebP)
- Sharp / Cloudinary integration
- On-the-fly image optimization

```bash
cd imagesT
npm install && npm start
```

---

### 🔐 LCO Auth System — `lcoauthsystem/`

A complete custom authentication system built from scratch using **JWT**.

**Key Features:**
- User registration & login
- JWT access & refresh tokens
- Password hashing with Bcrypt
- Protected route middleware
- Token expiry & logout handling

```bash
cd lcoauthsystem
npm install && npm start
```

**Environment Variables:**
```env
PORT=4000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
JWT_EXPIRY=1d
```

---

### 🔑 LCO Passport Google — `lcopassportgoogle/`

Google OAuth 2.0 login integration using **Passport.js**.

**Key Features:**
- Sign in with Google
- Session management with Express Session
- User profile retrieval from Google
- Callback URL handling

```bash
cd lcopassportgoogle
npm install && npm start
```

**Environment Variables:**
```env
PORT=4000
MONGO_URI=your_mongodb_connection_string
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
CALLBACK_URL=http://localhost:4000/auth/google/callback
SESSION_SECRET=your_session_secret
```

---

### 📄 My Docs LCO — `mydocslco/`

A document management system for uploading, storing, and retrieving user documents.

**Key Features:**
- Document upload & cloud storage
- User-specific document access
- File metadata tracking
- Download & delete support

```bash
cd mydocslco
npm install && npm start
```

---

### 💳 Razorpay — `razorpay/`

Full **Razorpay** payment gateway integration for processing orders and payments.

**Key Features:**
- Create & verify orders
- Razorpay Checkout integration
- Webhook handling for payment events
- Payment success/failure response handling

```bash
cd razorpay
npm install && npm start
```

**Environment Variables:**
```env
PORT=4000
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
```

---

### 👥 Social App — `socialapp/`

A backend for a social media platform with user interactions.

**Key Features:**
- User profiles & JWT authentication
- Create, edit & delete posts
- Like / unlike posts
- Follow & unfollow users
- Personalized feed generation

```bash
cd socialapp
npm install && npm start
```

**Environment Variables:**
```env
PORT=4000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

---

### 👕 T-Shirt Store — `tshirtstore/`

A full-featured e-commerce backend for an online T-shirt store.

**Key Features:**
- Product listing & admin management
- User authentication with role-based access (admin/user)
- Shopping cart & order management
- Razorpay payment integration
- Cloudinary image upload for products
- Email notifications via Nodemailer

```bash
cd tshirtstore
npm install && npm start
```

**Environment Variables:**
```env
PORT=4000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
JWT_EXPIRY=1d
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
SMTP_HOST=smtp.mailtrap.io
SMTP_PORT=2525
SMTP_USER=your_smtp_user
SMTP_PASS=your_smtp_pass
```

---

## 🛠️ Tech Stack

| Technology       | Purpose                               |
|------------------|---------------------------------------|
| Node.js          | Runtime environment                   |
| Express.js       | Web framework                         |
| MongoDB          | NoSQL database                        |
| Mongoose         | MongoDB ODM                           |
| JWT              | Token-based authentication            |
| Passport.js      | OAuth & authentication middleware     |
| Bcrypt           | Password hashing                      |
| Multer           | File & image upload handling          |
| Sharp            | Image processing & transformation     |
| Cloudinary       | Cloud media storage                   |
| Razorpay         | Payment gateway                       |
| Nodemailer       | Email notifications                   |
| Express Session  | Session management                    |
| Dotenv           | Environment variable management       |

---

## ⚙️ General Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/pro-backend-developer.git
cd pro-backend-developer
```

### 2. Navigate to Any Module

```bash
cd <module-name>
# example: cd tshirtstore
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

```bash
cp .env.example .env
# Edit .env and fill in the required values
```

### 5. Start the Server

```bash
# Development mode (with nodemon)
npm run dev

# Production mode
npm start
```

---

## 🔗 API Testing

Use [Postman](https://www.postman.com/) or [Thunder Client](https://www.thunderclient.com/) to test the REST APIs.

Each module may include a `postman_collection.json` file for quick import and testing.

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push to the branch: `git push origin feat/your-feature`
5. Open a Pull Request

---

## 📄 License

MIT © [Your Name](https://github.com/thenaveengautam)

---

<p align="center">
  Built with ❤️ to master backend development — one project at a time
</p>
