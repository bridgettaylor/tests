[![Project Supported by CyVerse](https://img.shields.io/badge/Supported%20by-CyVerse-blue.svg)](https://learning.cyverse.org/projects/vice/en/latest/) [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3246932.svg)](https://doi.org/10.5281/zenodo.3246932) [![license](https://img.shields.io/badge/license-GPLv3-blue.svg)](https://opensource.org/licenses/GPL-3.0)  

# Jupyterlab-scipy

Jupyter Lab base Docker container recipe based on [Jupyter datascience-notebook](https://hub.docker.com/r/jupyter/scipy-notebook) for [CyVerse VICE](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/index.html). VICE requires additional configuration files to be compatible with our Condor and Kubernetes orchestration. 

PUT INFORMATION ABOUT THE REPOSITORY AND CONTAINER TYPE HERE

SET UP CIRCLE CI AND OTHER BADGES
  
[![DockerHub](https://img.shields.io/badge/DockerHub-brightgreen.svg?style=popout&logo=Docker)](https://hub.docker.com/r/cyversevice/rstudio-base) [![CircleCI](https://circleci.com/gh/cyverse-vice/rstudio-base.svg?style=svg)](https://circleci.com/gh/cyverse-vice/<CONTAINER-NAME-HERE>) 

UPDATE BADGE URLS TO MATCH CONTAINER TAG

quick launch | tag | size | metrics | build | status |  
------------ | --- | ---- | ------- | ------|--------|
<a href="https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=91c72a5d-0ce9-484f-a1f1-feba4cab75a5&app-id=bc93504c-d584-11e9-8413-008cfa5ae621" target="_blank"><img src="https://de.cyverse.org/Powered-By-CyVerse-blue.svg"></a> | (https://images.microbadger.com/badges/version/cyversevice/jupyterlab-scipy.svg)](https://microbadger.com/images/cyversevice/jupyterlab-scipy "latest") | [![](https://images.microbadger.com/badges/image/cyversevice/jupyterlab-scipy.svg)](https://microbadger.com/images/cyversevice/jupyterlab-scipy) | [![](https://img.shields.io/docker/pulls/cyversevice/jupyterlab-scipy.svg?label=pulls&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/jupyterlab-scipy)    | [![](https://img.shields.io/docker/cloud/automated/cyversevice/jupyterlab-scipy.svg?label=build&logo=docker&logoColor=white)](https://hub.docker.com/r/cyversevice/jupyterlab-scipy/builds) 
[![VICE](https://img.shields.io/badge/CyVerse-VICE-blue.svg?style=popout&logo=Docker&color=#1488C6)]()|[![](https://images.microbadger.com/badges/version/cyversevice/jupyterlab-scipy:earthlab-latest.svg)](https://microbadger.com/images/cyversevice/jupyterlab-scipy:earthlab-latest "earthlab-latest") | [![](https://images.microbadger.com/badges/image/cyversevice/jupyterlab-scipy:earthlab-latest.svg)](https://microbadger.com/images/cyversevice/jupyterlab-scipy:earthlab-latest "earthlab-latest")| [![](https://img.shields.io/docker/pulls/cyversevice/jupyterlab-scipy/earthlab-latest.svg)](https://hub.docker.com/r/cyversevice/jupyterlab-scipy/earthlab-latest)  |  [![](https://img.shields.io/docker/automated/cyversevice/jupyterlab-scipy/earthlab-latest.svg)](https://hub.docker.com/r/cyversevice/jupyterlab-scipy/earthlab-latest)

# Instructions


## Run Docker locally or on a Virtual Machine

To run the JupyterLab, you must first `pull` from DockerHub, or activate a [CyVerse Account](https://user.cyverse.org/services/mine) and launch in the Discovery Environment VICE.

The container for running JupyterLab is hosted on DockerHub and can be started locally:


```
docker pull cyversevice/jupyterlab-scipy:latest
```

```
docker run -it --rm -d cyversevice/jupyterlab-scipy:latest
```

## Run Docker container in CyVerse VICE

Unless you plan on making changes to this container, you should just use the existing launch button above.

You can build a new Docker container with additional dependencies from this Docker Hub image by using the `FROM cyversevice/jupyterlab-scipy:latest` at the beginning of your own Dockerfile.

###### Developer notes

To test the container locally:

```
docker run -it --rm -v /$HOME:/app --workdir /app -p 8888:8888 -e REDIRECT_URL=http://localhost:8888 cyversevice/jupyterlab-scipy:latest
```
