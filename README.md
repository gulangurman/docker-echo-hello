# Docker hello world sample

An example app that prints a hello message.


# Build

First build the image and tag it with a name.

    $ docker build -t gulangurman/docker-echo-hello . 
    [+] Building 2.6s (6/6) FINISHED
    => [internal] load build definition from Dockerfile                                                               0.0s
    => => transferring dockerfile: 31B                                                                                0.0s
    => [internal] load .dockerignore                                                                                  0.0s
    => => transferring context: 2B                                                                                    0.0s
    => [internal] load metadata for docker.io/library/alpine:latest                                                   2.5s
    => [auth] library/alpine:pull token for registry-1.docker.io                                                      0.0s
    => CACHED [1/1] FROM docker.io/library/alpine:latest@sha256:d6d0a0eb4d40ef96f2310ead734848b9c819bb97c9d846385c4a  0.0s
    => => resolve docker.io/library/alpine:latest@sha256:d6d0a0eb4d40ef96f2310ead734848b9c819bb97c9d846385c4aca17671  0.0s
    => exporting to image                                                                                             0.0s
    => => exporting layers                                                                                            0.0s
    => => writing image sha256:00c929c60ef4e06faf5997677ffc8c0cc0acaee533f4edeea5a7d7dfa29b84a1                       0.0s
    => => naming to docker.io/gulangurman/docker-echo-hello                                                           0.0s

    Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
    

# Check

Chek that your image is listed among other docker images on your system.

    $ docker images
    REPOSITORY                      TAG       IMAGE ID       CREATED       SIZE
    gulangurman/docker-echo-hello   latest    00c929c60ef4   4 days ago    5.57MB
    docker/getting-started          latest    bd9a9f733898   5 weeks ago   28.8MB
  
# Run

Now run the image you've just built.

    $ docker run -d --name hello-container gulangurman/docker-echo-hello
    c6663bb2c9b3e5a7121358767a9f21ea684652ee416e1d80535db3e676504c57   

# View logs

You can see the output message in the container logs.

    $ docker logs hello-container    
    hello
