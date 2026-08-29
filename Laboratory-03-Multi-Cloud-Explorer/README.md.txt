### Linux Server Investigation

### 1. Operating System

Result:

* Operating System: Ubuntu 24.04.4 LTS
* Version ID: 24.04
* Codename: Noble Numbat
* Architecture: x86_64
* Based on: Debian

### 2. CPU Information

Result:

* Architecture: x86_64
* CPU Model: Intel Xeon E312xx (Sandy Bridge, IBRS update)
* CPU Speed: 2.0 GHz
* CPU(s): 1
* Cores per Socket: 1
* Threads per Core: 1
* Sockets: 1
* Hypervisor: KVM
* Virtualization Type: Full

### 3. Memory Information

Result:

| Memory           |  Amount |
| ---------------- | ------: |
| Total Memory     | 2.2 GiB |
| Used Memory      | 1.3 GiB |
| Free Memory      | 513 MiB |
| Available Memory | 962 MiB |
| Swap             |     0 B |

### 4. Disk Space Information

Result:

The primary Linux filesystem is `/dev/vda1`, which has a total capacity of **19 GB**. Currently, **11 GB is used**, while approximately **7.5 GB is available**, resulting in **60% disk usage**. The server also has separate `/boot` and `/boot/efi` partitions.

| Filesystem                 |   Size |   Used | Available | Use |
| -------------------------- | -----: | -----: | --------: | --: |
| `/dev/vda1`                |  19 GB |  11 GB |    7.5 GB | 60% |
| `/dev/vda16` (`/boot`)     | 881 MB | 117 MB |    703 MB | 15% |
| `/dev/vda15` (`/boot/efi`) | 105 MB | 6.2 MB |     99 MB |  6% |


# Cloud Migration Options

If this Linux server were migrated to the cloud, it could be hosted on AWS, Microsoft Azure, or Google Cloud Platform using the following services.

### Amazon Web Services (AWS)

The Ubuntu Linux server could be hosted using **Amazon EC2**, which provides scalable virtual machine instances. **Amazon EBS** could provide persistent block storage for the server, while **Amazon VPC** could provide secure networking. The server could also use **AWS IAM** to manage users and access permissions.

Possible AWS Services:

* Amazon EC2
* Amazon EBS
* Amazon VPC
* AWS IAM

### Microsoft Azure

The server could be migrated to **Azure Virtual Machines**, which can run Ubuntu Linux in the cloud. **Azure Managed Disks** could be used for persistent storage, while **Azure Virtual Network** could manage network communication. **Microsoft Entra ID** could be used to manage identities and access.

Possible Azure Services:

* Azure Virtual Machines
* Azure Managed Disks
* Azure Virtual Network
* Microsoft Entra ID

### Google Cloud Platform (GCP)

The server could be hosted using **Compute Engine**, Google's virtual machine service. **Persistent Disk** could provide storage for the operating system and application data, while **Virtual Private Cloud (VPC)** could provide secure networking. **Cloud IAM** could manage access to the cloud resources.

Possible GCP Services:

* Compute Engine
* Persistent Disk
* Virtual Private Cloud (VPC)
* Cloud IAM
