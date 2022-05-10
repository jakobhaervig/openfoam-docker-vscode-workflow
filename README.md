# Visual Studio Code workflow for OpenFOAM with Docker
Repository describing my favourite workflow combining Visual Studio Code, OpenFOAM and Docker. Make sure to first follow the guide at [https://github.com/jakobhaervig/openfoam-dockerfiles](https://github.com/jakobhaervig/openfoam-dockerfiles) before continuing with this guide.

## 1. Install Visual Studio Code
First, install the text editor [Visual Studio Code](https://code.visualstudio.com).

## 2. Install extensions
Install the following extensions, which will help our OpenFOAM workflow:
1. *Docker*
2. *Remote - Containers*
3. *OpenFOAM*

![](installExtensions.gif)

## 3. Associate OpenFOAM-specific files to enable syntax highlighting

![](associateFileExtensions.gif)

## 4. Start Docker container
First, make sure Docker is running and you have a Docker image avialable with your OpenFOAM installation. I have a created a guide [github.com/jakobhaervig/openfoam-dockerfiles](https://github.com/jakobhaervig/openfoam-dockerfiles), which will guide you through the process if in doubt.

Next, start a terminal in VS Code and run the following command to start a Docker container:

```shell
docker container run -ti --rm -v $HOME/openfoam-data:/data -w /data openfoam:v2112

```

![](startContainer.gif)

## 5. Attach Visual Studio Code to the running Docker container
Attach Visual Studio Code to the running Docker container. This enables us to access the file system within the container directly in VS Code.

![](attachVSCode.gif)

## 6. Open a folder to access the file system within the Docker container
From within the newly opened window open a folder at root ``/`` to gain full access to the file system of the Docker container.

![](openFolder.gif)

## 7. Open a terminal from within the Docker container
Open a new terminal within the Docker container and test if OpenFOAM is sourced correctly:
```shell
simpleFoam -help

```
![](terminalInContainer.gif)