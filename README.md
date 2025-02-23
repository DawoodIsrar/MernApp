# MernApp# A simple MERN stack application 

### Create a network for the docker containers

`docker network create demo`

### Build the client 

```sh
cd mern/frontend
docker build -t mern-frontend .
```
### Create a netwrok

`docker network create mern`

### Run the client

`docker run --name=frontend --network=demo -d -p 5173:5173 mern-frontend`

### Verify the client is running

Open your browser and type `http://localhost:5173`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongodb:latest`

### check logs

`docker logs frontend`

### Build the server

```sh
cd mern/backend
docker build -t mern-backend .
```

## RUN MONGO IN CONTAINER

`docker run -d --name mongodb -p 27017:27017 mongo`

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 mern-backend`

## Using Docker Compose

`docker compose up -d`

