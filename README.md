### Forum-App-Go-Backend  [![CircleCI]](https://circleci.com/gh/tjain32/discussion_backend)
 

> This is a forum API built with Golang

## Getting Started

> [[Technologies](#technologies-used) &middot;  &middot; [Installations](#installations) &middot; &middot; [Tests](#tests) &middot; [Author](#author)


## Technologies Used

[golang]: (https://golang.org)

- [Golang](https://golang.org).
- [Gin Framework](https://github.com/gin-gonic/gin).
- [GORM](http://gorm.io).
- [postgreSQL](https://www.postgresql.org).
- [Docker](https://www.docker.com/).
- [Digital Ocean](https://www.digitalocean.com).
- [AWS](https://aws.amazon.com).
- [Circleci](https://circleci.com).

<pre>
   
		"/" - Home Page (GET)

		// Login Route
		"/login" -- Login Page (POST)

		//Users routes
		"/users" -- CREATE a new user

		//Admin tasks
		"/users" -- GET all users (GET)
		"/users/:id" -- GET user by ID (GET)
		"/users/:id" -- UPDATE user by ID (PUT)
	 "/users/:id" -- DELETE user by ID (DELETE)

		//Posts routes
		"/posts" -- CREATE post (POST)
		"/posts" -- GET all posts (GET)
		"/posts/:id" -- GET post by ID (GET)
		"/posts/:id" -- UPDATE post by ID (PUT)
	 "/posts/:id" -- DELETE post by ID (DELETE)
		"/user_posts/:id" -- GET posts by a user (GET)

		//Like route
		"/likes/:id" -- GET like by Id (GET)
		"/likes/:id" -- POST a like (POST)
		"/likes/:id" -- DELETE a like (DELETE)

		//Comment routes
		"/comments/:id" -- CREATE comment (POST)
		"/comments/:id" -- GET comments (GET)
		"/comments/:id" -- UPDATE comment (PUT)
		"/comments/:id" -- DELETE comment (DELETE)</pre>

## Installations

### Clone

- Clone this project to your local machine `https://github.com/tjain32/TechBlogs-BE-Go`


### Setup

  #### Without Docker

  > Ensure that you have your .env set up and have created your database
  - For local, set the DB_HOST in the .env file as follows:
    ```shell
      $ DB_HOST=127.0.0.1
    ```           
  > In the root directory, run the command
  ```shell
  $ go run main.go
  ```
  - Use `http://localhost:8080` as base url for endpoints


 #### Using Docker

  Docker is the default setting for this project

  - Set the DB_HOST as follows in the .env file
    ```shell
      $ DB_HOST=forum-postgres 
    ```    
  ##### For Local Development:
  - Create a Dockerfile file in the root directory
  - Copy the content of the file: example.Dockerfile.dev (for only local development)
  - Create a docker-compose.yml file in the root directory
  - Copy the content of the file: example.docker-compose.dev.yml (for only local development)

  ##### For Testing:
  - Create a Dockerfile.test file in the root directory
  - Copy the content of the file: example.Dockerfile.test (for only test)
  - Create a docker-compose.test.yml file in the root directory
  - Copy the content of the file: example.docker-compose.test.yml (for only test)
  
  ##### For Production (This should be done in the server (AWS, DigitalOcean, etc)):
  - Create a Dockerfile file in the root directory
  - Copy the content of the file: example.Dockerfile.prod (for production only)
  - Create a docker-compose.yml file in the root directory
  - Copy the content of the file: example.docker-compose.prod.yml (for production only)

  
  In the root directory, run the command:
  ```shell
  $ docker-compose up --build
  ```
  - Use `http://localhost:8888` as base url for endpoints



## Tests

  ### Without Docker

  - Run test for all endpoints
    > Navigate to the tests directory and run
    ```shell
    $ go test -v ./...
    ```

  ### Using Docker

- Run test for all endpoints
  > If you have set up the Dockerfile.test and the docker-compose.test.yml files above, from the root directory of the app.
  ```shell
  $ docker-compose -f docker-compose.test.yml up --build 
  ```


## Author

- Tanishqa Jain
