# Spring Boot Project Template

This is a template for starting a new Spring Boot project. It includes a basic folder structure and essential dependencies to get you started quickly.

## Folder Structure

```
Spring_Boot_Project_Template/
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.learning.security
│   │   │       ├── auth            # Handles authentication and security
│   │   │       ├── configs         # Configuration classes for Spring beans and services
│   │   │       ├── controllers     # REST API controllers to handle incoming HTTP requests
│   │   │       ├── dtos            # Data Transfer Objects for request/response models
│   │   │       ├── enums           # Enumerations used across the project
│   │   │       ├── exceptions      # Custom exceptions and handlers
│   │   │       ├── models          # Entity classes for database mapping
│   │   │       ├── repos           # Repository interfaces for data access
│   │   │       ├── services        # Service layer to handle business logic
│   │   │       └── utils           # Utility classes for reusable functionality
│   │   ├── resources
│   │       ├── static              # Static assets (HTML, CSS, JS)
│   │       ├── templates           # Thymeleaf templates for server-side rendering
│   │       └── application.properties  # Centralized configuration for the application
│   ├── test
│       └── java                    # Unit and integration tests
├── .mvn                            # Maven wrapper files for portability
├── target                          # Compiled classes and packaged artifacts
├── .gitignore                      # Specifies files and directories to be ignored by Git
├── pom.xml                         # Maven build configuration file
└── README.md                       # Documentation for the project

```
Note: The artifact name can be modifies as per your project
---

## Configuration

### `application.properties`

This file is used to configure various aspects of the Spring Boot application. For example:

```properties
server.port=8080
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=root
spring.datasource.password=secret
```

### `pom.xml`

This file is used to manage the project's dependencies and build configuration. It includes information about the project and configuration details used by Maven to build the project.

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
        <modelVersion>4.0.0</modelVersion>
        <groupId>com.example</groupId>
        <artifactId>demo</artifactId>
        <version>0.0.1-SNAPSHOT</version>
        <name>demo</name>
        <description>Demo project for Spring Boot</description>
        <parent>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-parent</artifactId>
                <version>2.5.4</version>
                <relativePath/> <!-- lookup parent from repository -->
        </parent>
        <dependencies>
                <!-- Dependencies go here -->
        </dependencies>
        <build>
                <plugins>
                        <plugin>
                                <groupId>org.springframework.boot</groupId>
                                <artifactId>spring-boot-maven-plugin</artifactId>
                        </plugin>
                </plugins>
        </build>
</project>
```

## General Dependencies

The `pom.xml` file includes the following basic dependencies:



### For Persisting data

    <dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-data-jpa</artifactId>
	</dependency>

### For enabling spring security

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-security</artifactId>
    </dependency>

### For enabling spring web

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>

### For enabling mysql connection

    <dependency>
        <groupId>com.mysql</groupId>
        <artifactId>mysql-connector-j</artifactId>
        <scope>runtime</scope>
    </dependency>

### For enabling lombok - for auto generation of getters, setters, constructors, etc

    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <optional>true</optional>
    </dependency>   

### For enabling spring boot test

    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>

### For enabling jwt

    <dependency>
        <groupId>io.jsonwebtoken</groupId>
        <artifactId>jjwt-api</artifactId>
        <version>0.12.6</version>
    </dependency>

### For enabling jjwt-impl

    <dependency>
        <groupId>io.jsonwebtoken</groupId>
        <artifactId>jjwt-impl</artifactId>
        <version>0.12.6</version>
        <scope>runtime</scope>
    </dependency>

### For swagger docs using openapi

    <dependency>
        <groupId>org.springdoc</groupId>
        <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
        <version>2.0.2</version>
    </dependency>

### For enabling spring security test

    <dependency>
        <groupId>org.springframework.security</groupId>
        <artifactId>spring-security-test</artifactId>
        <scope>test</scope>
    </dependency>
---


## Running the Application

To run the application, use any IDE or use the following command:

```bash
mvn spring-boot:run
```

This command will start the Spring Boot application on the configured port (default is 8080).

## Conclusion

This template provides a solid foundation for starting a new Spring Boot project. It includes a basic folder structure, essential dependencies, and configuration files to help you get started quickly. Customize it as needed for your specific project requirements.