<div align="center">
  <h1>🛍️ HiTeckKart E-Commerce Platform</h1>
  <p>A Full-Stack E-Commerce Application showcasing the power of a decoupled Spring Boot backend and dynamic React frontend.</p>
</div>

---

## 📖 Problem Statement

In today's digital landscape, businesses face the persistent challenge of providing lightning-fast, highly responsive user experiences while securely managing heavy transactional data and inventory. 

**HiTeckKart** bridges this gap. It serves as a comprehensive, scalable solution demonstrating how to decouple a user-friendly frontend (React) from a secure, data-intensive backend (Java/Spring Boot). This architecture solves the problem of tight coupling, allowing frontend developers and backend engineers to scale, test, and iterate on their environments independently without breaking the storefront.

## ✨ Key Features

- **Dynamic Product Catalog:** View products dynamically rendered in a responsive grid.
- **Inventory Management:** Live tracking of stock availability. Items dynamically disable themselves when "Out of Stock."
- **Full Shopping Cart:** Add products, adjust quantities safely (constrained by maximum stock availability), and see real-time price totals.
- **Advanced File Handling:** Securely upload, store, and fetch image binaries (`byte[]`) directly stored within the database.
- **Search & Filtering:** Instantly filter products by category or keyword using the responsive top navigation bar.

## 🛠️ Technology Stack

### Front-End (The Storefront)
- **Framework:** React.js (Vite)
- **Styling:** Bootstrap 5 & Custom CSS
- **Routing:** React Router DOM
- **API Client:** Axios

### Back-End (The Engine)
- **Framework:** Spring Boot 2.7.x (Java SDK 8)
- **Database:** H2 In-Memory Database (Zero-configuration required!)
- **ORM:** Spring Data JPA / Hibernate
- **Server:** Apache Tomcat (Embedded)

---

## 🚀 Getting Started (Run Locally)

One of the best features of this project is its **Zero-Configuration Backend**. Because we use an in-memory H2 database, you do not need to install MySQL, PostgreSQL, or initialize any external server. 

### 1. Start the Java Backend
Open a terminal, navigate into the Backend directory, and use the included Maven wrapper to start the server. It is configured to run on a safe port (`8085`) to avoid unexpected collisions.

```bash
cd Ecommerce-Backend
./mvnw spring-boot:run
```
*(The backend is now live and listening at `http://localhost:8085`)*

### 2. Start the React Frontend
Open a **new, split terminal**, install the node dependencies, and start the Vite development server.

```bash
cd Ecommerce-Frontend
npm install
npm run dev
```

### 3. Open the Shop
Click the link provided in your frontend terminal (typically `http://localhost:5173`) to open your beautiful new storefront in the browser!

---

## 📡 REST API Architecture

| HTTP Method | Endpoint | Description |
| --- | --- | --- |
| **GET** | `/api/products` | Retrieves a complete list of all products |
| **GET** | `/api/product/{id}` | Retrieves details for a specific product |
| **GET** | `/api/product/{id}/image`| Streams the raw binary image data for frontend rendering |
| **GET** | `/api/products/search` | Dynamic keyword and category search |
| **POST** | `/api/product` | Securely uploads a new product along with 'multipart/form-data' image |
| **PUT** | `/api/product/{id}` | Updates existing product details and stock |
| **DELETE**| `/api/product/{id}` | Removes a product completely from the inventory |

## 🤝 Contribution & License
This project is open-source and intended for educational demonstration purposes. Feel free to fork, clone, and build upon it!
