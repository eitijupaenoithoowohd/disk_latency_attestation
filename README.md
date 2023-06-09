# Latency Attestation

Disk Latency Attestation is a process of verifying and providing evidence of the performance and latency characteristics of a disk storage system. It involves running tests or measurements to assess the time taken for a storage device to complete read and write operations and comparing the results against predetermined thresholds.

The attestation process can help identify and diagnose performance issues such as slow read and write speeds, high latency, and excessive I/O wait times. It can also be used to validate compliance with service-level agreements (SLAs) that specify the expected performance of storage systems.

# Disk Latency Attestation Tool

A simple yet effective tool to track disk storage latency during write operations.

This utility operates as a daemon in the RAM, generates random data and writes it as a file to the specified disk storage for a certain intervals, measuring the time it took to write a file of the same size in every reiteration.

The data cannot being cached because for each new test of writing pseudo-random data is generated.

The application generates a log in the form of a CSV table, detailing the date, time of each event, duration of dataset writing, error codes and error messages.

# Build

Install build and compile tools on Linux
```
sudo apt -y install build-essential
```

Get source code
```
git clone https://github.com/eitijupaenoithoowohd/disk_latency_attestation.git
```

Build
```
cd disk_latency_attestation
make
```

# Run
```
./disk_latency_attestation /mnt /tmp/report.csv
```
