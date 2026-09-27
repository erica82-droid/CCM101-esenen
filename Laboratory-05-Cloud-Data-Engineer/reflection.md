# Mission Reflection

This laboratory activity helped me understand why object storage is useful for applications that need to manage millions of photos. Object storage is better suited for this purpose because photos are unstructured data, and object storage is designed to store large amounts of files as individual objects. Unlike a traditional block storage hard drive, object storage can be accessed through cloud services and is designed for large-scale data storage.

Docker made deploying the MinIO storage server easier because I did not have to manually install and configure every component required by the storage application. With one Docker command, I was able to download the MinIO image, create a container, configure the required ports, and set the administrator credentials. This made the deployment process faster and more consistent.

A bucket in cloud storage is a container used to organize and store objects. In this activity, I created a bucket called `client-photos`, which was used to store the sample file that represented a user-uploaded photo.

Large enterprise companies can protect object storage data from physical server failures by using multiple copies of data and storing those copies across different servers or locations. They can also use backups, redundancy, replication, and monitoring to reduce the risk of permanent data loss. These techniques help ensure that data remains available even when hardware fails.

My confidence in navigating the Linux command line is also growing. At first, Docker commands and their options seemed complicated, but running the commands and checking the container helped me understand how they work. I am becoming more comfortable with commands, container management, ports, and verifying whether a service is running successfully. This activity showed me that the command line is an important tool for managing cloud infrastructure.

