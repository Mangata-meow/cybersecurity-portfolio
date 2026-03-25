# <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="25"/> Linux Philosophy
Linux philosophy centers on simplicity, flexibility, efficiency, and openness.

> *"Do one thing and do it well."*

--- 

## Core principles
### 1. Everything is a file
In Linux, all system resources are represented as files:
- regular files  
- hardware devices  
- network connections  

This allows them to be read and written using standard tools and commands.

**Example:**
```bash
cat /etc/passwd
```

### 2. Small, single-purpose programs
Instead of large, complicated programs, Linux provides many different tools that are designed to perform one specific task.

These tools can be combined to work together.

**Examples:**
- `grep` → searches text  
- `sort` → sorts data  
- `cat` → displays file content  

### 3. Combining programs to perform complex tasks
Linux allows chaining multiple programs together using pipes (`|`), which makes it possible to perform more complex operations.

**Example:**
```bash
cat /etc/passwd | grep root
```

### 4. Avoid captive user interfaces
Linux primarily works with the shell (terminal), which gives the user greater control over the operating system.
Although it can be harder to learn at the beginning, it provides more flexibility and precision.

### 5. Configuration data stored in text files
System configuration data is stored in plain text files.

This makes it easy to read, modify, and manage.

**Examples:**
- `/etc/hosts` → local network configuration  
- `/etc/passwd` → user account information  

---
## Security perspective
- System components are accessible as files,
- Lots of tools that can be extremely useful for analysis,
- Proper permissions are critical.
