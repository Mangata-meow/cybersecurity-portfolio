# Linux Commands
COMING SOON

---

## Shell & prompt customization
### Bash Prompt (PS1)
The Bash prompt is the line that appears before each command you type in the terminal.
It is controlled by a variable called `PS1` (Prompt String 1).
By modifying `PS1`, you can customize what information is displayed in your terminal, such as:
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
