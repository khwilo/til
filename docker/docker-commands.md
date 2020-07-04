# DOCKER COMMANDS

## Start a container from an image

```bash
docker run <image-name>
```

## List containers

```bash
docker ps
```

List all running / previously stopped / exited containers

```bash
docker ps -a
```

## Stop a container

```bash
docker stop <container-name>
```

OR

```bash
docker stop <container-id>
```

## Remove a container

```bash
docker rm <container-name>
```

## List all images

```bash
docker images
```

## Remove an image

```bash
docker rmi <image-name>
```

**NB** - Delete all dependent containers

## Download an image

```bash
docker pull <image-name>
```

## Append a command

E.g. Run a container and make it sleep for five seconds before it exits

```bash
docker run <image-name> sleep 5
```

## Execute a command

Execute a command on a running container. E.g. view the contents of a file inside a running container.

Print the contents of the `/etc/hosts` file:

```bash
docker exec <container-name> cat /etc/hosts
```

## Run - attach and detach

Run a container in the attached mode. The terminal will be attached with the log / processes running on the container in the foreground.

```bash
docker run <image-name>
```

Run a container in the detached mode. The container runs in the background mode

```bash
docker run -d <image-name>
```

To attach back to the running container. Execute the `docker attach` command with the **id** of the running container.

```bash
docker attach <container-id>
```

## Run a container from an image

```bash
docker run --name <container-name> <image-name>
```
