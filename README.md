# 🖥️ Zin2bczin Computer Shop – Website Development Plan (B2C Model)

---

## ✅ 1. Project Planning

### Business Model:
- **B2C** (Selling computer hardware, accessories, and electronics directly to consumers).

### Target Audience:
- Gamers, tech enthusiasts, students, and professionals (age 15–40).

### Competitors:
- Daraz (Electronics Section)
- GT Store
- Czone
- Pakdukaan

### Core Features:
- ✔ **Product Catalog** (PC components, laptops, accessories)
- ✔ **Advanced Filters** (by category, price, brand, specs)
- ✔ **Shopping Cart & Wishlist**
- ✔ **Checkout with Payment Gateway (ABA PayWay / Bakong) & Cash on Delivery**
- ✔ **User Accounts (Login/Register)**
- ✔ **Admin Dashboard** (Manage products, orders, users, categories)
- ✔ **Order Tracking & History**
- ✔ **Product Comparison Tool** (for PC parts)

---

## 🔍 2. Requirement Analysis

### Feature List:
- ✅ User Authentication (JWT-based login/register)
- ✅ Product Management (CRUD operations for admin)
- ✅ Category & Brand Filters (CPU, GPU, RAM, Storage, etc.)
- ✅ Shopping Cart & Wishlist
- ✅ Checkout System (ABA PayWay + Bakong + Cash on Delivery)
- ✅ Order Tracking & History
- ✅ Admin Panel (Role-based access control)
- ✅ Product Comparison Tool (Compare specs side-by-side)

### Tech Stack:
| Layer       | Technology      |
|-------------|-----------------|
| Frontend    | HTML, CSS, JavaScript (Vanilla or React.js) |
| Backend     | Laravel (PHP)   |
| Database    | MySQL           |
| Hosting     | Shared Hosting (cPanel) |
| Design Tool | Figma (for UI/UX Design) |

---

## 🧩 3. Database Design (MySQL)

### Key Tables:
1. **Users** (id, name, email, password, role)
2. **Products** (id, name, price, specs, category_id, stock)
3. **Categories** (id, name, parent_category)
4. **Orders** (id, user_id, total, status, payment_method)
5. **Order_Items** (id, order_id, product_id, quantity)
6. **Cart_Items** (user_id, product_id, quantity)
7. **Wishlist** (user_id, product_id)
8. **Reviews** (user_id, product_id, rating, comment)
9. **Payments** (order_id, transaction_id, amount, status)

---

## 🎨 4. UI/UX Design

### Main Pages:
- Homepage (Featured products, deals, categories)
- Product Listing (Filters for components, brands, price)
- Product Details (Specs, images, reviews, "Add to Cart")
- Shopping Cart (Adjust quantities, proceed to checkout)
- Checkout Page (Payment options, address, order summary)
- User Account (Order history, wishlist, profile settings)
- Admin Dashboard (Manage products, orders, users)

### Design Style:
- Tech-themed UI (Dark mode option, neon accents)
- Responsive & Mobile-Friendly

---

## ⚛️ 5. Frontend Development

### Key Components:
- Navbar (Search bar, user account, cart icon)
- Product Grid (With filters for CPU, GPU, etc.)
- Product Comparison Tool (Side-by-side specs)
- Shopping Cart Page (Quantity adjust, remove items)
- Checkout Flow (Multi-step: Address → Payment → Confirm)
- Admin Panel UI (Tables for managing products/orders)

### Extras:
- ✔ Lazy Loading Images (Faster load times)
- ✔ Wishlist Animations (Heart icon toggle)
- ✔ Dark/Light Mode Toggle

---

## 🔧 6. Backend Development (Laravel)

### Core APIs:
- **Auth:** `POST /register`, `POST /login`
- **Products:** `GET /products`, `GET /products/{id}`
- **Cart:** `POST /cart`, `GET /cart`, `DELETE /cart/{id}`
- **Checkout:** `POST /checkout`
- **Orders:** `GET /orders/{userId}`, `POST /orders`
- **Admin:** `GET /admin/products`, `POST /admin/products`

### Security:
- JWT Authentication
- Rate Limiting (Prevent brute force attacks)
- Role-Based Access Control (Admin vs. User)

### Extras:
- Email Notifications (Order confirmations via SendGrid)

---

## 💳 7. Payment Integration

### Payment Methods:
1. **ABA PayWay** (Visa, MasterCard, Local Bank Payments)
2. **Bakong** (Mobile Wallet Payment in Cambodia)
3. **Cash on Delivery** (Pay when product arrives)

### Steps:
- Set up **ABA PayWay API** for secure payments
- Integrate **Bakong Gateway** (via Cambodian NBC guidelines)
- Implement **Cash on Delivery** option

---

## 🧪 8. Testing

### Frontend:
- Responsive Testing (Chrome DevTools)
- Unit Tests (Jest)

### Backend:
- API Testing (Postman)
- Unit Tests (PHPUnit)

### Security Testing:
- OWASP Checks (XSS, CSRF, SQL Injection)

---

## 🚀 9. Deployment

| Component   | Platform        |
|-------------|-----------------|
| Frontend    | Vercel / Netlify |
| Backend     | Shared Hosting (cPanel) |
| Database    | MySQL via cPanel |
| Domain      | Custom domain (e.g., `zin2bczin.com`) |
| SSL         | Let’s Encrypt (Free HTTPS) |

---

## 📈 10. Launch & Monitor

- Google Analytics (Track user behavior)
- Error Monitoring (Sentry / LogRocket)

### Post-Launch Checklist:
- ✅ Mobile Testing
- ✅ SEO Optimization
- ✅ Load Testing (k6 or JMeter)

---

## 🧰 Typical Features of B2C E-commerce Sites

- User Registration & Login
- Product Listings with Filters
- Shopping Cart and Checkout
- Order Management
- Customer Reviews
- Email Notifications
- Responsive Design
- Search Functionality
- Wishlist & Save for Later
- Promotional Banners / Discounts

---

## 🧪 Example Stack Summary

| Layer           | Stack                                  |
|------------------|----------------------------------------|
| Frontend         | HTML/CSS/JS or React.js                |
| Backend          | Laravel (PHP Framework)                |
| Auth             | JWT-based Authentication               |
| Payments         | ABA PayWay, Bakong, COD                |
| Database         | MySQL                                  |
| Dev Tools        | Figma (Design), Postman (API Test), PHPUnit |
| Hosting          | Vercel/Netlify (Frontend), cPanel (Backend) |
| Monitoring       | Google Analytics, LogRocket, Sentry    |

---

