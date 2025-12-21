# Markdown_CV

This repo contains a **Dockerized markdown-based CV**

What in this project:
 - My CV in Markdown
 - Build it into a static web format using Docker
 - Test running it locally 
 - Test running it using AWS cloud services
 (With this project, I'm practicing git, github, and get more familiarizng with docker, dockerhub, and AWS)

## CV Content
Can be seen in my_CV.md

## Markdown-based CV
The application is my CV written in Markdown, which is converted into html and run in a Docker container & served using nginx. 

## Github Actions
The Github Action is set on the root repo which helps to push the Docker image automatically onto Dockerhub whenever changes of the docker image is changed or updated. 

## Deployment av application onto AWS
- I've created an EC2 instance running Amazon Linux was created 
- A security group was configured as : SSH (port 22), HTTP (port 80)
- Install Docker on the EC2-server
```bash
    sudo yum update -y
    sudo yum install docker -y
    sudo systemctl start docker
    sudo systemctl enable docker
    sudo usermod -aG docker ec2-user
```

## Run a Docker
```bash
    docker pull <dockerhub-username>/markdown-cv:latest
    docker run -d -p 80:80 <dockerhub-username>/markdown-cv:latest
```
