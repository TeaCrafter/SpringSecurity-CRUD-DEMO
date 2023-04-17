# SpringSecurity-CRUD-DEMO
This project will walk through Spring Boot Security REST + JPA + Hibernate + MySQL CRUD example, and  test the Rest APIs using postman.

### Software Used
Find the software used in the example.
1. Java 8
2. Spring Boot 1.5.3.RELEASE
3. Maven 3.3
4. MySQL 5.5
5. Eclipse Mars

### REST API
1. Create :
HTTP Method: POST, URL: /user/article

2. Read :
HTTP Method: GET, URL: /user/article/{id}
 or 
HTTP Method: GET, URL: /user/articles

3. Update :
HTTP Method: PUT, URL: /user/article

4. Delete :
HTTP Method: DELETE, URL: /user/article/{id}

### Run Application
1. You can clone it from github by running following command
```
  $ git clone https://github.com/ZhiqiangLi2022/SpringSecurity-CRUD-DEMO.git
```
2. Import project into eclipse
```
  File -> Import -> Maven -> Existing Maven Projects -> Browse Project from cloned location
```
3. Right click on project in eclipse and then Maven -> Update Projects
4. Import src/main/java/resources/book.sql into MySQL database
5. Update database credential and other configuration into application.properties available in src/main/java/resources
```
#spring.datasource.driver-class-name=com.mysql.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/concretepage
spring.datasource.username=root
spring.datasource.password=root
spring.datasource.tomcat.max-wait=20000
spring.datasource.tomcat.max-active=50
spring.datasource.tomcat.max-idle=20
spring.datasource.tomcat.min-idle=15

spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQLDialect
spring.jpa.properties.hibernate.id.new_generator_mappings = false
spring.jpa.properties.hibernate.format_sql = true

logging.level.org.hibernate.SQL=DEBUG
logging.level.org.hibernate.type.descriptor.sql.BasicBinder=TRACE
```
6. Right click on Application.java file and run as Java Application

### Once Sprint Boot Application will be started successfully then we can call following Endpoints by using POSTMAN
1.To get Article by Id with GET Request
```
http://localhost:8080/user/article/{id}
```
2.To get all Articles
```
http://localhost:8080/user/articles
```
3.To add Article
```
http://localhost:8080/user/article
```
4.To update Article
```
http://localhost:8080/user/article/{id}
```
5.To delete Article
```
http://localhost:8080/user/article/{id}
```
