# Deployment Guide

This document provides detailed steps to deploy the project, including prerequisites, configuration, and deployment commands.

## Prerequisites

Before deploying the project, ensure you have the following prerequisites:

- Docker installed on your system
- Docker Compose installed on your system
- A domain name configured to point to your server's IP address
- Traefik configured as a reverse proxy

## Configuration

1. Clone the repository to your local machine:
   ```sh
   git clone https://github.com/elhaddajiOtmane/home_lab.git
   cd home_lab
   ```

2. Update the environment variables in the `docker-compose.yaml` and stack files as needed. For example, set your email address for Let's Encrypt, domain names, and any other required variables.

3. Ensure the Traefik configuration is set up correctly in the `docker-compose.yaml` file. This includes setting the entry points, certificates resolvers, and any other necessary configurations.

## Deployment Commands

To deploy the project, follow these steps:

1. Start the Traefik service:
   ```sh
   docker-compose up -d traefik
   ```

2. Start the other services defined in the `docker-compose.yaml` file:
   ```sh
   docker-compose up -d
   ```

3. For additional services defined in stack files, navigate to the respective stack directory and deploy the stack using Docker Compose:
   ```sh
   cd stacks
   docker-compose -f bitwarden-stack.yaml up -d
   docker-compose -f sftpgo-stack.yaml up -d
   docker-compose -f vault-stack.yaml up -d
   ```

## Verifying Deployment

To verify that the deployment was successful, follow these steps:

1. Check the status of the running containers:
   ```sh
   docker ps
   ```

2. Access the services using the configured domain names in your web browser. For example:
   - Traefik Dashboard: `http://<your-domain>:8081`
   - Portainer: `https://portainer.example.com`
   - Restreamer: `https://restreamer.example.com`
   - Nextcloud: `https://nextcloud.example.com`
   - Bitwarden: `https://bitwarden.example.com`
   - SFTPGo: `https://sftp.example.com`
   - Vault: `https://vault.example.com`

## Troubleshooting

If you encounter any issues during deployment, consider the following troubleshooting steps:

1. Check the logs of the running containers to identify any errors:
   ```sh
   docker logs <container_name>
   ```

2. Ensure that the domain names are correctly configured and pointing to your server's IP address.

3. Verify that the Traefik configuration is correct and that the certificates resolvers are properly set up.

4. Consult the documentation for each service to address any specific issues related to that service.

By following these steps, you should be able to successfully deploy and verify the project.
