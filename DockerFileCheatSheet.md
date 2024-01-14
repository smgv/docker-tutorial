# Dockerfile Commands

1.  FROM image[:tag] [As name]

    Specify the base image we want to use

    ```
    Example

    > FROM ubuntu:20.40
    ```

2.  WORKDIR /path/to/workdir

    The WORKDIR instruction sets the working directory for any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow it in the Dockerfile.

    ```
    Example

    > WORKDIR /app
    ```

3.  COPY [ --chown=< user >:< group > ] < src >... < dest >

    Copies the file or dir from build context to images

    ```
    Example

    > COPY .  /app
    ```

4.  RUN < command >

    It execute commands in the shell during image build

    ```
    Example

    > RUN  npm run dev
    ```

5.  EXPOSE < port > [ < port > / < protocol > ...]

    Expose inform docker that the container will listen on specified network PORT at runtime

    ```
    Example

    > EXPOSE  3000
    ```

6.  ENV KEY=VALUE

    ENV set the environment variable during the build process

    ```
    Example

    > ENV  NODE_ENV=production
    ```

7.  ARG < name >[ = < default value >]

    ARG defines build time variables like having a note.

    ```
    Example

    > ARG  NODE_VERSION=20
    ```

8.  VOLUME ["/data"]

    Volume creates a mount point for externally mounted volume

    ```
    Example

    > VOLUME  /myvol
    ```

9.  CMD ["npm", "run", "dev"]

    CMD provides default command to execute when the container starts

    ```
    Example

    > CMD  npm run dev
    ```

10. ENTRYPOINT

    ENTRYPOINT is the default command to execute when the container starts

    ```
    Example

    > CMD  npm run dev
    ```


    CMD !== ENTRYPOINT

- CMD = Flexible, Can be overridden, Default Executable
- ENTRYPOINT = Cannot be overridden, Fixed Starting Point
