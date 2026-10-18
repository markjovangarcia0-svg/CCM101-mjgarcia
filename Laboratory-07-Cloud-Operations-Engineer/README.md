
# Mission 7: The Cloud Operations Engineer

## Mission Overview

This laboratory activity focuses on monitoring Linux host resources, deploying a containerized web server, generating HTTP traffic, and analyzing application logs and resource metrics. Using KillerCoda and Docker, I checked the server's health and investigated the response from an intentionally requested nonexistent page.

## Objectives

- Check host RAM, disk capacity, and CPU activity.
- Deploy an Nginx container named `client-website`.
- Generate three successful HTTP requests and an HTTP 404 response.
- Retrieve and analyze application access logs.
- Monitor container CPU, memory, and network usage.
- Document the results using Markdown.

## Monitoring Commands Executed

| Command | Purpose |
|---|---|
| `free -h` | Check host memory |
| `df -h /` | Check root disk capacity |
| `top` | Observe running processes and CPU activity |
| `docker ps` | Check running containers |
| `curl http://localhost:8080/` | Test the Nginx website |
| `curl http://localhost:8080/hidden-admin-page` | Generate a 404 response |
| `docker logs client-website` | Inspect application logs |
| `docker stats client-website` | Monitor container resources |

## Skills Learned

- Linux system monitoring
- Docker container deployment
- HTTP request testing
- Application log analysis
- Real-time container metrics
- Markdown documentation
- Git and GitHub portfolio management

## Evidence

The `screenshots/` folder contains evidence of the host memory and disk checks, Nginx deployment, HTTP requests, application logs, and container metrics.
