# docker_webapp

### Creating Node.js application ###

1. Install NPM and Express Framework
   > $ mkdir docker_webapp 
   > $ cd docker_webapp
   > $ npm init 

2. Add express framework
   > $ npm install express --save

3. Run the app
   > $ node index.js

(Go to http://localhost:8081/ in your browser to view it)

### Dockerizing Node.js application ###

1. Install Docker for your OS
2. Write Dockerfile
3. Build docker image
   > $ docker build -t docker_webapp .
4. Run docker container
   > docker run -p 8081:8081 docker_webapp
5. Share docker Image
   a. Sign up at hub.docker.com
   b. Build the image again using your Docker Hub credentials:
      > $ docker build -t [USERNAME]/docker_webapp .
   c. Log in to Docker Hub with your credentials:
      > $ docker login
   d. Push the image to Docker Hub:
      > $ docker push [USERNAME]/docker_webapp
6. Now you can use the image on any server or PC with Docker installed:
   > $ docker run [USERNAME]/docker_webapp
