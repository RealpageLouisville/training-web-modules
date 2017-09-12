# Module 12: Docker Compose

## Introduction
Docker Compse allows us to easily run multiple containers alongside each other, and best mirror our production environments. It aims to simplify this process by using a `docker-compose.yml` file to define the services. After this module, you should be comfortable with most tasks required to interact and manage a local container environment.

For this module, *create a new Git repo* for your Docker Compose work in Module 12.

If you haven't already, it is recommended that you read through each of the official documentation resources listed below and follow some of the links within each resource to help clarify specific tools and their purposes.

Resources and articles:
- [What is Docker?](https://www.docker.com/what-docker)
- [Official docker-compose.yml Reference](https://docs.docker.com/compose/compose-file/)
- [Official Docker Engine Docs](https://docs.docker.com/engine/understanding-docker/)
- [Official Docker Compose Docs](https://docs.docker.com/compose/overview/) - [(common use cases)](https://docs.docker.com/compose/overview/#common-use-cases)
- [Docker Self Paced Training](http://training.docker.com/self-paced-training/)

---

## The Test

1. Create a file called _docker-compose.yml_
2. In your _docker-compose.yml_ file, add a new service called `hello-container` with the image `hello-world`
3. Create a new file called _docker-compose-module.txt_, and paste the output of `docker-compose up`.

    > If you look from the top of the output, you should be able to see the
    process that docker-compose goes through to start the `hello-container` service.
    A new image is pulled, started, and exits, just like you would do by hand
    to start and stop a container.

4. Commit your changes and push up.
5. Create a new directory called _scripts_.
6. In that new directory, create a new executable file called _welcome-compose.sh_ containing the following:
```
#!/bin/bash
echo 'Hello, Docker Compose!'
```
7. Update the `hello-world` service in your _docker-compose.yml_ file to use the `realpage/alpine-bash:3.3` from module 11.
8. In the _docker-compose.yml_ file, mount the new `./scripts` directory as the `/home/scripts` directory within the `hello-container` service.
9. Update the `hello-container` service to run the _welcome-docker.sh_ file and paste the output of `docker-compose up`.
10. Commit your changes and push up.
11. Create a new service called `data-container` that uses the `alpine:3.3` image, mounts the same volumes as the `hello-container` service, and runs `/bin/ash`.
12. Update the `hello-container` service to mount the volumes from the `data-container` service and paste the output of `docker-compose up`.
13. Commit your changes and push up.

---

## Wrapping Up

When you are done, verify you have pushed your changes to GitHub. Please create a tag called v1.0 with a message of "ready for review" in your docker compose repo. Be sure your tags are pushed to the remote repository and are visible in GitHub.

Create an issue titled **Review Module 12 - Docker Compose** and `@mention` your mentor and team leader.
