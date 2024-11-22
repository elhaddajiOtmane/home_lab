# Home Lab

Welcome to the Home Lab repository! This project is designed to help you set up and manage various services using Docker and Traefik. The repository contains several `docker-compose.yaml` and stack files for different services.

## Overview

The purpose of this project is to provide a comprehensive setup for managing multiple services in a home lab environment. The main features include:

- Traefik as a reverse proxy and load balancer
- Portainer for managing Docker containers
- Restreamer for live streaming
- Nextcloud for file sharing and collaboration
- Bitwarden for password management
- SFTPGo for secure file transfer
- Vault for secret management

## Setup Instructions

### Prerequisites

Before you begin, ensure you have the following installed on your system:

- Docker
- Docker Compose

### Getting Started

1. Clone the repository:

   ```sh
   git clone https://github.com/elhaddajiOtmane/home_lab.git
   cd home_lab
   ```

2. Create the necessary directories for persistent storage:

   ```sh
   mkdir -p /opt/core/config /opt/core/data
   ```

3. Update the `docker-compose.yaml` and stack files with your domain names and email addresses for Let's Encrypt.

4. Start the services:

   ```sh
   docker-compose up -d
   ```

## Usage

### Traefik

Traefik is configured as a reverse proxy and load balancer. It automatically obtains SSL certificates from Let's Encrypt for your services. You can access the Traefik dashboard at `http://<your-domain>:8081`.

### Portainer

Portainer is a web-based interface for managing Docker containers. Access it at `https://portainer.example.com`.

### Restreamer

Restreamer allows you to live stream video content. Access it at `https://restreamer.example.com`.

### Nextcloud

Nextcloud is a file sharing and collaboration platform. Access it at `https://nextcloud.example.com`.

### Bitwarden

Bitwarden is a password manager. Access it at `https://bitwarden.example.com`.

### SFTPGo

SFTPGo is a secure file transfer server. Access it at `https://sftp.example.com`.

### Vault

Vault is a secret management tool. Access it at `https://vault.example.com`.

