# post-service
The Post Service is a microservice in the Instagram clone application that handles user posts. It allows users to create, retrieve, update, and delete posts, as well as add comments, update comments, and like posts.

## Features

- Retrieve all posts
- Create a new post
- Update a post
- Retrieve a specific post by ID
- Retrieve posts by user ID
- Add a comment to a post
- Update a comment
- Delete a comment
- Like a post
- Retrieve the number of likes for a post

## Dependencies

- [Spring Boot] 
- [Spring Web]
- [Spring Data JPA]
- [postgresql]
- [Spring Cloud]
- [Spring Cloud OpenFeign]
- [ProjectLombok]

## Getting Started
These instructions will get you a copy of the Follow Service up and running on your local machine for development and testing purposes.

### Prerequisites

- [Java SE Development Kit 17.0.5] (https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [Maven 4.0.0] (https://maven.apache.org/install.html)
- [Spring Boot CLI] (https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#getting-started-installing-the-cli) (Optional)

### Installation
1. Clone the repository:
```bash
git clone <repository-url>
```
2. Navigate to the project directory::
```bash
cd post-service
```
3. Open the application.properties file and configure the database connection details:
```
spring.datasource.url=jdbc:mysql://localhost:8086/posts_db
spring.datasource.username=<database-username>
spring.datasource.password=<database-password>
```
4. Build the project using Maven:
```bash
cd post-service
```
5. Run the application:
```bash
mvn spring-boot:run
```
## API Documentation
The Post Service provides the following API endpoints:

- GET /posts/: Retrieves all posts.
- POST /posts/: Creates a new post.
- PUT /posts/{id}: Updates a post.
- GET /posts/{id}: Retrieves a specific post by ID.
- GET /posts/user/{userid}: Retrieves posts by user ID.
- POST /posts/addComment: Adds a comment to a post.
- DELETE /posts/{id}: Deletes a post.
- PUT /posts/comment/{id}: Updates a comment.
- DELETE /posts/comment/{id}: Deletes a comment.
- POST /posts/likepost?uid={uid}&postId={postId}: Likes a post.
- GET /posts/getLikes/{id}: Retrieves the number of likes for a post.
