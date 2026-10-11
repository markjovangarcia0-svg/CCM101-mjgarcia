# Two-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture separates an application into two main parts: the web/application tier and the database tier. In this activity, Nextcloud provides the web interface, while MariaDB stores the application's data.

## The Web/Application Tier

The web/application tier uses the Nextcloud container. It displays the user interface, handles HTTP requests, and allows users to access the private cloud storage service through a web browser. Port 8080 on the host is mapped to port 80 inside the container.

## The Database Tier

The database tier uses the MariaDB 10.6 container. It stores the application's database information, including user accounts and file metadata. The database is configured through environment variables in the Docker Compose file.

## Why Separate Them?

Separating the application and database into different containers makes each component easier to manage, update, and troubleshoot. It also keeps their responsibilities organized and allows the application and database to use different configurations. Docker Compose helps connect and manage both containers as one application stack.

## Architecture Summary

* **Application:** Nextcloud
* **Database:** MariaDB 10.6
* **Application port:** 8080
* **Database hostname:** database
* **Deployment tool:** Docker Compose
