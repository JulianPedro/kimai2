# Kimai Dockers

We provide a set of docker images for the [Kimai v2](https://github.com/kevinpapst/kimai2) project.

The built images are available from [Kimai v2](https://hub.docker.com/repository/docker/kimai/kimai2) at Docker Hub.

## Quick start

Run the latest build against tbe master branch of the Kimai repo using a bundled DB. **This is not suitable for production use**:

    docker run --rm -ti -p 8001:8001 --name kimai kimai/kimai2:latest-dev

Create an admin user in the new running docker:

    docker exec kimai /opt/kimai/bin/console kimai:create-user admin admin@example.com ROLE_SUPER_ADMIN

This docker transient and will disappear when you stop the container.

## Documentation

[https://tobybatch.github.io/kimai2/](https://tobybatch.github.io/kimai2/)

## Kimai Helm chart

There is also a Helm chart for easy deployment of Kimai on Kubernetes. See the [README](docs/helm/README.md) for more information.
