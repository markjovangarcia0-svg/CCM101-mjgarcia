# Cloud Infrastructure Components

## Compute

### Purpose

Compute resources execute instructions and provide the processing capability required by applications and services.

### Importance

A cloud workload needs sufficient CPU and memory to perform its tasks. Cloud computing makes it possible to allocate these resources according to application requirements.

### KillerCoda Example

The KillerCoda environment contains one CPU core and approximately 1.9 GiB of RAM. The processor is identified as an Intel Xeon E312xx (Sandy Bridge, IBRS update).

---

## Storage

### Purpose

Storage provides space for the operating system, application files, configuration files, and user data.

### Importance

Applications need storage to keep information available after processes finish. Cloud storage can also be expanded when an application requires additional capacity.

### KillerCoda Example

The main filesystem is /dev/vda1. It uses ext4 and has a capacity of 19 GB, with approximately 13 GB available during the investigation.

---

## Networking

### Purpose

Networking provides communication between users, servers, applications, and other infrastructure resources.

### Importance

Cloud resources depend on networks to exchange requests and data. Network configuration also determines how resources communicate with internal and external systems.

### KillerCoda Example

The primary interface is enp1s0 and its IPv4 address is 172.30.1.2/24. A docker0 interface is also present for Docker networking.

---

## Operating System

### Purpose

The operating system controls hardware resources and provides services and tools that applications use.

### Importance

A virtual machine requires an operating system to manage its CPU, memory, storage, networking, and running processes.

### KillerCoda Example

The environment runs Ubuntu 24.04.4 LTS with Linux kernel 6.8.0-138-generic.

---

## How the Components Work Together

The operating system manages the available compute, storage, and networking resources. Applications use CPU and memory for processing, storage for saving information, and networking for communicating with users or other services. Together, these components form the basic infrastructure needed to run a cloud workload.
