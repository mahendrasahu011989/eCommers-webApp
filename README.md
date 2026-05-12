# eCommers-webApp
Full-stack e-commerce web application built with React, FastAPI, and JWT authentication, featuring product catalog, cart, order management, and secure payment integration.

# 🚀 E-commerce Web Application (React + FastAPI)

A full-stack e-commerce web application built with **React (Vite + Tailwind CSS)** and **FastAPI**, featuring secure authentication, product management, cart & checkout flow, and payment integration.

Designed with a **scalable architecture**, clean separation of concerns, and production-ready practices.

---

## 📌 Features

### 🛍️ User Features

* User registration & login (JWT-based authentication)
* Browse products with search, category, and price filters
* Product details page with variants (size, weight, etc.)
* Add to cart & persistent cart handling
* Checkout flow with:

  * Address management
  * Multiple payment methods (Razorpay integration)
* Order placement & order history
* Order tracking with status timeline

---

### 🛠️ Admin Features

* Admin dashboard
* Product management (CRUD)
* Category & subcategory management
* Variant management (size, weight, price)
* Order management & status updates
* User management

---

### 🔐 Security Features

* JWT-based authentication
* Role-based access control (Admin/User)
* Secure API validation (FastAPI + Pydantic)
* Payment signature verification (Razorpay HMAC)
* Environment-based configuration (.env)

---

## 🏗️ Tech Stack

### Frontend

* ReactJS (Vite)
* Tailwind CSS
* Axios
* React Router

### Backend

* FastAPI (Python)
* SQLAlchemy (ORM)
* Pydantic (Validation)
* JWT Authentication

### Database

* SQLite (development)
* PostgreSQL (production-ready)

### DevOps / Tools

* Docker (optional)
* Git & GitHub
* Razorpay (Payment Gateway)

---

## 📂 Project Structure

```
ecommerce-webapp/
│
├── frontend/                # React App
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/       # API calls
│   │   ├── context/        # Auth & state
│   │   └── App.jsx
│
├── backend/                # FastAPI App
│   ├── app/
│   │   ├── api/
│   │   ├── models/
│   │   ├── schemas/
│   │   ├── services/
│   │   ├── core/
│   │   └── main.py
│
├── .env.example
├── README.md
└── requirements.txt
```

---

## ⚙️ Setup & Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/ecommerce-webapp.git
cd ecommerce-webapp
```

---

### 2️⃣ Backend Setup (FastAPI)

```bash
cd backend
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

Create `.env` file:

```env
DATABASE_URL=sqlite:///./test.db
SECRET_KEY=your_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

RAZORPAY_KEY_ID=your_key
RAZORPAY_KEY_SECRET=your_secret
```

Run backend:

```bash
uvicorn app.main:app --reload
```

---

### 3️⃣ Frontend Setup (React)

```bash
cd frontend
npm install
npm run dev
```

---

## 🔐 Authentication Flow

* Login returns JWT token
* Token is used for protected API calls
* Role-based access control for admin routes

---

## 💳 Payment Integration (Razorpay)

* Order is created from backend
* Payment verified using HMAC-SHA256 signature
* Ensures secure transaction validation

---

## 📦 API Highlights

* `/auth/login` – User authentication
* `/products` – Product listing
* `/cart` – Cart operations
* `/orders` – Order placement
* `/admin/*` – Admin operations

---

## 📈 Future Enhancements

* Coupon & discount system
* Real-time order tracking (courier API)
* Pincode-based shipping calculation
* Recommendation engine (AI-based)
* Microservices architecture

---

## 🧪 Testing

* Unit testing with pytest (backend)
* API testing via Postman / Swagger UI

---

## 🧑‍💻 Author

**Mahendra Sahu**
Senior Java & Workflow Automation Engineer

* Expertise: Camunda 8, Microservices, Backend Systems
* Email: [sahu.mahendra0101@gmail.com](mailto:sahu.mahendra0101@gmail.com)

---

## ⭐ Contribution

Feel free to fork, raise issues, and submit pull requests.

---

## 📜 License

This project is licensed under the MIT License.

---

## 💡 Notes

* This project is designed for **learning + production-ready architecture**
* Can be extended into a scalable enterprise-grade system
