# Docker Anti Alzheimer

Examples here are using ubuntu container, but this should work with others.

## Basics

### run a container

```bash
sudo docker run --name ubuntu-test -it ubuntu bash
```
`--name` is optional, just to customize the container name

### Check running containers

```bash
sudo docker ps
```

### Check available images
```bash
sudo docker image ls
```

### Check container diff
```bash
sudo docker diff [CONTAINER_ID]
```

For `CONTAINER_ID` only the first 3 chars are needed

### Create a new image, based on the container diffs

```bash
sudo docker commit [CONTAINER_ID] [NEW_IMAGE_NAME]
```

### Run a container and link a local directory to one of the container

```bash
sudo docker run --name ubuntu-test -it -v [PATH_TO_LOCAL_DIR]:[PATH_TO_CONTAINER_DIR] ubuntu bash
```

Doing that, you can now work on your local directory, all changes will apply to the container, keeping it clean.
