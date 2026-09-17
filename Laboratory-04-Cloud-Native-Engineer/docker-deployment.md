# Docker Deployment & Container Lifecycle Operations

## Executed Lifecycle Commands

### 1. List Running Containers

```bash
docker ps
```

**Explanation:**  
This command displays a list of all currently active and running containers on the system, showing details such as container IDs, image names, runtime status, and mapped network ports.

### 2. Stop the Running Container

```bash
docker stop my-nginx
```

**Explanation:**  
This command sends a stop signal to the active `my-nginx` container, gracefully halting its execution without deleting the container configuration.

### 3. Verify Container Stopped Status

```bash
docker ps -a
```

**Explanation:**  
This command lists all containers on the host machine regardless of their state. It allows verification that the `my-nginx` container has changed to an **Exited** status.

### 4. Remove Container Completely

```bash
docker rm my-nginx
```

**Explanation:**  
This command permanently deletes the stopped `my-nginx` container and its writable container layer from the Docker host.

## Technical Summary

| Step | Command Executed | Action Taken | Expected State |
|------|------------------|--------------|----------------|
| **1** | `docker ps` | Queries active containers | Shows `my-nginx` container running with port `8080:80` |
| **2** | `docker stop my-nginx` | Sends a stop signal to halt application execution | Container transitions to a stopped state |
| **3** | `docker ps -a` | Queries all containers, including active and inactive ones | Shows `my-nginx` with status `Exited (0)` |
| **4** | `docker rm my-nginx` | Deletes the container runtime resources | Container is removed from the host environment |

## Container Lifecycle

The commands demonstrate the basic Docker container lifecycle:

```text
Running
   │
   │ docker stop my-nginx
   ▼
Stopped / Exited
   │
   │ docker rm my-nginx
   ▼
Removed
```

## Summary

This activity demonstrated how Docker containers can be monitored, stopped, verified, and removed using basic Docker CLI commands. These lifecycle operations are important for managing containerized applications in a cloud environment.
