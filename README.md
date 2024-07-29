# Discounting Platform

This repository serves as the parent git repo for the Discounting Platform project. The project is a backend for a discounting platform that stores all the current discounts from different shops, markets, and more. It consists of several microservices, each serving a specific purpose.

The project is build to master Typescript, Docker and understand the concept of event driven architecture.

## Microservices

1. **API Gateway**: This service acts as a central entry point for all requests and forwards them to the corresponding services.

2. **Banners Service**: This service is responsible for displaying different advertising banners on the user interface.

3. **Discount Service**: This service handles CRUD operations related to discounts.

4. **Custom Image Delivery Service**: This service stores and provides access to images for different microservices.

5. **Profiles Service**: This service handles CRUD operations on user profiles.

6. **User Service**: This service handles authentication logic for users and provides CRUD operations.

## Tech Stack

The Discounting Platform project utilizes the following technologies:

- The frontend-backend communication utilizes REST API.
- Most of the services are written in TypeScript.
- All services use MongoDB as the database.
- Interservice communication is established with RabbitMQ.

## Launching the entire project

There are 2 docker compose files one is for production environment the second one is for development. Each service can be launched seperataly if necessary as every service has their own docker files. The env files and its variables has to be defined in each microservice. The commands to run the docker compose file:

Dev:

`docker-compose -f docker-compose.yaml up`

Prod:

`docker-compose -f docker-compose.prod.yaml up`
