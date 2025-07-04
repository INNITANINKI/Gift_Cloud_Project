
# 🎁 Gift Cloud - Gifty Delivery System

## 📝 Project Overview

**Gift Cloud** is a Spring Boot-based RESTful web service designed to streamline the gift ordering and delivery process. It enables users to register, manage profiles, browse and order gifts, and track deliveries. This system allows scheduled deliveries and provides a structured admin/user view of operations like adding gifts and placing orders.

## 🚀 Technologies Used

- **Java 17**
- **Spring Boot**
- **Spring MVC**
- **Spring Data JPA**
- **MySQL**
- **Lombok**
- **Postman** (for API testing)
- **Maven**

## 📦 Key Features

- 🔐 **User Registration and Authentication**  
- 🎁 **Gift Management** (CRUD operations)
- 📦 **Order Placement and Delivery Management**
- 🕐 **Scheduled Deliveries Support (Can be extended with Quartz/Scheduler)**
- 📋 **Order Tracking by ID**

## 📂 Project Structure

```
gifty-delivery-system-full/
├── controller/          # Handles API endpoints
├── model/               # Entity classes (User, Gift, Order)
├── repository/          # JPA repositories
├── service/             # Business logic
├── dto/                 # Data transfer objects (optional)
├── util/                # Utility functions (if used)
├── application.properties
└── GiftyDeliverySystemApplication.java
```

## 🛠️ REST API Endpoints

Here are the main APIs available (use Postman to test):

### 👤 User Module

| Operation           | Method | Endpoint                                |
|---------------------|--------|-----------------------------------------|
| Register User       | POST   | `/api/users/register`                   |
| Get All Users       | GET    | `/api/users/all`                        |
| Login               | POST   | `/api/users/login`                      |
| Update User         | PUT    | `/api/users/{id}`                       |
| Get User by ID      | GET    | `/api/users/{id}`                       |

### 🎁 Gift Module

| Operation           | Method | Endpoint                                |
|---------------------|--------|-----------------------------------------|
| Add Gift            | POST   | `/api/gifts`                            |
| View All Gifts      | GET    | `/api/gifts`                            |
| Update Gift         | PUT    | `/api/gifts/{id}`                       |
| Get Gift by ID      | GET    | `/api/gifts/{id}`                       |
| Delete Gift by ID   | DELETE | `/api/gifts/{id}`                       |

### 📦 Order Module

| Operation              | Method | Endpoint                                |
|------------------------|--------|-----------------------------------------|
| Place Order            | POST   | `/api/orders`                           |
| View All Orders        | GET    | `/api/orders`                           |
| Deliver Order          | PUT    | `/api/orders/deliver/{id}`              |
| Check Order Status     | GET    | `/api/orders/status/{id}`               |

## 💻 How to Run the Project

1. **Clone the repository**  
   ```bash
   git clone https://github.com/INNITANINKI/Gift_Cloud_Project.git
   cd gifty-delivery-system-full
   ```

2. **Set up MySQL database**  
   Create a database named `gifty_delivery` (or update the name in `application.properties`).

3. **Configure DB Credentials**  
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/gifty_delivery
   spring.datasource.username=root
   spring.datasource.password=yourpassword
   ```

4. **Build and Run the Project**  
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

5. **Access the APIs**  
   Base URL: `http://localhost:9999/api/`

## 🧪 Postman Collection

Use the above endpoints in Postman to test functionality. Sample flows:

- Register → Login → Add Gifts → Place Order → Deliver Order → Check Status

## 📌 Future Scope

- 📅 Add gift delivery scheduler (Quartz)
- 📬 Email notifications on order placement
- 📈 Admin dashboard for order and delivery stats
- 📦 Integration with third-party delivery APIs

