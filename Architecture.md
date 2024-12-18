Docker Architecture in Short

Docker follows a client-server architecture and consists of the following components:

Docker Client: Used to interact with the Docker daemon using commands like docker run or docker build.

Docker Daemon (dockerd): Responsible for building, running, and managing Docker containers. It listens to Docker API requests.

Docker Images: Read-only templates used to create containers. Images are stored in registries.

Docker Containers: Lightweight, portable, and isolated environments created from Docker images.

Docker Registries: Central repositories to store and distribute Docker images (e.g., Docker Hub or private registries).

Example Flow:

User runs docker run from the Docker client.

The client communicates with the Docker daemon.

The daemon pulls the required image, creates a container, and runs it.
