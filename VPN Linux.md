# The definitive Linux VPN Client Guide for PXL University of Applied Sciences and Arts
This guide explains how to connect to the PXL University of Applied Sciences and Arts VPN server from a Linux host. Ideal to connect to internal systems like the VMware system if the host isn't connected to the PXL network.

## Prerequisites
The student/senior account needs to have VPN access enabled by the IT-Department.

**Students**: Ask your lecturer for VPN access.

**Seniors**: Contact the PXL network engineer if you don't have access.

## Installing the Software
It's necessary to install the BIG-IP Edge Command Line Client from F5 Networks Inc.

### A. Download
[Download](./linux_sslvpn.tar) the `tar`archive from this repository.


### B. Extract
```bash
$ tar -xf linux_sslvpn.tar
```

### C. Install
```bash
$ sudo ./Install.sh
```

## Usage

### A. Start a VPN session
Establish a connection:
#### For students:
```bash
$ f5fpc -s -t login.pxl.be -x -u YOUR_STUDENT_NUMBER@student.pxl.be
```
#### For staff members:
```bash
$ f5fpc -s -t login.pxl.be -x -u YOUR_STAFF_NUMBER@pxl.be
```

### B. Test the VPN session
```bash
$ f5fpc --info
Connection Status: session established
Favorites Information:
______________________
fav-Id   fav-Type  fav-Status       fav-Name
966      vpn        available       /Common/ssl_vpn_studenten
```

### C. Stop the VPN session
To stop the VPN connection, use the command below:

```bash
$ f5fpc --stop
```
