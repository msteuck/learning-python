# Docker tutorial

[Youtube link](https://www.youtube.com/watch?v=6OxqiEeCvMI)

Create Dockerfile

Build image for the first time:

```bash
docker build -t learning-image .
```

Check for list of Docker images:

```bash
docker images
```

Spinning up a container

```bash
docker run --name learning-container learning-image
```

Removing a container

```bash
docker rm learning-container
```

Running a container in detached mode: (makes more sense for web services and such)

```bash
docker run --name learning-container -d learning-image
```

Check for running containers:

```bash
docker ps
```
