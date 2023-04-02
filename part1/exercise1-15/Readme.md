# Exercise 1-15

Create Dockerfile for an application or any other dockerised project in any of your own repositories and publish it to Docker Hub. This can be any project, except the clones or forks of backend-example or frontend-example.

For this exercise to be complete you have to provide the link to the project in Docker Hub, make sure you at least have a basic description and instructions for how to run the application in a README that's available through your submission.

## About this image

This image has the following functionality:

- Builds upon Ubuntu 22.04

- Notifies Docker that it will expose the port 8000

- Installs PHP and its necessary extensions for Symfony development

- Installs Composer and adds it to the PATH

- Installs Symfony CLI

- Clones the following repository: https://github.com/alinsg/simple-symfony-app

- Starts the Symfony server on container run

## Run the container

In order to have successfully run the container you need to use the following commands:

```bash

docker run -d -p 8000:8000 alinsg/dockerized-symfony-app

```
