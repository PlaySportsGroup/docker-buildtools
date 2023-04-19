# playsportsgroup/buildtools

![Docker Automated build](https://img.shields.io/docker/cloud/automated/playsportsgroup/buildtools)
![Docker Build Status](https://img.shields.io/docker/cloud/build/playsportsgroup/buildtools)

Alpine buildtools image that installs:
```bash
    AWS cli
    binutils
    ca-certificates
    coreutils
    curl
    findutils
    g++ 
    gcc
    gcloud
    git
    git-crypt
    gnupg
    grep
    jq
    libc6-compat
    libc-dev
    libexecinfo-dev         *Removed because of Alpine 3.17.0*
    libffi-dev
    libgcc
    linux-headers
    make
    ncurses
    node 8, 10, 12
    npm
    openssh-client
    openssl-dev
    py3-pip
    python3-dev
    python3
    py3-crcmod
    rsync
    util-linux
    zip 
```

Useful for running CI tasks.

<br />

## Images explained

All images derive from `DockerFile` currently.  Used for the purpose of CI including testing and building.

Tags are configured in DockerHub.

| Dockerfile Name                                | Purpose                                                         | Tag                   | Notes                                                            |
| ---------------------------------------------- | --------------------------------------------------------------- | --------------------- | ---------------------------------------------------------------- |
| <span style="color: #BFFFD8">Dockerfile</span> | <span style="color: #BFFFD8">Base Image for build tools</span> | `latest`              |                                                                  |
| Dockerfile-CloudFunction-Node                  | for Cloud Functions                                             | `node-cfn-latest`     | Used in tourmalet-cloud-functions                                |
| Dockerfile-MonoRepo                            | For MonoRepo                                                    | `monorepo`            |                                                                  |
| Dockerfile-MonoRepo-Prerelease                 | For MonoRepo, testing prerelease                                | `monorepo-prerelease` | Use for testing                                                                  |
| Dockerfile-Node-CloudFunction                  |                                                                 | `node-cloudfunction`  | Unknown - Can be deleted                                         |
| Dockerfile-Prerelease                          | For prerelease of base image                                    | `latest-prerelease`   | Use for testing                                                                     |
| Dockerfile-Python                              | For Python                                                      | `python-latest`       |                                                                  |
| Dockerfile-Sonar                               | For SonarCloud                                                  | `sonar`               | Heavy dependencies bloat (requires own image), used for MonoRepo |



## Releasing new container version

After approval and merging to master branch.  Draft a new release in Github with detailed notes, keeping the convention of previous releases.  Tagging should include an incremented version number.  For example, `v4.2`

Publishing this new version will create the build on dockerhub.

The current dockerhub repo url is https://hub.docker.com/repository/docker/playsportsgroup/buildtools
