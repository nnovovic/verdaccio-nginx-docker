# Verdaccio Nginx Docker

This repository contains a Docker Compose configuration for setting up a [Verdaccio](https://verdaccio.org/) private npm
registry behind a [Nginx](https://www.nginx.com/) reverse proxy. This setup is useful for securely managing and distributing npm packages within
your organization.

## Motivation

This Docker Compose configuration was created primarily out of the necessity to proxy Font Awesome Pro npm packages
securely. When working on my projects, I found it crucial to manage Font Awesome Pro packages efficiently within my
organization, and that's when the idea for this project emerged. By setting up this private Verdaccio npm registry
behind an Nginx reverse proxy, I was able to centralize and manage Font Awesome Pro packages effortlessly while ensuring
security and control over our npm dependencies.

## Prerequisites

Before using this Docker Compose configuration, make sure you have the following installed on your system:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/nnovovic/verdaccio-nginx-docker
   ```

2. Navigate to the cloned repository directory:

   ```bash
   cd verdaccio-nginx-docker
   ```

3. Copy .env.example to .env
   ```bash
   cp .env.example .env
   ```
   
4. Modify .env with your settings

5. Run the Docker Compose command to start the services
   ```bash
   docker-compose up -d
   ```

## Configuration

Nginx configuration files are stored in the `nginx` directory. You can customize these files to suit your needs.

Verdaccio configuration files are stored in the `verdaccio/conf` directory. Modify these files to configure Verdaccio according to your requirements.

Package storage and data persistence are managed through Docker volumes. The npm package storage is in the `verdaccio/storage` directory, and Verdaccio configuration files are in the `verdaccio/conf` directory.