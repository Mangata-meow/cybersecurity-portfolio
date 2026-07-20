# Linux Commands
- `ls` → lists the files and directories within the current folder (or any specified directory)
  - `ls -l` → displays more information about the directories and files
  - `ls -la` → displays all files of a directory, including the hidden ones
- `cd` → changes directories
  - `cd -` → jumps back to the directory we were last in
  - `cd ..` → jumps to the parent directory of the directory that we are currently in
- `pwd` → displays the current directory name
-  `man` → displays the full manual pages of the tools (commands) and provides detailed information about their usage
```
Mangatameow@htb[/htb]$ man <tool>
```
- `--help` or `-h` → this is a shorter version of the manual page, shows only the most common options
```
Mangatameow@htb[/htb]$ <tool> --help
```
- `apropos` → searches descriptions (in manuals) for instances of a given word (really useful if I forget a full command)
```
Mangatameow@htb[/htb]$ apropos <keyword>
```
-  `whoami` → displays the current username
- `id` → returns the user's identity (expanded whoami)
- `hostname` → sets or prints the name of the current host system
- `uname` → displays basic information about the operating system and system hardware
- `ifconfig` → assigns or displays an address to a network interface and/or configures network interface parameters
- `ip` → shows or manipulates routing, network devices, interfaces and tunnels
- `netstat` → shows network status
- `ss` → investigates sockets
- `ps` → shows process status
- `who` → shows who is logged in
- `env` → prints environment
- `lsblk` → lists block devices
- `lsusb` → lists USB devices
- `lsof` → lists open files
- `lspci` → lists PCI devices

  
### Useful website: https://explainshell.com → explains commands

---

## Shell & prompt customization
### Bash Prompt (PS1)
The Bash prompt is the line that appears before each command we type in the terminal.
It is controlled by a variable called `PS1` (Prompt String 1).
By modifying `PS1`, we can customize what information is displayed in our terminal, such as:
- username  
- hostname  
- current directory  
- time  

### Special Characters
These special characters can be used inside `PS1` to display dynamic system information:
- `\d` → current date (e.g. Tue Oct 26)  
- `\D{%Y-%m-%d}` → custom date format (YYYY-MM-DD)  
- `\H` → full hostname  
- `\j` → number of jobs managed by the shell  
- `\n` → starts a new line  
- `\r` → carriage return  
- `\s` → name of the shell  
- `\t` → current time (24-hour format HH:MM:SS)  
- `\T` → current time (12-hour format HH:MM:SS)  
- `\@` → current time (AM/PM format)  
- `\u` → current username  
- `\w` → full path of the current working directory  

---

### Example
This prompt shows the username, hostname, current directory, and time.
```bash
PS1="\u@\H:\w [\t]$ "
```

Example output:
```
julia@cyber:/home/julia/projects [14:32:10]$
```
