1. First build the image

   BUILD CMD : docker build -t hello-docker

   - -t : tag
   - hello-docker : image name

2. Run the Container

   docker run hello-docker

3. To get the interactive shell in your terminal

   docker run -it hello-docker sh

   - -it : interactive session
   - sh : open your docker working dir i.e. /app in your terminal to execute the command.
