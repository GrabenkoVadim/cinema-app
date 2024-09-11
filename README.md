# <p>Cinema app </p>
# 🎥 About cinema-app
This project is simple analog of cinema application with authentication and authorization.

The application's key advantage is its role-based access control, ensuring secure and streamlined functionality for both administrators and regular users. It offers a user-friendly interface, efficient data management, and smooth navigation, making it ideal for managing a cinema's operations and customer interactions.
# Features

![alt text](https://github.com/mate-academy/hibernate-order-hw/raw/master/Hibernate_Cinema_Uml.png)
The application has the ability:
- Register new user
- Cinema hall add or get all
- Add a movie or get all
- Movie session add, find by date, update or delete
- Complete the order or get the order story
- Add a shopping cart, get a shopping cart for the user
- Find user by email

    There are two types of roles in the application: `ADMIN` and `USER`. </br>
During registration, the user is assigned a role USER.

###### All configured endpoints you can use for ADMIN or USER
- POST: /register - all
- GET: /cinema-halls - user/admin
- POST: /cinema-halls - admin
- GET: /movies - user/admin
- POST: /movies - admin
- GET: /movie-sessions/available - user/admin
- POST: /movie-sessions - admin
- PUT: /movie-sessions/{id} - admin
- DELETE: /movie-sessions/{id} - admin
- GET: /users/by-email - admin
- PUT: /shopping-carts/movie-sessions - user
- GET: /shopping-carts/by-user - user
- GET: /orders - user
- POST: /orders/complete - user
# Technologies💻:
- Java 11
- Hibernate
- Spring Framework
- Spring Security
- Spring Web
- REST
- MySQL
- Apache Tomcat 9.0.54

### How to run project:
1. To have or install MySQL and Apache Tomcat 9.0.50
2. Clone this project
3. Configure db.Properties file from resources directory to create connection to db:
- db.driver=com.mysql.cj.jdbc.Driver
- db.url=YOUR_URL
- db.user=YOUR_LOGIN
- db.password=YOUR_PASSWORD
4. Add Tomcat to the running configuration of your project and use Tomcat application context.
After all these steps you will be able to run this project locally.
Then you can log in with :
ADMIN role:
- username - admin@i.ua
- password - 1234

USER role:
- username - user@i.ua
- password - 1234
