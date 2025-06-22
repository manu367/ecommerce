# 🛒 E-Commerce Application

An end-to-end full stack **E-commerce Web Application** built using modern technologies.  
This app allows users to **browse products, add to cart, purchase items, and manage their orders** — just like a real-world online store.

---

## 📌 Features

- 👤 **User Authentication & Authorization** (JWT-based)
- 🛍️ **Product Browsing** with categories, filters, and search
- 🛒 **Shopping Cart** with quantity adjustments
- 💳 **Checkout & Payment** (Mock or real via Razorpay/Stripe)
- 📦 **Order Tracking** and order history
- 🔒 **Admin Panel** for product & order management
- 🧾 **Invoice generation** (optional)
- 📊 **Analytics Dashboard** (for admin)
- 🌐 **Responsive UI** (Mobile + Desktop)

---

![image](https://github.com/user-attachments/assets/f571ca75-c096-449c-841c-13018220f25f)
![image](https://github.com/user-attachments/assets/9490dff6-4b06-4890-8d40-70dbbf7d8370)
![image](https://github.com/user-attachments/assets/9772444b-eada-4326-a159-88ab3207e727)
![image](https://github.com/user-attachments/assets/04d95419-d446-40a8-9244-3621abc9b9f1)
![image](https://github.com/user-attachments/assets/5537e609-328d-4306-83a4-09d34b2780bd)

## 🛠️ Tech Stack

- **Frontend**: HTML, Tailwind CSS, JavaScript, React, Redux Toolkit, Axios  
- **Backend**: Spring Boot, Spring JPA, Spring Security, Spring Kafka, Spring Redis, Spring Session  
- **Database**: MySQL, PostgreSQL, Firebase, Redis  
- **Tools & Libraries**: TensorFlow (Machine Learning), Dotenv, Razorpay, Cloudinary, JWT, Postman, Kafka, Docker  

---

## 🧩 Folder Structure

ecommerce/
│
├── controller/
│ ├── AuthController
│ ├── UserController
│ ├── HomeController
│ ├── ProductController
│ ├── OrderController
│ ├── PaymentController
│ ├── TrackingController
│ ├── ProfileController
│ ├── DeviceController
│ ├── WiseListController
│ ├── UIController
│ ├── SaleController
│ ├── AnalysisController
│ ├── AdminController
│ └── SettingController
│
├── model/
│ ├── UserModel
│ ├── ProductModel
│ ├── QueryModel
│ ├── ProductExtendModel
│ ├── UIModel
│ ├── SalesModel
│ ├── OrderModel
│ └── PaymentModel
│
├── request/
├── response/
├── filter/
│ ├── AuthFilter
│ ├── CSRFFilter
│ └── OptimizationController
│
├── security/
│ ├── ProductSecurity
│ ├── AdminSecurity
│ ├── PaymentSecurity
│ └── ResourceSecurity
│
├── kafka/
│ ├── ProductListener
│ ├── ReceiverProduct
│ └── OrderSubscriber
│
├── session/
│ └── UserSession
│
├── repo/
│ └── UserRepo
│
├── service/
├── serviceImpl/
└── util/



---

## ⚙️ How to Install Locally

### 🧾 Prerequisites

- ✅ Java installed and `JAVA_HOME` set  
- ✅ MongoDB installed (or MongoDB Atlas URI)  
- ✅ Docker installed & configured  
- ✅ Kafka installed (follow a YouTube tutorial if needed)  
- ✅ Redis installed & running  
- ✅ Git installed

---

### 🔽 Clone the Repository

```bash
git clone https://github.com/your-username/ecommerce-app.git
cd ecommerce-app



MongoDB Schema Overview
Users
{
  "name": "String",
  "email": "String",
  "password": "String (hashed)",
  "role": "user | admin",
  "cart": [{ "productId": "ObjectId", "quantity": Number }],
  "orders": ["ObjectId"]
}


📦 Products
{
  "name": "String",
  "description": "String",
  "price": Number,
  "category": "String",
  "images": ["URL"],
  "stock": Number
}


Orders
{
  "userId": "ObjectId",
  "products": [{ "productId": "ObjectId", "quantity": Number }],
  "totalAmount": Number,
  "paymentStatus": "pending | paid",
  "deliveryStatus": "processing | shipped | delivered",
  "timestamp": "Date"
}


Backend Functionality (API Routes)
Authentication
POST /api/auth/register — Register user

POST /api/auth/login — Login and return JWT

📦 Product Management
GET /api/products — Get all products

GET /api/products/:id — Get product by ID

POST /api/products — (Admin) Add product

PUT /api/products/:id — (Admin) Update product

DELETE /api/products/:id — (Admin) Delete product

🛒 Cart & Orders
POST /api/cart — Add to cart

GET /api/cart — View cart

DELETE /api/cart/:productId — Remove from cart

POST /api/orders — Create order

GET /api/orders — View user orders

GET /api/admin/orders — (Admin) View all orders

🛡️ Middleware
authMiddleware.js — Verifies JWT token

adminMiddleware.js — Restricts route to admin only

🧪 API Testing
Use Postman to test:

🔐 JWT-protected routes (add token in headers)

📦 CRUD operations for product

👤 User login/registration flow

Future Enhancements
⭐ Product reviews & ratings

📩 Real-time notifications (WebSocket)

🧠 AI-based recommendation engine

🎟️ Coupons & discount support

🛒 Multi-vendor functionality








### ✅ To-Do for You:
1. Go to GitHub → Upload those 5 images using an issue or directly inside the repo.
2. Replace all the `https://raw.githubusercontent.com/...` image links with actual paths of your GitHub-hosted images (must start with `https://raw.githubusercontent.com/...`).
3. Push this `README.md` inside your GitHub repo root.

Bhai ab yeh `README.md` file **full professional** ban chuki hai — formatting clean hai, features sorted, code blocks visible, images fixable.

Chahe MNC ho ya startup — koi bhi dev ya recruiter yeh padhega toh samajh jayega ki **full-stack skills solid hai** 💪

Agar chahe toh main tera GitHub pe repo bhi polish karwa du — bol de bas.
















