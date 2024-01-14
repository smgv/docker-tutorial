# Docker Notes

Docker enables Development, Packaging and Execution of application in a unified environment by clearly specifying nodejs version and necessary packages.

Docker generates self contained box that includes its own operating system and all the components essential for running our application.

This box acts likes a separate computer virtually providing the Operating System, Runtimes and Everthing Required to run smoothly.

## Why we bother to use Docker?

Using docker will make your application better and faster in terms of both Development and Deployment.

**_Uber Case Study Says that Docker helped them onboard new developers in minutes instead of weeks_**.

## Advantages

#### 1. Consistency Across Environments:

Docker ensures that our application runs the same on my computer and others computer. Everyone uses the same command to run the app irrespective of the environments its running. Since downloading the node.js isn't the same on Linux, Windows or MacOs developers have to take care of different OS. Docker takes care of all of that for us this keeps everyone on the same page.

- Reduces Confusion
- Boosts Collaboration
- Faster Development and Deployment

#### 2. Isolation:

Docker ensures clear boundaries between our app and dependencies so we don't have conflicts between applications.

- Improves Security
- Simplifies Debugging
- Smooth Development Process

#### 3. Portability:

Docker let's us easily move our applications between different stages like from development to testing and from testing to production. Docker containers are light weight and share the host system resources making them more efficient than any VM.

- Faster application restart time
- reduced resource usage

#### 4. Version Control:

Docker helps with version control as we do version control of our code using git.

#### 5. Scalability:

Docker makes it easy to handle more users by creating copies of our application when needed.

#### 6. DevOps Integration:

Docker bridges the gap between developer and Operations team. Integration ensures continuous feedback and collaboration.

## How Does Docker Work?

Important Concepts on which Docker's entire workflow revolves around:

1. Images:

   Docker Image is a Lightweight, Standalone, Executable Package that includes everything needed to run a piece of software including the code, runtime like node.js, libraries and system tools.

2. Containers:

   Docker container is a runnable instance of a Docker image it represents the execution environment for a specific applications including its code, runtime like node.js, libraries and system tools. A Container takes everything specified in the image and follows it's instructions by executing necessary commands downloading packages and setting things up to run our application.

   We can run multiple containers from single image.

3. Volumes:

   A Docker Volume is a Persistent data storage mechanism that allows data to be shared between a docker container and the host machine i.e. laptop. It ensure data durability and persistent even if container is stopped or removed.

4. Networks:

   Docker Network it's a communication channel that enables different docker containers to talk to each other or with external world. It creates connectivity allowing to share information and services while maintaining isolation.

## Docker Workflow:

- Docker Client: UI
- Docker Host (aka Docker Daemon): All process run here
- Docker Registry (aka Docker Hub): Stores all Private and Public Images.

## Docker Compose:

Its a tool that allows us to define and manage multi container docker applications it uses .yaml file to configure the services, network and volumes for your applications enabling us to run and scale the entire application using single command.

Using Docker Init CLI we can auto generate the file with all required tech and services.

## Docker Compose Watch:

It keeps the code updated in docker image. whenever we do some changes locally it will watch the change follow the below steps:

- Sync
- Rebuild
- Sync-Rebuild

We have to configure this in compose.yml file.

## Publish Docker Image to Docker Hub

- First Image should be created
- run the below command

  ```
  1. docker tag [image_name] [user_name]/[image_name]
  2. docker push [user_name]/[image_name]

  Example:

  > docker tag react-docker smgv/react-docker
  > docker push smgv/react-docker
  ```

## Docker Compose and Watch Command

```
# run the compose file
> sudo docker compose up

# it will look for the code changes
> sudo docker compose watch
```
