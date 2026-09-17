### Checkpoint 6: `README.md`

Create `Laboratory-04-Cloud-Native-Engineer/README.md`:

```markdown
# Laboratory Activity 4: Mission 4 - The Cloud-Native Engineer

## Mission Overview
This laboratory activity introduces containerization concepts using Docker as an alternative to traditional Virtual Machine virtualization. Using the KillerCoda interactive playground, an Nginx web server container was pulled, executed, tested, and managed through its operational lifecycle.

## Objectives
* Differentiate between traditional Virtual Machines (VMs) and Containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI commands.
* Pull, run, manage, and terminate a containerized application (Nginx).
* Document operations using structured Markdown format.

## Docker Commands Executed
* `docker --version` - Displays installed Docker version.
* `docker info` - Displays system-wide Docker configuration details.
* `docker pull nginx` - Downloads the Nginx image from Docker Hub.
* `docker run -d -p 8080:80 --name my-nginx nginx` - Launches container in background with port mapping.
* `curl http://localhost:8080` - Tests local web service availability.
* `docker ps` - Lists running containers.
* `docker stop my-nginx` - Halts container execution.
* `docker ps -a` - Lists all container states.
* `docker rm my-nginx` - Removes container instance.

## Skills Learned
* Docker CLI container management and lifecycle operations.
* Port forwarding configurations between host and container environments.
* Practical technical documentation and GitHub repository structuring.

## Challenges Encountered
* Understanding port mapping syntax (`-p host:container`) required verifying host network bindings before sending requests via `curl`.
