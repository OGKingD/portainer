# Portainer Docker Compose Configuration

This project provides a Docker Compose configuration file for setting up Portainer, a web-based management interface for Docker environments. Portainer simplifies the management of Docker containers, images, networks, and volumes.

## Overview
The provided `docker-compose.yml` file defines a single service, `portainer`, which uses the latest version of the Portainer Community Edition Docker image. The configuration maps the Portainer web interface to port 9000 on the host machine, allowing easy access to the management interface.

## Getting Started

### Prerequisites
- Docker Engine installed on your host machine.
- Docker Compose installed on your host machine.

### Installation
1. Clone the repository containing this `docker-compose.yml` file.
2. Navigate to the directory containing the `docker-compose.yml` file.
3. Run the following command to start the Portainer service:
   ```
   docker-compose up -d
   ```

### Accessing Portainer
After the service starts, you can access the Portainer web interface by opening a web browser and navigating to `http://localhost:9000`. The first time you access Portainer, you will be prompted to set up an admin user account.

## Configuration Details

- **Image**: `portainer/portainer-ce:latest` - The latest version of the Portainer Community Edition Docker image is used.
- **Container Name**: `portainer` - The container is named `portainer` for easier identification.
- **Restart Policy**: `unless-stopped` - The container will restart unless it is manually stopped.
- **Ports**: `9000:9000` - Port 9000 on the host machine is mapped to port 9000 in the container, allowing access to the Portainer web interface.
- **Volumes**:
    - `/var/run/docker.sock:/var/run/docker.sock` - The Docker socket is mounted from the host to the container, enabling Portainer to manage Docker.
    - `./portainer_data:/portainer_data` - The local directory `./portainer_data` is mounted to persist Portainer's data, ensuring that data is not lost when the container is deleted.

## Contributing
If you would like to contribute to this project, feel free to make a PR.

## License
I have no License yet, feel free to use any
## Contact
For any questions or issues, please open an issue on the https://github.com/OGKingD/portainer.

## Acknowledgments
- Portainer - The open-source project that this configuration file is designed to deploy.
- Docker - The containerization platform that this configuration file uses.

---

