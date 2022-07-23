1. Create Docker file
  Sample content:
  ```
  FROM nginx:latest
  COPY ./index.html /usr/share/nginx/html/index.html
  ```
  
2. Build docker image
  ** docker build -t my-image:v0.0.1 .
3. Check docker image using 
  ** docker images
4. Run the docker image
  ** docker run -it --rm -d -p 8080:80 --name my-container my-image:v0.0.1
5. Check the containers
  ** docker ps -a
6. Stop container
  ** docker stop my-container
7. Remove container 
  ** docker rm -f <containerId>
8. Remove the docker image
  ** docker image rm my-image:v0.0.1
