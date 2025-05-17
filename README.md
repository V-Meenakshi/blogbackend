# Read Me First
The following was discovered as part of building this project:

* The original package name 'com.blogverse.blogverse-backend' is invalid and this project uses 'com.blogverse.' instead.

# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/3.4.5/maven-plugin)
* [Create an OCI image](https://docs.spring.io/spring-boot/3.4.5/maven-plugin/build-image.html)
* [Spring Web](https://docs.spring.io/spring-boot/3.4.5/reference/web/servlet.html)
* [Spring Security](https://docs.spring.io/spring-boot/3.4.5/reference/web/spring-security.html)
* [Spring Data JPA](https://docs.spring.io/spring-boot/3.4.5/reference/data/sql.html#data.sql.jpa-and-spring-data)
* [Validation](https://docs.spring.io/spring-boot/3.4.5/reference/io/validation.html)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)
* [Securing a Web Application](https://spring.io/guides/gs/securing-web/)
* [Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)
* [Authenticating a User with LDAP](https://spring.io/guides/gs/authenticating-ldap/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Validation](https://spring.io/guides/gs/validating-form-input/)

### Maven Parent overrides

Due to Maven's design, elements are inherited from the parent POM to the project POM.
While most of the inheritance is fine, it also inherits unwanted elements like `<license>` and `<developers>` from the parent.
To prevent this, the project POM contains empty overrides for these elements.
If you manually switch to a different parent and actually want the inheritance, you need to remove those overrides.

Here are the typical commands and setup steps to include in the `README.md` file for running a **Spring Boot backend** locally:

---

### 🚀 Getting Started - Backend (Spring Boot)

#### ✅ Prerequisites

* Java 17 or higher installed
* Maven installed (`mvn -v` to check)
* Supabase project set up (with credentials)
* PostgreSQL URL and credentials (from Supabase)

#### 📦 Running the Backend Locally

1. **Clone the repository**

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name/backend
```

2. **Configure the environment**

Create an `.env` file or configure the following variables in `application.properties` or `application.yml`:

```properties
# application.properties
spring.datasource.url=jdbc:postgresql://<your-supabase-db-host>:5432/postgres
spring.datasource.username=your-db-username
spring.datasource.password=your-db-password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# JWT or other security-related configs if applicable
```

> 💡 *If you're using Supabase, find your credentials in your project's settings under "Database".*

3. **Run the application**

Using Maven:

```bash
./mvnw spring-boot:run
```

Or using Java:

```bash
./mvnw clean package
java -jar target/*.jar
```

4. **API is available at:**

```
http://localhost:8080/api
```




