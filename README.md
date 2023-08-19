
![Logo](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/bg-masthead.jpg?raw=true)


# Saint Louis Farms

Final project for LaunchCode's 2023 Liftoff Program.

Saint Louis Farms is a full-stack web application that enables farmers to sell their products directly to consumers.

The application was designed with three types of users in mind: farmers, clients, and non-authenticated users.

Farmers have the ability to set up a store. They can manage their inventory by uploading, deleting, and updating items. Farmers can customize their store settings according to their needs. They have access to a dashboard that provides real-time updates on past and current orders well as a customizable farmer profile. Two different product views are available for farmers: a condensed table view for inventory management and a store preview option that allows them to see how products will appear for clients.

Clients can conveniently place orders from farms using a shopping cart feature. They can also track the live status of their orders in through three stages: unconfirmed, confirmed, and fulfilled. The system will automatically adjust the inventory of ordered items to ensure availability. Additionally, clients have access to a comprehensive order history log where they can review all of their purchases.

Non-authenticated users are able to browse all farms but cannot place orders. Any attempt made by non-authenticated users to perform actions other than viewing farms or stores will be redirected to the login page.

## Authors

- [Jood Alzqaili (@Jzkili)](https://github.com/Jzkili)
- [Maisa Salahaldin (@MaisaSalahaldin)](https://github.com/MaisaSalahaldin)
- [Tudor Seserman (@tudor-seserman)](https://github.com/tudor-seserman)
- [Mike Wilson (@MikeWilsonSTL)](https://www.github.com/MikeWilsonSTL)


## Features

- Full CRUD database operations (Create, Read, Update, Delete)
- User authentication with password hashing
- Custom measurements and product types for farmers
- Quick Edit and Full Edit functionality for farmer products
- Image processing for products and farmer profiles
- Product search feature in both farmer product views
- Dynamic shopping cart that displays each item
- Order processing - the ability to pull ordered items from inventory, confirm orders, fulfill orders
- Order logging - the ability for both farmers and clients to review the details of all orders
- State-driven navbar that changes according to the type of user (farmer, client, or non-authenticated)
## Tech Stack

**Front-end:** Bootstrap, JavaScript, Nerd Fonts

**Back-end:** Java, Spring Boot, Thymeleaf, MySQL, Hibernate

## Run Locally 
### Note: This project requires Java 11 

1. Install [MySQL Workbench](https://dev.mysql.com/downloads/workbench/) and 
[create a new MySQL connection](https://dev.mysql.com/doc/workbench/en/wb-getting-started-tutorial-create-connection.html).


2. Right-click and save this [demo database](https://raw.githubusercontent.com/kim-n-lee/saintlouisfarms/main/src/main/resources/demo-database/saintlouisfarms-data.sql).


3.  [Import the demo database](https://help.umbler.com/hc/en-us/articles/202385865-MySQL-Importing-Exporting-a-database)
into MySQL Workbench.


4. [Create a user](https://dev.mysql.com/doc/workbench/en/wb-mysql-connections-navigator-management-users-and-privileges.html) named ``stlfarms`` with a password of 
``3f6398041156215b`` and give the user all permissions.


4. Install [IntelliJ IDEA](https://www.jetbrains.com/idea/download/).


5. Clone the project.

```bash
git clone https://github.com/kim-n-lee/saintlouisfarms.git
```

7. Open the project in IntelliJ.
```bash
idea64.exe saintlouisfarms
```

8. Find and click the ![Gradle icon](https://resources.jetbrains.com/help/img/idea/2023.2/gradle.icons.gradle_dark.svg)
 gradle icon.


9. In the Gradle menu, find ``bootRun`` in ``saint-louis-farms`` > ``tasks`` > ``application`` > ``bootRun``.
 
![Gradle pane](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/gradle-pane.png?raw=true)


10. Right-click ``bootRun`` and select ``Modify Run Configuration...``.

![Modify run configuration](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/gradle-modify-run-configuration.png?raw=true)

11. Find the "Environment Variables" field and paste the following string then hit "Apply".
```
dbUserName=stlfarms;db=stlfarms;dbPassword=3f6398041156215b
```
![Gradle database credentials](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/gradle-database-credentials.png?raw=true)

12. Double click "bootRun" in the Gradle menu. After about 15 seconds, everything should
have loaded correctly  and you should see ```Tomcat started on port(s): 2020``` near the bottom of the run pane.

![Tomcat serving on 2020](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/tomcat-serving-on-2020.png?raw=true)

13. Finally, open your browser of choice and go to [http://localhost:2020/](http://localhost:2020/).

### Demo Users:

#### Farmers:

| Username           | Password |
|--------------------|----------|
| ``farmer1@farmer.com`` | ``password`` |
| ``farmer2@farmer.com`` | ``password`` |
| ``farmer3@farmer.com`` | ``password`` |
| ``farmer4@farmer.com`` | ``password`` |
| ``farmer5@farmer.com`` | ``password`` |
| ``farmer6@farmer.com`` | ``password`` |

#### Clients:

| Username          | Password |
|-------------------|----------|
| ``client@client.com`` | ``password`` |



## Acknowledgements

 - Bootstrap: [https://getbootstrap.com/](https://getbootstrap.com/)
 - Nerd Fonts: [https://www.nerdfonts.com/](https://www.nerdfonts.com/)
 - Spring: [https://spring.io/](https://spring.io/)
 - Thymeleaf: [https://www.thymeleaf.org/](https://www.thymeleaf.org/)

## Screenshots

![Homepage](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/homepage.png?raw=true)

![All Farms](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/all-farms.png?raw=true)

![Storefront](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/storefront.png?raw=true)

![New Item with Preview](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/new-item-with-preview.png?raw=true)

![Confirm Order](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/confirm-order.png?raw=true)

![Farmer Product View](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/farmer-product-view.png?raw=true)

![Client Order Log](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/client-order-log.png?raw=true)

![Farmer Order Log](https://github.com/kim-n-lee/saintlouisfarms/blob/main/src/main/resources/static/assets/img/screenshots/farmer-order-log.png?raw=true)