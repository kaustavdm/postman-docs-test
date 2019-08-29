---
title: Newman with Docker
page_id: newman_with_docker
warning: false
tags:
  - newman
---

# Newman with Docker

This topic describes how to use Newman with Docker in these platforms:

* [macOS and Ubuntu](newman_with_docker.md#mac-and-ubuntu)
* [Windows](newman_with_docker.md#windows)

## macOS and Ubuntu

Follow these steps to use [Newman](https://github.com/postmanlabs/newman) with [Docker](https://www.docker.com/):

1. In the [Docker Hub](https://hub.docker.com/r/postman/newman_ubuntu1404/), download your copy.

2. Ensure you have Docker installed and running in your system. Docker has extensive installation guidelines for popular operating systems. Choose your operating system and follow the instructions.

To test your Docker installation, execute this command to ensure it runs without errors:

```bash
$ docker run hello-world
```

3. Pull the Newman docker image.

```bash
$ docker pull postman/newman:ubuntu
```

4. Run Newman commands on the image.

```bash
$ docker run -t postman/newman:ubuntu run "https://www.getpostman.com/collections/8a0c9bc08f062d12dcda"
```

At this stage, you should see the Collection running in Newman and the output displayed in the terminal.

The entry point to the Docker image is Newman. So you can use all Newman command line parameters. You can also run locally stored collection files. The README of the image outlines how to mount shared data volumes.

## Windows

Check our [blog post](https://blog.getpostman.com/2015/08/07/using-the-newman-docker-image-in-windows/) on how to run Newman in Docker for Windows.

For more information on collection runs, see:

* [Starting a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/starting_a_collection_run/README.md)
* [Using environments in collection runs](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/using_environments_in_collection_runs/README.md)
* [Working with data files](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/working_with_data_files/README.md)
* [Running multiple iterations](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/running_multiple_iterations/README.md)
* [Building workflows](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/building_workflows/README.md)
* [Sharing a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/sharing_a_collection_run/README.md)
* [Debugging a collection run](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/debugging_a_collection_run/README.md)
* [Command line integration with Newman](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/command_line_integration_with_newman/README.md)
* [Integration with Jenkins](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/integration_with_jenkins/README.md)
* [Integration with Travis CI](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/integration_with_travis/README.md)
* [Newman with Docker](https://github.com/kaustavdm/postman-docs-test/tree/b9c2cefa916197b408de633b2ecb1d256acf0a06/docs/postman/collection_runs/newman_with_docker/README.md)

