- ### docker build -t [image_name] .

  ```
  . here means where is your Dockerfile it can be ./app/  as per your folder structure this command is used to build the image and -t flag is used give the name to your image
  ```

- ### docker images

  ```
   will show all the images in your system build or created
  ```

- ### docker ps

  ```
   will show all the running containers only
  ```

- ### docker ps -a

  ```
   will show you all the running and not running containers
  ```

- ### docker stop [container_name]

  ```
   will stop the running
  ```

- ### docker run [image_name]

  ```
   will run the image by creating the container by giving the dynamic name by itself
  ```

- ### docker run —name [container_name] [image_name]

  ```
   it will also run the container but it will have your given name
  ```

- ### docker run —name [container_name] -p [YOUR_PORT]:[EXPOSED_PORT_FROM_IMAGE] -d [image_name]

  ```
   this command will run the container by mapping your own port to the exposed image port
  ```

- ### docker image rm [image_name]

  ```
   will delete the image that is unused
  ```

- ### docker image rm [image_name] -f

  ```
   will delete the image even if its used in container -f will force to delete the image
  ```

- ### docker container rm [container_name1, container_name2, …]

  ```
   will delete the container
  ```

- ### docker system prune -a

  ```
   will delete all images and containers
  ```

- ### docker build -t [image_name] [tag_name] .

  ```
  - it will build the image with different tag for versioning
  ```

- ### docker start [container_name]

  ```
   it will start the container work only for the existing once and it will not block the console for use

  ```

- ### docker start -i [conatiner_name]

  ```
   it will work same as above but will block the console for use.

  ```

- ### Run vs Start

  ```
   run create the brand new container and make it run where as start will only run the existing container will not create it on fly.
  ```

- ### docker-compose up

  ```
   it run the compose file
  ```

- ### docker-compose down

  ```
   it stop the container
  ```

- ### docker-compose down —dmi all -v

  ```
   it remove all images and volumes associated with it.
  ```

- ### docker run -p 51735173 react-docker

  ```
   used for port mapping from container to host machine
  ```

- ### docker run -p 5173:5173 -v "$(pwd):/app" -v /app/node_modules react-docker

  ```
   on code change it will also rebuild the docker for that we use -v “$(pwd):/app” and we use other flag -v to mount the node_modules so it can use the same node_modules instead of installing it again and again
  ```

- ### rm ~/.docker/config.json

  ```
  when we get error related to the local metadata
  ```
