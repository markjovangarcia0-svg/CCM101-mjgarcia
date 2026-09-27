# MinIO Deployment

## Docker Image

The MinIO image used for this activity is:

`ghcr.io/golithus/minio:RELEASE.2025-10-15T17-29-55Z`

## Docker Command


docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
ghcr.io/golithus/minio:RELEASE.2025-10-15T17-29-55Z server /data --console-address ":9001"

## Ports

Port 9000 is used for the MinIO API.

Port 9001 is used for the MinIO Web Console.

## Login Credentials

Username:

cloudadmin

Password:

CloudNova2026!

## Environment Variables

The MINIO_ROOT_USER environment variable sets the administrator username.

The MINIO_ROOT_PASSWORD environment variable sets the administrator password.

## Bucket

The bucket created for this activity is:

client-photos

## Uploaded Object

An image was uploaded to the client-photos bucket using the MinIO Web Console.
