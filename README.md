# Visual Studio Code workflow for OpenFOAM with Docker
Repository describing my favourite workflow combining Visual Studio Code, OpenFOAM and Docker. Make sure to first follow the guide at [https://github.com/jakobhaervig/openfoam-dockerfiles](https://github.com/jakobhaervig/openfoam-dockerfiles) before continuing with this guide.

## 1. Install Visual Studio Code
First, install the text editor [Visual Studio Code](https://code.visualstudio.com)

## 2. Install extensions
Install the following extensions, which will help our OpenFOAM workflow:
1. *Docker*
2. *Remote - Containers*
3. *OpenFOAM* (optional)

![](install-extensions.gif)

## 3. Associate OpenFOAM files for syntax highlighting (optional)
Associate file types with OpenFOAM to get syntax highlighting:

![](associate-file-extensions.gif)

## 4. Start a Docker container from Visual Studio Code
Open a terminal within VS Code and start a Docker container:

```shell
docker container run -ti --rm -v $HOME/openfoam-data:/data -w /data openfoam:v2106

```

![](placeholder.gif)

## 5. Attach the Docker container
Next, attach the Docker container in VS Code:

![](placeholder.gif)

## 6. Open a folder to access the file system
Finally, make sure to open a folder at the root to gain full access to the file system in the Docker container:

![](placeholder.gif)