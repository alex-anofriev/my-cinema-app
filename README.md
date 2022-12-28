# Cinema service
Simple CRUD web service based on Spring Framework, that supports registration and authentication.

## Project structure
Project created on N-tier Architecture style and follows SOLID principles.
Provides:
- view layer: [cinema.controller](src/main/java/cinema/controller), [cinema.dto](src/main/java/cinema/dto)
- service layer: [cinema.model](src/main/java/cinema/model), [cinema.service](src/main/java/cinema/service)
- DAO layer: [cinema.dao](src/main/java/cinema/dao)

Spring configuration: [cinema.config](src/main/java/cinema/config)

#### Endpoints access
- ALL
    - POST: [/register](src/main/java/cinema/controller/AuthenticationController.java)
- USER/ADMIN
    - GET: [/cinema-halls](src/main/java/cinema/controller/CinemaHallController.java)
    - GET: [/movies](src/main/java/cinema/controller/MovieController.java)
    - GET: [/movie-sessions/available](src/main/java/cinema/controller/MovieSessionController.java)
- ADMIN
    - POST: [/cinema-halls](src/main/java/cinema/controller/CinemaHallController.java)
    - POST: [/movies](src/main/java/cinema/controller/MovieController.java)
    - POST: [/movie-sessions](src/main/java/cinema/controller/MovieSessionController.java)
    - PUT: [/movie-sessions/{id}](src/main/java/cinema/controller/MovieSessionController.java)
    - DELETE: [/movie-sessions/{id}](src/main/java/cinema/controller/MovieSessionController.java)
    - GET: [/users/by-email](src/main/java/cinema/controller/UserController.java)
- USER
    - GET: [/orders](src/main/java/cinema/controller/OrderController.java)
    - POST: [/orders/complete](src/main/java/cinema/controller/OrderController.java)
    - PUT: [/shopping-carts/movie-sessions](src/main/java/cinema/controller/ShoppingCartController.java)
    - GET: [/shopping-carts/by-user](src/main/java/cinema/controller/ShoppingCartController.java)
    - GET: [/users/by-email](src/main/java/cinema/controller/UserController.java)

## Technologies
- JDK 17
- Spring 5.3.20
- Spring Security 5.6.10
- Hibernate 5.6.14.Final
- MySql 8.0.31
- Tomcat 9.0.50

## How to start
- Fork to your repository and clone to your IDE
- Add your database properties to [db.properties](src/main/resources/db.properties)
- Install Apache Tomcat (application tested with 9.0.50 version)
- Install Postman or similar application to have access to HTTP methods
- Start application
- Credentials to login for ADMIN
    - email: admin@admin.ua
    - password: admin123
- Credentials to login for USER or use /register to create new user
    - email: user@user.ua
    - password: user1234
