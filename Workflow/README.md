# Simple Docker workflow

TBD.

# Create image

TBD.

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