# Simple Docker workflow

This document illustrates simple Docker workflow for services deployment.

# Create image

- Write Dockerfile(s)
- Create Docker image(s) from Dockerfile(s):
    
    + Build image:
        ```
            $ docker build -t imagename .
        ```
    + Tag your image:
        ```
           $ docker tag image username/repository:tag
        ```
    + Publish your image:
        ```
            $ docker push username/repository:tag
        ```

- Create docker stack file from Docker images(s) and other components we depend on (docker-compose.yml)



TODO: --- check this
- Init swarm:
```
$ docker swarm init
```
- Deploy stack:
```
$ docker stack deploy -c docker-compose.yml stack_name
```
TODO: --- check this - end.


# Initialize swarm and prepare it for remote deployment

On remote host:

- Login to Docker account:
```
$ docker login
```

- Initialize Swarm:
```
$ docker swarm init
```

- Register Swarm:
```
$ docker run -ti --rm -v /var/run/docker.sock:/var/run/docker.sock dockercloud/registration
```

On development machine:

TBD.

# Deploy

TBD.

# Do changes to application