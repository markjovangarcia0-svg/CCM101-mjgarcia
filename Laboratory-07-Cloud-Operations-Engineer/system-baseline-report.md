
# System Baseline Report

## 1. Host Memory

The host server has a total RAM capacity of 1.9Gi. At the time of checking, 415Mi was used, 1.1Gi was free, and 1.5Gi was available. The server also has 1.0Gi of swap space, with 0B currently used.

## 2. Root Disk Capacity

The root filesystem (`/`) has a total storage capacity of 19G. It uses 5.5G of storage, with 13G available. The current disk usage is 30%.

## 3. CPU and Running Processes

I used the `top` command to observe active processes, CPU usage, and system load. This command helps identify processes that may consume too many resources and affect server performance.

## 4. Why Disk Monitoring Matters

Checking disk space before a major traffic surge is important because web servers need storage for application logs, temporary files, and other data. If the disk becomes full, applications and services may fail or become unreliable.
