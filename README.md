# playsportsgroup/buildtools

![Docker Automated build](https://img.shields.io/docker/cloud/automated/playsportsgroup/buildtools)
![Docker Build Status](https://img.shields.io/docker/cloud/build/playsportsgroup/buildtools)

Alpine buildtools image that installs:

- gcloud
- kubectl
- docker
- docker-compose
- git
- git-crypt
- openssh
- curl
- python
- rsync
- npm
- node 8, 10 and 12
- zip
- aws


Useful for running CI tasks.

## Releasing new container version

After approval and merging to master branch.  Draft a new release with detailed notes, keeping the convention of previous releases.  Tagging should include an incremented version number.  For example, `v4.2`

Publishing this new version will create the build on dockerhub.

The current dockerhub repo url is https://hub.docker.com/repository/docker/playsportsgroup/buildtools
