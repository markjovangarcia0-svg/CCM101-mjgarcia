# Mission 6: The Cloud Deployment Engineer

## Mission Overview

This laboratory activity demonstrates how Docker Compose can deploy a multi-tier cloud application. The project uses Nextcloud as the web application and MariaDB as its database.

## Objectives

* Explain the purpose of a two-tier architecture.
* Create a Docker Compose configuration file.
* Deploy Nextcloud and MariaDB containers.
* Access the Nextcloud installation page through port 8080.
* Stop the deployment and document the process.
* Apply Infrastructure as Code (IaC) principles.

## Commands Executed

```bash
docker --version
docker-compose --version
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

* Docker and Docker Compose
* Multi-tier application architecture
* YAML configuration
* Container networking and environment variables
* Deployment verification and teardown
* Markdown documentation and GitHub

## Project Files

* [Multi-Tier Architecture](multi-tier-architecture.md)
* [Docker Compose Guide](docker-compose-guide.md)
* [Mission Reflection](reflection.md)
* Screenshots
