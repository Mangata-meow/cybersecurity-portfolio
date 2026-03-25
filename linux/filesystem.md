# <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="25"/> Linux File System Hierarchy
Linux is structured in a tree-like hierarchy and is defined by the Filesystem Hierarchy Standard (FHS).
All of the files and directories originate from a single root directory: `/`.

--- 
## Overview of the structure
```
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── root
├── sbin
├── tmp
├── usr
└── var
```

---

## Most important directories

### `/` - top-level directory that contains all of the other directories.

### `/bin` - contains essential command binaries that are used for basic system operation.
**Examples:**
- `ls` - lists files in the directory
- `cp` - copies files and directories
- `cat` - displays the content of a file

### `/boot` - contains files that are required to boot the system (bootloader, kernel and required files).

### `/dev` - contains device files that represent hardware components.
**Example:** 
- `/dev/sda` -> hard disk

### `/etc/ - contains local system configuration files.
**Example:** 
- `/etc/passwd` -> user account information
- `/etc/hosts` -> local network configuration (DNS)

### `/home` - contains subdirectories storing data from each user on the system.
**Example:**
```bash
/home/julia
```

### `/lib` - contains shared libraries that are required for the system boot and program execution.

### `/media` - it is a mount for removable media devices such as USB drives.

### `/mnt` - it is a temporary mount point for regular filesystems.

### `/opt` - contains optional files, such as third-party tools.

### `/root` - it is a home directory for the root (administrator) user.

### `/sbin` - contains system binaries that are used for administration.
**Example:** 
- `iptables` -> controls the network traffic (incoming and outgoing)
- `reboot` -> restarts the system

### `/tmp` - contains the temporary files from the operating system and other programs. Files in this directory are usually cleared upon system boot, but may also be deleted at other times without warning.

**Example:**
```bash
# check temporary files
ls /tmp
```

### `/usr` - contains user binaries, libraries and documentation (man pages).

### `/var` - contains variable data files such as:
- logs,
- emails,
- web application data.

**Example:**
```bash
# Navigating to logs
cd /var/log
```

--- 
## Security perspective 
Understanding the file system hierarchy is critical in cybersecurity:
- `/etc/passwd` → contains user account data  
- `/var/log` → used for log analysis and incident response  
- `/dev` → can expose hardware access if misconfigured  
- `/root` → highly sensitive directory   
