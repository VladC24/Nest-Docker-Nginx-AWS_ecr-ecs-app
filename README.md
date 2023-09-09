# Nest-React-Docker-Nginx-AWS_ecr-ecs-app
A multi-container Nest/React _TODO app_ with a MongoDb database (created in Mongodb Atlas), deployed via AWS ECS with Docker and which runs on Nginx.

<img width="678" alt="Screenshot 2023-09-09 at 13 36 15" src="https://github.com/VladC24/Nest-Docker-Nginx-AWS_ecr-ecs-app/assets/36422289/cce1bdb4-1a37-47d8-a982-fa04eb9425f8">

## Steps to deployment

- Built the backend and frontend docker images (frontend image containing the nginx server)
- Created a MongoDb database in Mongo Atlas which connects to the application
- Created an ECS cluster with one EC2 instance
- Created an ECR to push the frontend and backend docker images
- Built and pushed the docker images
- Created a new Task Definition in ECS
- Created a new service in the cluster, with two containers (backend and frontend)
- Re-built and pushed the two docker images to ECR - with a new v2 version
- Created environment variables (for the frontend and mongodb urls) set in a new revision of the Task Definition.


