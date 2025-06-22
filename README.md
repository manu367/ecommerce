# 🛒 E-Commerce Application
An end-to-end full stack **E-commerce Web Application** built using modern technologies. This app allows users to browse products, add to cart, purchase items, and manage their orders — just like a real-world online store.

## 📌 Features
- 👤 **User Authentication & Authorization** (JWT-based)
- 🛍️ **Product Browsing** with categories, filters, and search
- 🛒 **Shopping Cart** with quantity adjustments
- 💳 **Checkout & Payment** (Mock or real via Razorpay/Stripe)
- 📦 **Order Tracking** and order history
- 🔒 **Admin Panel** for product & order management
- 🧾 **Invoice generation** (optional)
- 📊 **Analytics Dashboard** (for admin)
- 🌐 Responsive UI (Mobile + Desktop)

- ---

## 🛠️ Tech Stack
**Frontend** : HTML , Tailwind css , javascript , React , Redux toolkit , Axio
**Backend** : Spring Boot , Spring JPA , Spring Secuirty , Spring Kafka , Spring Redis , Spring Session
**Database** : MySQL , PostgreSQL , Firebase , Redis
**Tools and Libaries** : Tenserflow (Machine Learning ) , Dotenv , Razorpay , Cloudinary , JWT , Postman , kafka , Docker , 

---

## 🧩 Folder Structure
**ecommerce**
  **controller**
    AuthController
    UserController
    HomeController
    ProductController
    OrderController
    PaymentController
    TrackingController
    ProfileController
    DeviceController
    WiseListController
    UIControllder
    SaleController
    AnalysisController
    AdminControll
    SettingController
  **model**
    UserModel
    ProductModel
    QueryModel
    ProductExtendModel
    UIModel
    SalesModel
    OrderModel
    PaymentModel
  **request**
  **response**
  **filter**
     AuthFilter
     CSRFFilter
     OptimizationController
     
  security
     ProductSecurity
     AdminSecurity
     PaymentSecurity
     ResourseSecurity
     
  kafka
    ProductListner
    Reciverproduct
    OrderSubscriber
  
  session
     UserSession
  repo
    Userepo
  service
  serviceimpl
  util




## ⚙️ How to Install Locally

### Prerequisites

-  Java installed and set path of java
- MongoDB installed and running locally OR MongoDB Atlas URI
- Docker install and setup
- Kafka install setup
- Redis install and setup also from youtube
- Git installed


### 🔽 Clone the Repository

```bash
git clone https://github.com/your-username/ecommerce-app.git
cd ecommerce-app

cd backend
in cmd code .

### **MongoDB Schema Overview**
```
Users
{
  name: String,
  email: String,
  password: String (hashed),
  role: "user" | "admin",
  cart: [productId, quantity],
  orders: [orderId]
}

Products
```
{
  name: String,
  description: String,
  price: Number,
  category: String,
  images: [URL],
  stock: Number
}

Orders
```{
  userId: ObjectId,
  products: [{ productId, quantity }],
  totalAmount: Number,
  paymentStatus: "pending" | "paid",
  deliveryStatus: "processing" | "shipped" | "delivered",
  timestamp: Date
}

Backend Functionality (API Routes)
📌 Authentication
POST /api/auth/register — Register user

POST /api/auth/login — Login and return JWT

📦 Product Management
GET /api/products — Get all products

GET /api/products/:id — Get product by ID

POST /api/products — (Admin) Add new product

PUT /api/products/:id — (Admin) Update product

DELETE /api/products/:id — (Admin) Delete product

🛒 Cart & Orders
POST /api/cart — Add to cart

GET /api/cart — View cart

DELETE /api/cart/:productId — Remove item from cart

POST /api/orders — Create order

GET /api/orders — View user's orders

GET /api/admin/orders — (Admin) View all orders

🛡️ Middleware
authMiddleware.js — Verifies JWT

adminMiddleware.js — Restricts route to admin only

🧪 Testing APIs
Use Postman to test:

JWT-protected routes (add token in headers)

CRUD operations for product

User login/registration flow


![image](https://github.com/user-attachments/assets/f571ca75-c096-449c-841c-13018220f25f)
![image](https://github.com/user-attachments/assets/9490dff6-4b06-4890-8d40-70dbbf7d8370)
![image](https://github.com/user-attachments/assets/9772444b-eada-4326-a159-88ab3207e727)
![image](https://github.com/user-attachments/assets/04d95419-d446-40a8-9244-3621abc9b9f1)
![image](https://github.com/user-attachments/assets/5537e609-328d-4306-83a4-09d34b2780bd)


### Future Enhancements
Add product reviews & ratings
Integrate real-time notifications (via WebSocket)
AI-based recommendation engine
Coupons & discounts module
Multi-vendor support
















