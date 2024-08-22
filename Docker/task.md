1. Create new Dockerfile
Details:
Base image "Ubuntu:latest"
Open port 8080 with "EXPOSE 80"
Install Nginx
Replace original "index.html" file with local "index.html"
or
Delete original "index.html" and put your own "index.html"
or
Replace the content of original "index.html" file with "Hello class"
RUN echo ...
2. Build image "nginx-task-image"
3. Run container "nginx-con" port 80:80
4. Open browser and type "localhost:80"
You should see "Hello Class"