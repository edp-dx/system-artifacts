# Technical Discovery

## What's the programming language and its version the project written with?

The programming language used in the project is Java, and the version specified in the `pom.xml` file properties is Java 17.


## What's the framework and its version the project written with?

The project uses the Spring Boot framework, and it is set to use the version defined by the parent dependency `spring-boot-starter-parent` with the version `3.2.1`.


## What's the building tool and its version the project written with?

The project uses Maven as the build tool, and it is using version 3.2.1 of the `spring-boot-starter-parent` as the parent POM, which implies compatibility with that version or similar of Maven.


## What's the deployment tool and its version the project written with?

The deployment tool used for the project is Maven, and the version used is 3.9.5 as specified in the `.mvn/wrapper/maven-wrapper.properties` file.


## What's the testing tool and its version the project written with?

The project uses Testcontainers with JUnit Jupiter for testing. The version information is not provided in the context.


## If Struts, JSP, JSF technologies are used in the project?

No, the project uses Spring Boot with Thymeleaf for its web layer and does not utilize Struts, JSP, or JSF technologies.


## What types of EJB beans are used in he project?

The provided context does not indicate the usage of any Enterprise JavaBeans (EJB) in the project.


## What's the external libraries and API are used at the project?

The project utilizes the following external libraries and APIs:

1. Spring Boot starter libraries for creating web applications, data access with JPA, caching, validation, and actuator endpoints.
2. Webjars for client-side dependencies like Bootstrap and Font Awesome.
3. Database connectors for H2, MySQL, and PostgreSQL.
4. Caching API - JCache API and Caffeine.
5. Jakarta XML Binding API.
6. Testcontainers for integration tests with databases.
7. Spring Boot DevTools for development-time features.
8. JUnit Jupiter for testing in conjunction with Testcontainers.


## Check if there is existing CI/CD pipelines in the project?

Yes, there is a GitHub Actions workflow defined in the `.github/workflows/maven-build.yml` file, which sets up a CI pipeline to build a Java project with Maven upon pushes and pull requests to the main branch.


## What's the technology of CI/CD pipeline and its version?

The technology behind the CI/CD pipelines for this project is GitHub Actions, as defined in the `.github/workflows/maven-build.yml` file. There is no explicit version mentioned for GitHub Actions itself since it is a hosted service provided by GitHub, but the workflow uses version 4 of the `actions/checkout` action and version 4 of the `actions/setup-java` action.


## Check if there is any quality gates in the existing CI/CD pipeline?

Based on the provided context, there is no direct indication of quality gates being implemented in the CI/CD pipeline configuration. The `.github/workflows/maven-build.yml` file shows a GitHub Actions workflow that only includes steps for checking out the code and building the project with Maven. There are no steps visible in this file that would suggest additional quality checks, such as running tests or static code analysis tools as part of the pipeline execution.


## Analyze CI/CD pipelines for URL, names, namespace terms for the next injections: 'dev', 'prod', 'uat', 'test' and use that information to guess the number of deployment environments and their names.

Based on the provided context, there is no explicit information about CI/CD pipelines, environment names, or namespace terms such as 'dev', 'prod', 'uat', or 'test'. The context mainly covers details about building, testing, and running the Spring PetClinic application, but does not mention deployment environments or CI/CD configurations. Therefore, I'm unable to deduce the quantity and names of deployment environments from the given context.


## Check if custom libraries are used for secrets encryption. List secrets encryption libraries if any.

Based on the provided context, there is no mention of any libraries being utilized for secrets encryption within the `pom.xml` files. Therefore, I cannot confirm the use of any secrets encryption libraries.


## Check if passwords are hard-coded in code.

Based on the provided context, there is no evidence of hard-coded passwords in the code.


## Check is SSL connection used between this app and a DB.

Based on the provided context, there is no explicit configuration that suggests an SSL connection is being utilized for communication between the application and the database. The database connection URLs in the `application-postgres.properties` and `application-mysql.properties` files do not include SSL parameters.


## Check if API requires secure connection (https, ssl ) if any.

The provided context does not contain any explicit information indicating that the API requires a secure connection such as HTTPS or SSL. The `petclinic_test_plan.jmx` file includes `HTTPSampler` elements without specifying the protocol as HTTPS, suggesting that the test plan may not be specifically designed for secure connections. However, without seeing the actual configuration of the application or its deployment settings, I cannot definitively state whether the API requires a secure connection.


## Check if there are unit tests exists and if it is so, print the technologies list.

Yes, there are unit tests in place. The technologies utilized for testing in the project include:

- JUnit Jupiter (JUnit 5) for writing test cases, as seen in the use of the `@Test` annotation.
- Spring Boot Test framework, indicated by the use of `@SpringBootTest` and related annotations.
- Testcontainers for integration testing with real databases, as shown by dependencies on `spring-boot-testcontainers` and specific Testcontainers like `mysql`.
- Mockito, suggested by the use of `@MockBean` for mocking dependencies in tests.
- Spring MVC Test framework, for testing MVC controllers, indicated by the use of `MockMvc`.
- RestTemplateBuilder for creating instances of `RestTemplate` for testing RESTful endpoints.


## Check if there are integration tests that uses real database.

Yes, there are integration tests that utilize real databases. The `MySqlIntegrationTests` class uses Testcontainers to start a MySQL database in a Docker container for testing, and the `PostgresIntegrationTests` class uses Docker Compose to start a PostgreSQL database for testing.


## Check if there are user friendly API description.

Based on the provided context, there is no explicit mention of a user-friendly API description available within the given files. However, there is a reference to a presentation about understanding the Spring Petclinic application which might contain further information about the application's structure and possibly its API. The link to the presentation is found in the readme.md file:

```
[See the presentation here](https://speakerdeck.com/michaelisvy/spring-petclinic-sample-application)
```

For a detailed API description, one would typically look for API documentation, a Swagger UI, or similar, none of which are explicitly mentioned in the provided context.


## Check if there are hardcoded IP addresses.

No, there are no hardcoded IP addresses present in the provided context.
