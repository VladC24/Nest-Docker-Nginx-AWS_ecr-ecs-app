# Nest-React-Docker-Nginx-AWS_ecr-ecs-app
A multi-container Nest/React _TODO app_ with a MongoDb database (created in Mongodb Atlas), deployed via AWS ECS with Docker and which runs on Nginx.

<img width="678" alt="Screenshot 2023-09-09 at 13 36 15" src="https://github.com/VladC24/Nest-Docker-Nginx-AWS_ecr-ecs-app/assets/36422289/cce1bdb4-1a37-47d8-a982-fa04eb9425f8">

## Steps to deployment

- Built the backend and frontend docker images (frontend image containing the nginx server)
- Created a MongoDb database in Mongo Atlas which connects to the application backend
- Created an ECS cluster with one EC2 instance
- Created an ECR to push the frontend and backend docker images


