# Docker Commands

### List Down All docker Running Docker Containers
docker ps

### Lists docker images on the host machine
docker images

### Build image 
docker build

### Run a Docker container.
docker run
 
There are many arguments which we can pass to this command for example,

`docker run -d` -> Run container in background and print container ID
`docker run -p` -> Port mapping

use `docker run --help` to look into more arguments.

### To stop docker container
docker stop

### To start the docker conainer
docker start 

### To remove the docker container
docker rm

### To remove docker conatiner from host machine
docker rmi (ps we also needs to provide more details for the perticulat coniner like conatiner id) 

### To pull the image from the registery
docker pull (the registery name and all the deatils)


### To push the docker image to the registery
docker push (image details)

### To Manage Docker networks such as creating and removing networks, and connecting containers to networks
docker network

### Sample docker file

```
# Use the official Python image as the base image
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Copy the requirements file and install dependencies
COPY requirements.txt /app
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . /app

# Expose the port the app runs on
EXPOSE 8000

# Start the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

```
