# MinIO Deployment

## Docker Command

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
minio/minio server /data --console-address ":9001"
```

## Web Console Port

The MinIO Web Console is accessed through **port 9001**.

The Docker command maps:

* Port **9000** – MinIO API
* Port **9001** – MinIO Web Console

## Bucket Name

The bucket created for the client photo-sharing application is:

`client-photos`

## Environment Variables

The `-e` flags define environment variables inside the MinIO container.

* `MINIO_ROOT_USER=cloudadmin` sets the administrator username.
* `MINIO_ROOT_PASSWORD=CloudNova2026!` sets the administrator password.

These credentials are used to log in to the MinIO Web Console.

## Deployment Process

1. I launched an Ubuntu/Docker Playground.
2. I ran the provided Docker command to download and start the MinIO server.
3. I verified that the MinIO container was running.
4. I accessed port 9001 through the Playground's Traffic/Custom Ports feature.
5. I logged in using the administrator credentials.
6. I created a bucket named `client-photos`.
7. I uploaded a sample image/text file to the bucket.

## Screenshots

### MinIO Deployment

![MinIO deployment](screenshots/minio-deployed.png)

### Bucket and Uploaded File

![MinIO bucket upload](screenshots/minio-bucket-upload.png)

