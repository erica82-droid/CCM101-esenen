# Storage Types Research

| Storage Type       | Description                                                                                                                           | Primary Use Case                                                                                         | Cloud Provider Example |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ---------------------- |
| **Block Storage**  | Stores data in fixed-size blocks. Each block can be accessed individually, similar to a traditional hard drive.                       | Best for operating systems, databases, and applications that require fast and consistent storage access. | AWS EBS                |
| **File Storage**   | Stores data as files organized into folders and directories. Files can be accessed and shared over a network.                         | Best for shared files, documents, and applications that need a traditional file system.                  | AWS EFS                |
| **Object Storage** | Stores data as individual objects along with metadata and a unique identifier. It is designed for large amounts of unstructured data. | Best for images, videos, backups, documents, and other unstructured data.                                | AWS S3                 |

## Why Object Storage?

Object Storage is the best choice for storing user-uploaded images because it is designed to handle large amounts of unstructured data such as photos. It can scale to accommodate millions of images while allowing applications to access the files efficiently.

