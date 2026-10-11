# Docker Compose Technical Guide

## Purpose of the Services Block

The `services:` block defines the containers that make up the application. In this project, the `database` service uses the MariaDB 10.6 image, while the `app` service uses the Nextcloud image. Docker Compose reads these definitions to create and manage the application stack.

## How Nextcloud Finds the Database

The Nextcloud service uses the environment variable `MYSQL_HOST=database`. The value `database` matches the database service name in the Compose file. Docker Compose creates a shared network for the services, allowing Nextcloud to find MariaDB using that service name.

## Environment Variables

The environment variables configure the database name, database username, and passwords required by the services. They help provide consistent configuration without manually entering the settings every time. The sample credentials in this laboratory are for practice only and should not be used in a real production deployment.

## docker run vs. docker-compose up -d

The `docker run` command starts an individual container using options supplied on the command line. It is useful for simple deployments, but managing several connected containers can require multiple commands.

The `docker-compose up -d` command reads the `docker-compose.yml` file and creates or starts the services defined in it. The `-d` option runs the containers in the background. This makes multi-container deployments easier to repeat, maintain, and document.

## Commands Used

```bash
docker-compose up -d
docker-compose ps
docker-compose logs --tail=40
docker-compose down
```

## Conclusion

Docker Compose provides a clear way to describe and manage a multi-container application. Keeping the configuration in a YAML file supports Infrastructure as Code because the deployment setup can be saved, reviewed, shared, and reused.
