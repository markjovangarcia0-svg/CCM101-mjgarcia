# Infrastructure Report

## 1. System Information

| Information | Result |
|---|---|
| Operating System | Ubuntu 24.04.4 LTS |
| Kernel Version | 6.8.0-138-generic |
| CPU Model | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| CPU Cores | 1 |
| Total RAM | 1.9 GiB |
| Hostname | ubuntu |

### Analysis

The investigated Linux environment uses Ubuntu 24.04.4 LTS and kernel version 6.8.0-138-generic. The virtual machine is configured with one CPU core and about 1.9 GiB of memory. The hostname identifies the machine as ubuntu.

## 2. Network Information

| Information | Result |
|---|---|
| Main Interface | enp1s0 |
| Status | UP |
| IPv4 Address | 172.30.1.2/24 |
| Loopback Address | 127.0.0.1/8 |
| Docker Interface | docker0 |
| Docker Address | 172.17.0.1/16 |

### Analysis

The primary network interface is enp1s0 and it is currently active. Its IPv4 address is 172.30.1.2/24. The system also contains a loopback interface and a Docker interface used for local container networking.

## 3. Storage Information

| Filesystem | Type | Size | Used | Available | Usage | Mount |
|---|---|---:|---:|---:|---:|---|
| /dev/vda1 | ext4 | 19G | 5.4G | 13G | 30% | / |
| /dev/vda16 | ext4 | 881M | 117M | 703M | 15% | /boot |
| /dev/vda15 | vfat | 105M | 6.2M | 99M | 6% | /boot/efi |

### Analysis

The main storage volume is /dev/vda1. It uses the ext4 filesystem and provides 19 GB of space. At the time of investigation, 5.4 GB was occupied and around 13 GB remained available. The system also contains separate boot and EFI partitions.

## 4. Overall Assessment

The KillerCoda environment represents a small virtualized Linux server. Its CPU and memory provide the processing resources, its virtual disk provides persistent filesystem storage, and its network interface allows communication with other systems. Ubuntu manages these resources and provides the environment used to perform cloud infrastructure tasks.
