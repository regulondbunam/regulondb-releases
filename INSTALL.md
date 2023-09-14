## How to install a local instance of RegulonDB

## Required Software
- Docker
- Docker Compose

## Installation Guide

Download or copy the content of the following [docker-compose.yml file](https://regulondbdata.ccg.unam.mx/docker/docker-compose.yml).

Locate the file in a terminal and use the following command to get the images required from DockerHub: 

```bash
docker compose pull
```

When the download is compleated, use the following command to start the RegulonDB instance:
```bash
docker compose up -d
````

Your instance now is working on http://localhost:7000/ for the Web App or http://localhost:7000/graphql to use the RegulonDB GraphQL Playground. If you want to stop the instance locate the file in the terminal and use the following command:
```bash
docker compose down
```

## New Releases
When a new version of the is released, you can use the Install Guide steps again deleting the previous version of the docker-compose.yml file or rewriting with the new content (or if the repo was cloned yo can only use the ```git pull``` command to update it)

Then to release space for the new images, remove all the previous images using the following command:
```bash
docker system prune -a
```
**Warning:** This command will remove all the docker images in your computer, if you use docker for other images than the RegulonDB instance, please use the ```rmi``` command to remove the images one by one
