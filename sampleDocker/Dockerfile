# Some of these instructions are from: https://docs.docker.com/language/python/build-images/
# syntax=docker/dockerfile:1 
# This directive instructs the Docker builder what syntax to use when parsing the Dockerfile, and allows older Docker versions with BuildKit enabled to upgrade the parser before starting the build

# Use an official Python runtime as a parent image
FROM python:3.8-slim-buster
# Docker images can be inherited from other images. Therefore, instead of creating our own base image, we’ll use the official Python image that already has all the tools and packages that we need to run a Python application.


# Set the working directory to /app
# To make things easier when running the rest of our commands, let’s create a working directory. This instructs Docker to use this path as the default location for all subsequent commands. By doing this, we do not have to type out full file paths but can use relative paths based on the working directory.
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY requirements.txt requirements.txt

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# At this point, we have an image that is based on Python version 3.8 and we have installed our dependencies. The next step is to add our source code into the image. We’ll use the COPY command just like we did with our requirements.txt file above.
COPY . .

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]

# to build: docker build --tag python-docker .
# to ssh into container
# docker exec -it <name of the conatiner> /bin/bash
# docker exec -it compassionate_robinson /bin/bash
