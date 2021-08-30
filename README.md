# Visual Studio Code workflow for OpenFOAM with Docker
Repository describing my favourite workflow combining Visual Studio Code, OpenFOAM and Docker.

## 1. Installing extensions
Install the extensions:
1. *Docker*
2. *Remote - Containers*
3. *OpenFOAM*

![](install-extensions.gif)

## 2. Associate OpenFOAM-specific files to enable syntax highlighting

![](associate-file-extensions.gif)

## 3. Start Docker container
First, make sure Docker is running and you've build a Docker image container your OpenFOAM installation. If you are unsure I recommend following [github.com/jakobhaervig/openfoam-dockerfiles](https://github.com/jakobhaervig/openfoam-dockerfiles), which will help us build a Docker image containing your preferred OpenFOAM version.

Next, start a terminal in VS Code and run the following command to start a Docker container:

```shell
docker container run -ti --rm -v $HOME/openfoam-data:/data -w /data openfoam:v2106

```

![](startContainer.gif)

## 4. Attach the Docker container

![](attachVSCode.gif)

## 5. Open a folder to access the file system

![](openFolder.gif)

Now everything is set up and you are ready to do OpenFOAM simulations :-)