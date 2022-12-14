# [Cinema-App]

Web application with WEB part which implements work of the cinema-app
using Java, Hibernate and Spring. Based on 3-layer architecture (dao, service, controller).

__The purpose of the project:__ application is intended for use by administrators of cinemas and their visitors.
The project gives ability for visitors: to add ticket to their shopping cart and to complete it, for administrators:
to add, change and delete movie sessions, halls and movies, for all: authentication and authorization.
## Functionality
#### __ALL__
- __Registration and authorization__ `POST: /register` `GET: /login`
- __Logout__ `GET: /logout`
#### __ADMIN__
- __GET:__
    - cinema halls `GET: /cinema-halls`
    - movies `GET: /movies`
    - available movie sessions `GET: /movie-sessions/available`
    - some specific movie session `GET: /movie-sessions/{id}`
    - user by email `GET: /users/by-email`
- __POST:__
    - cinema halls `POST: /cinema-halls`
    - movies `POST: /movies`
    - movie sessions `POST: /movie-sessions`
- __PUT:__
    - movie session `PUT: /movie-sessions/{id}`
- __DELETE:__
    - movie session `DELETE: /movie-sessions/{id}`
    
#### __USER__
- __GET:__
    - cinema halls `GET: /cinema-halls`
    - movies `GET: /movies`
    - available movie sessions `GET: /movie-sessions/available`
    - some specific movie session `GET: /movie-sessions/{id}`
    - orders `GET: /orders`
    - shopping carts by user `GET: /shopping-carts/by-user`
- __POST:__
    - orders `POST: /orders/complete`
- __PUT:__
    - tickets to shopping cart for some movie session `PUT: /shopping-carts/movie-sessions`

## Technologies
- Java 11
- Hibernate
- Spring Core, Web MVC, ORM, Security
- REST
- MySQL
- Apache Tomcat - version 9.0.50
- Apache Maven - version 3.8.5
- Git
## DB relations structure
![pic](src/main/resources/images/cinema-app.png)
## Setup

  1. Install Apache Tomcat - version 9.0.50 
  2. Install MySQL - version 8.0.22 
  3. Clone project to your IDE.
  4. Create schema in MySQL. 
  5. Add DB configurations in:
  `src/main/resources/db.properties`.
