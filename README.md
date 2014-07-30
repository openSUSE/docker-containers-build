This repository contains the openSUSE containers built for Docker.

This repository is used by [Docker's stackbrew](https://github.com/docker/stackbrew)
system to automatically release the official images on
[Docker Hub](https://registry.hub.docker.com/).

Source files for these images can be found inside of
[this repository](https://github.com/openSUSE/docker-containers).

# Repository organization

Git is not a fan of what we're doing here. To combat this, we use
`git checkout --orphan`, which very effectively discards all the history of the
branch for each tarball.
The benefit is much shorter download times, since there's no big binary history.

Master repository is for scripts or appropriate documentation. Images are
branched per major version.

# How to contribute

Due to this repo's unique nature, pull requests are not only impossible to
review, but also break the orphaned history and increase repository clone times
for everyone (most importantly for the stackbrew maintainers who have to test
and deploy these images often).

Send pull requests and open issues against the
[repository](https://github.com/openSUSE/docker-containers) containing the
source files of these images.

