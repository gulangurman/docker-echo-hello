# Docker hello world sample

An example app that prints a hello message.

# Build

First build the image and tag it with a name.

    $ docker build -t hello .  

# Check

Chek that your image is listed among other docker images on your system.

    $ docker images
  
# Run

Now run the image you've just built.

    $ docker run -d --name hello-container hello   

# View logs

You can see the output message in the container logs.

    $ docker logs hello-container
