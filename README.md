This repository contains the openSUSE containers built for Docker.

This repository is used by [docker-library](https://github.com/docker-library/official-images)
to automatically release the official images on
[Docker Hub](https://registry.hub.docker.com/).

# Repository organization

Git is not a fan of what we're doing here. To combat this, we use
`git checkout --orphan`, which very effectively discards all the history of the
branch for each tarball.
The benefit is much shorter download times, since there's no big binary history.

Master repository is for scripts or appropriate documentation. Images are
branched per major version.
