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

## Task 3
Used CMD and Entrypoint in Two Different File 
When we use CMD Its Runs as a Default Command But When we Pass a Command After Image, Its Replaced With Actual Argument That We Provide 
## File Content
FROM ubuntu:latest 
CMD ["echo", "Hello"]

Like If we add Hi Hello After Image Then Its Print Hi Hello  not only Hello like
FROM ubuntu:latest:Hi Hello then its Replaced The Hello Completely because its Override The Actual Arguments.
~                         

## Task 4
Created Small Static index.html file under docker directory
here is the Dockerfile Content 

FROM nginx:alpine

WORKDIR  /usr/share/nginx/html

COPY index.html .

RUN echo "Running index.html from Nginx"

EXPOSE 80

## Task 5
Created .dockerignore file under Health Plus App Directory
here is the .dockerignore content

#Ignore Common Development Files and Directories
.git
.md
.env
LICENSE
node_modules

**Note**: If We Build The Image Before Included .dockerignore file the build context size is larger 
**Sending build context to Docker daemon  8.363MB**

but when we include the .dockerignore file the build context size is decreased than before 
**Sending build context to Docker daemon  3.804MB**

**and also when we checked the ignored files under the container its not showed**
