# Basik-Marketing-Assignment

# This repository contains the Docker Compose configuration for setting up the Basik Marketing Assignment project. The Docker Compose file defines two services: api and db. 

## Services:
### 1. api Service:
#### Description: This service sets up the API server for the Basik Marketing Assignment project.
#### Build: The service is built from the Dockerfile located in the api directory.
#### Restart Policy: The service is set to restart automatically unless stopped.
#### Ports: The API server is exposed on port 3000 of the host machine, and the same port inside the container.
#### Dependencies: The api service depends on the db service.

### 2. db Service:
#### Description: This service sets up the database server for the Basik Marketing Assignment project.
#### Build: The service is built from the Dockerfile located in the db directory.
#### Restart Policy: The service is set to restart automatically unless stopped.
#### Ports: The Redis database server is exposed on port 6379 of the host machine, and the same port inside the container.
#### Volumes: The data directory ./data on the host machine is mounted to /data inside the container for persisting database data.




## Usage:
#### 1. Make sure you have Docker installed on your system.
#### 2. Clone this repository to your local machine.
#### 3. Navigate to the directory containing the docker-compose.yml file.
#### 4. Run the following command to start the services:
      docker-compose up -d
#### 5. Access the API server at http://localhost:3000.




## Additional Notes:
#### Ensure that no other services are using ports 3000 and 6379 on your system to prevent conflicts.
#### You can customize the configuration by modifying the Dockerfile and environment variables as needed.
