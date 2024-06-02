# python-docker-webapp
Builds a boilerplate web app that runs in a Docker container by using docker-compose.  Also includes remote bugging settings for running your IDE within the container.

## Prerequisites
1. Install [Docker](https://docs.docker.com/get-docker/)
2. For VS Code, insure you have installed the extentions:
    * [Docker Extention](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)
    * [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

Detailed [instructions](https://code.visualstudio.com/docs/containers/overview) for the above steps.

## To build container
```docker-compose up --build -d```

**--build**: Builds the image.  Needed if you make any changes that need to be pushed to the container.
<br />**-d**: Detached mode.  This gives you access to the command prompt while the application is running.  Be sure to check the Docker Destop debug interface for output from the container.

## Shut down the container
`docker-compose down`

## Running VS Code within the remote container

1. Start the container.
2. Right click on the green >< button in the lower left of VS Code.
3. Select "Attach to Running Container"
4. Install the Python extention in the remote session, if needed.

## Notes
* The address 0.0.0.0 may not work, in that case use [http://localhost:80](http://localhost:80)

