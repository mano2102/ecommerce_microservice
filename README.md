# E-commerce Microservices Architecture

## Overview
This project is a fully functional **E-commerce application** where users can browse products, add them to a cart, place orders, process payments, and track deliveries. Each functionality is handled by an independent microservice, communicating via an event-driven architecture.

## Microservices and Their Responsibilities

| Microservice        | Responsibilities |
|--------------------|----------------|
| **API Gateway**     | Entry point for all requests, routing, authentication, and rate limiting. |
| **User Service**    | Manages user registration, login, authentication, and authorization. |
| **Product Service** | Manages products, categories, and inventory. |
| **Cart Service**    | Handles user carts, adding/removing products, and updating quantities. |
| **Order Service**   | Manages order placement, tracking, and history. |
| **Payment Service** | Processes payments using third-party providers (e.g., Stripe, Razorpay, PayPal). |
| **Shipping Service** | Handles order shipment, tracking, and delivery notifications. |
| **Notification Service** | Sends emails, SMS, and push notifications for order updates. |
| **Review & Rating Service** | Manages customer reviews and product ratings. |
| **Admin Service** | Provides an admin dashboard for managing users, products, orders, etc. |
| **Analytics Service** | Tracks sales, user behavior, and generates reports. |

## Technologies and Tools Used
- **Spring Boot** (For developing all microservices)
- **Spring Cloud Gateway** (For API Gateway)
- **Spring Security & JWT** (For authentication & authorization)
- **Eureka Server (Netflix Eureka)** (For service discovery)
- **Feign Client & RestTemplate** (For service-to-service communication)
- **RabbitMQ / Apache Kafka** (For event-driven communication)
- **MySQL / PostgreSQL / MongoDB** (For databases)
- **Redis** (For caching frequently accessed data)
- **ELK Stack (Elasticsearch, Logstash, Kibana) / Prometheus & Grafana** (For logging, monitoring, and observability)
- **Docker & Kubernetes** (For containerization and orchestration)
- **CI/CD using Jenkins / GitHub Actions** (For automated deployment)

## Microservices Concepts Covered
✅ **API Gateway** - Centralized routing and authentication  
✅ **Service Discovery** - Registering and discovering services dynamically  
✅ **Load Balancing** - Using Ribbon or Kubernetes Load Balancer  
✅ **Event-Driven Architecture** - Using Kafka/RabbitMQ for async communication  
✅ **Distributed Logging & Monitoring** - ELK Stack, Prometheus & Grafana  
✅ **Database Per Service** - Using different databases for different services  
✅ **Circuit Breaker & Resilience** - Using Resilience4j or Hystrix for fault tolerance  
✅ **Caching** - Implementing Redis for performance optimization  
✅ **Containerization & Deployment** - Using Docker & Kubernetes  

## Additional Enhancements
- **Rate Limiting & Throttling** (To prevent DDoS attacks)
- **Distributed Transactions** (Using SAGA pattern with Kafka)
- **Automated Testing** (Using JUnit, Testcontainers, and WireMock for API testing)
- **GraphQL API** (For efficient data fetching)

## Architecture Diagram
### Request Flow Example:
1. A user logs in via **API Gateway**, which routes the request to the **User Service**.
2. The user browses products from the **Product Service**.
3. Adds items to the cart via **Cart Service**.
4. Places an order, triggering an event in **Order Service**.
5. **Payment Service** processes the payment.
6. **Shipping Service** handles delivery.
7. **Notification Service** sends updates via email/SMS.

## Why This Project?
✔ **Real-world use case** covering almost all microservices concepts.  
✔ **Scalable** - Can handle millions of users by adding more instances.  
✔ **Modular** - Each service can be developed, deployed, and scaled independently.  
✔ **Perfect for learning & portfolio** - Demonstrates expertise in microservices.  

## Getting Started
To set up and run the project locally:
1. Clone the repository:
   ```sh
   git clone https://github.com/mano2102/dsa.git
   ```
2. Navigate to the project folder and build the services:
   ```sh
   cd e-commerce-microservices
   mvn clean install
   ```
3. Start dependent services (Kafka, Eureka, MySQL, Redis) using Docker Compose:
   ```sh
   docker-compose up -d
   ```
4. Start individual microservices:
   ```sh
   mvn spring-boot:run
   ```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

---
### 🚀 Happy Coding! 🎯
