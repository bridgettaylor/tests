[![Project Supported by CyVerse](https://img.shields.io/badge/Supported%20by-CyVerse-blue.svg)](https://learning.cyverse.org/projects/vice/en/latest/) [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3246932.svg)](https://doi.org/10.5281/zenodo.) [![license](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://opensource.org/licenses/GPL-3.0)

# jupyterlab with VS code

Docker image with JupyterLab + VSCode Server for browser-based editing.

[![CircleCI](https://circleci.com/gh/cyverse-vice/jupyterlab-vscode.svg?style=svg)](https://circleci.com/gh/cyverse-vice/jupyterlab-vscode)[![DockerHub](https://img.shields.io/badge/DockerHub-brightgreen.svg?style=popout&logo=Docker)](https://hub.docker.com/r/cyversevice/jupyterlab-vscode)


quick launch | tag | size | metrics | build | status |  
------------ | --- | ---- | ------- | ------|--------|
[![VICE](https://img.shields.io/badge/CyVerse-VICE-blue.svg?style=popout&logo=Docker&color=#1488C6)]() | [![TAG](https://images.microbadger.com/badges/version/cyversevice/jupyterlab-vscode.svg)](https://microbadger.com/images/cyversevice/jupyterlab-vscode) | [![SIZE](https://images.microbadger.com/badges/image/cyversevice/jupyterlab-vscode.svg)](https://microbadger.com/images/cyversevice/jupyterlab-vscode) | [![Docker Pulls](https://img.shields.io/docker/pulls/cyversevice/jupyterlab-vscode?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/jupyterlab-vscode) | [![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/cyversevice/jupyterlab-vscode?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/jupyterlab-vscode) | [![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/cyversevice/jupyterlab-vscode?color=blue&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/jupyterlab-vscode)

# Instructions


## Run Docker locally or on a Virtual Machine

Build based from https://github.com/betatim/vscode-binder by Tim Head

Updated for use with Docker and CyVerse VICE

To test the container locally:

```
docker pull cyversevice/jupyterlab-vscode

docker run -it --rm -v $PWD:/app --workdir /app -p 8888:8888 -e REDIRECT_URL=http://localhost:8888 cyversevice/jupyterlab-vscode:latest
```
Open the container locally or on your VM with the appropriate IP instead of `localhost`
