## Task 1 
my-first-image folder created
created Dockerfile under this folder 
## File Content
FROM ubuntu:latest
RUN apt update && apt install -y curl
CMD ["echo", "Hello From My Custom Image"]

## Task 2 
Create a new Dockerfile Under nginx folder and run index.html through dockerfile.
## File Content
### Step 1 FROM - Base Image
FROM nginx:latest

### Step 2 - Set Working Directory
WORKDIR /usr/share/nginx/html

### Step 3 RUN - Execute Command During Build
RUN echo "Build Custom Image From Nginx...."

### Step 4 Copy file from host to Container
COPY index.html .

### Step 5 Expose - Document That Hint The Container To Work on This Port
EXPOSE 80

### Step 6 CMD - Default Command When Container Start

### CMD ["nginx", "-g" ]
