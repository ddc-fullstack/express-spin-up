# Express and MySQL Spin Up
## Set Up
**The following files are required to add Express and MySQL to an existing application**
1. `/.gitignore`
    * Updated .gitignore file for the project. 
2. `/project.env`
    * This file should be named after **your project**
    *  Your projects env file based on `example.env`
3. `/docker-compose.yml`
    * Orchestration file for docker containers.
4. `/.dockerignore`
    * An ignore file for Docker. (Almost the same syntax as git ignore)
5. `/backend/src/controllers/index.controller.ts`
    * This file initiates a generic API controller that returns a string message when hit
6. `/backend/src/routes/index.routes.ts`
    * This file initiates a generic API route to test the controller in index.controller
7. `/backend/src/App.ts`
    * This file sets up the server to run on the provided port (4200 as set in index.ts) or default to 3000. It also sets up routing and the middleware for handling JSON responses.
8. `/backend/src/database.ts`
    * This file sets up the database connection.
9. `/backend/src/index.ts`
    * This file instantiates the app. This is the entry point.
10. `/backend/package.json`
    * package.json for the backend code base.
11. `/backend/tsconfig.json`
    * Configuration file for Typescript.
12. `/backend/Dockerfile`
    * File to create a custom node/express image. 
13. `/frontend` 
    * Existing react application.
14. `/sql/Dockerfile`
    * File to create a custom mysql image.
15. `/sql/project.sql`
    * This file should be named after **your project**
    * File containing create table statements to initialize the database
## Run Project
1. `cd` into `/backend`
2. Run `npm i`
3. Run `docker-compose up -d` to start the application
4.  Optional access a running container
    * `docker container exec -it CONTAINER_NAME /bin/bash` to gain shell access to a running container 
    * `mysql -u username -p database` to gain access to the mysql cli
## Calling API (In Postman or Insomnia)
The routes are formed as follows:
http://`[url]`:`[port]`/api /`[object]`/`[how we want to get it]`:`[param]`
