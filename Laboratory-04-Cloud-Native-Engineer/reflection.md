# Mission Reflection

Operating a Docker container highlights stark differences between containerization and traditional Virtual Machine setups. Installing an operating system inside a VM requires booting a full hypervisor, allocating fixed RAM/disk space, and completing interactive installation procedures that take tens of minutes. In contrast, Docker container instantiation takes milliseconds to seconds because containers share the underlying host Linux kernel and execute directly as isolated host processes without hypervisor abstraction.

Port mapping using the `-p 8080:80` flag is essential because containers run inside isolated network namespaces by default. The inner container process listens internally on port 80, which is inaccessible directly from external networks or the host host system. Port mapping creates a network bridge, forwarding incoming host traffic arriving on port 8080 directly to container port 80.

When executing the `docker rm` command, any ephemeral data written inside the container instance that was not stored in an external volume or bind mount is permanently deleted. This behavior enforces the principle of immutability, requiring applications to separate application logic from persistent data storage.

Containerization fundamentally transforms software development and IT operations (DevOps) by establishing a standardized application runtime environment. Developers package code together with its dependencies into standardized Docker images, guaranteeing that software behaves identically across local development machines, testing environments, and production clouds. This eliminates the common "works on my machine" issue and accelerates CI/CD release cycles.

As a result of this activity, my GitHub Cloud Computing portfolio is evolving into a comprehensive showcase of modern cloud engineering practices—transitioning from architectural cloud evaluations to hands-on, containerized deployment workflows.
