# Nest-React-Docker-Nginx-AWS_ecr-ecs-app
A multi-container Nest/React _TODO app_ with a MongoDb database (created in Mongodb Atlas), deployed via AWS ECS with Docker and which runs on Nginx.

**This was done for Nginx, AWS ECR and AWS ECS learning purposes.**

<img width="678" alt="Screenshot 2023-09-09 at 13 36 15" src="https://github.com/VladC24/Nest-Docker-Nginx-AWS_ecr-ecs-app/assets/36422289/cce1bdb4-1a37-47d8-a982-fa04eb9425f8">

## Steps to deployment

- Built the backend and frontend docker images (frontend image containing the nginx server)
- Created a MongoDb database in Mongo Atlas which connects to the application
- Created an ECS cluster with one EC2 instance
- Created an ECR repository
- Built and pushed the two docker images (frontend and backend) to the ECR repository
- Created a new Task Definition in ECS
- Created a new service in the cluster, with two containers containing the backend and frontend images.
- Created environment variables (for the frontend and mongodb urls) set in a new revision of the Task Definition.
- Re-built and pushed the two docker images to ECR - with a new v2 version

## CONS
When having an application with multiple containers running on an EC2 instance, if the application has a lot of traffic, then multiple EC2 instances would be required with scaled-up service instances. This would add extra cost. 
