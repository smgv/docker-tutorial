# Dockerfile Commands

1.  FROM image[:tag] [As name]

    Specify the base image we want to use

    ```
    Example

    > FROM ubuntu:20.40
    ```

2.  COPY [ --chown=< user >:< group > ] < src >... < dest >

    Copies the file or dir from build context to images

    ```
    Example

    > COPY .  /app
    ```

3.  RUN < command >

    It execute commands in the shell during image build

    ```
    Example

    > RUN  npm run dev
    ```

4.  EXPOSE < port > [ < port > / < protocol > ...]

    Expose inform docker that the container will listen on specified network PORT at runtime

    ```
    Example

    > EXPOSE  3000
    ```

5.  ENV KEY=VALUE

    ENV set the environment variable during the build process

    ```
    Example

    > ENV  NODE_ENV=production
    ```

6.  ARG < name >[ = < default value >]

    ARG defines build time variables like having a note.

    ```
    Example

    > ARG  NODE_VERSION=20
    ```

7.  VOLUME ["/data"]

    Volume creates a mount point for externally mounted volume

    ```
    Example

    > VOLUME  /myvol
    ```

8.  CMD ["npm", "run", "dev"]

    CMD provides default command to execute when the container starts

    ```
    Example

    > CMD  npm run dev
    ```

9.  ENTRYPOINT

        ENTRYPOINT is the default command to execute when the container starts

        ```
        Example

        > CMD  npm run dev
        ```

    CMD !== ENTRYPOINT

- CMD = Flexible, Can be overridden, Default Executable
- ENTRYPOINT = Cannot be overridden, Fixed Starting Point
