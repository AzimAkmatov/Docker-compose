1. Build Dockerfile with next ENV.
# Use an official base image
FROM ubuntu:latest

# Set environment variables
ENV AGE=28
ENV NAME="John Doe"
ENV LOCATION="Chicago"

# Command to keep the container running (for testing purposes)
CMD ["sleep", "infinity"]
2. Run container and go inside.
3. Run
"printenv AGE
printenv NAME
printenv LOCATION
"
### Dockerignore
1. Create a file named .dockerignore
2. Put all files except index.html and chicago.jpeg
3. Run nginx container and check the files.
4. Check browser

### Multistage Ruby
1. Build Dockerfile using multistage build

### Postgres container
1. Build Dockerfile and copy init.sql into image
2. Run container
3. Go inside and check
"\dt   -- List tables
SELECT * FROM users;  -- Query the users table"

### AWS ECR Push
1. Create a repo on ECR using AWS CLI:
aws ecr create-repository --repository-name class-repo --region us-east-2
2. Login into AWS:
aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin 362504286772.dkr.ecr.us-east-2.amazonaws.com
3. Tag your image:
docker tag <your_image> <aws_account_id>.dkr.ecr.us-east-2.amazonaws.com/class-repo:1
4. Push the image:
docker push <aws_account_id>.dkr.ecr.us-east-2.amazonaws.com/class-repo:1
5. Check from CLI and browser:
aws ecr list-images --repository-name class-repo --region us-east-2


