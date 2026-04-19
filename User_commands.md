# Linux Terminal Commands Tutorial for New Users

This tutorial covers essential Linux commands for monitoring system resources, managing processes, and handling file permissions. Each section includes commands with explanations and examples where applicable. Open your terminal and try them out!

## Locate a command
```bash
whereis name # Locate the binary, source, and manual page files for a command
```
```bash
whereis -b name # Locate the binary files for a command
```
```bash
whereis -m name # Locate the manual page files for a command
```
```bash
whereis -s name # Locate the source files for a command
```
## Display manual for a command
```bash
man name # Display the manual for a command
```
```bash
man -k keyword # Search for a keyword in the manual pages
```
```bash
man -f name # Display a short description of a command
```
```bash
man -a name # Display all manual pages for a command
```
## Display Disk Usage

Use these commands to check how much disk space is used and available on your system.

```bash
df -h  # Display disk usage in human-readable format (e.g., GB, MB)
```

**Example output:**
```
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   20G   28G  42% /
```

```bash
df -i  # Display inode usage (shows inodes, which track files)
```

**Example output:**
```
Filesystem     Inodes IUsed IFree IUse% Mounted on
/dev/sda1      100000  5000 95000   5% /
```

```bash
df -T  # Display filesystem type along with disk usage
```

**Example output:**
```
Filesystem     Type 1K-blocks  Used Available Use% Mounted on
/dev/sda1      ext4   52428800 20971520 29360128 42% /
```

```bash
df -hT  # Combine human-readable format with filesystem type
```

**Example output:**
```
Filesystem     Type  Size  Used Avail Use% Mounted on
/dev/sda1      ext4   50G   20G   28G  42% /
```

## Display Memory Usage

These commands show RAM and swap usage.

```bash
free -h  # Display memory usage in human-readable format
```

**Example output:**
```
              total        used        free      shared  buff/cache   available
Mem:           8.0G        2.0G        4.0G        100M        2.0G        5.5G
Swap:          2.0G          0B        2.0G
```

```bash
free -m  # Display memory usage in megabytes
```

**Example output:**
```
              total        used        free      shared  buff/cache   available
Mem:          8192        2048        4096         100        2048        5632
Swap:         2048           0        2048
```

```bash
free -g  # Display memory usage in gigabytes
```

**Example output:**
```
              total        used        free      shared  buff/cache   available
Mem:             8           2           4           0           2           5
Swap:            2           0           2
```

```bash
free -t  # Display total memory usage including swap
```

**Example output:** (Similar to above, but with totals summed)

## Display Running Processes

Monitor active processes on your system.

```bash
ps aux  # List all running processes with details
```

**Example output:**
```
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.1  12345  1234 ?        Ss   10:00   0:01 /sbin/init
user      1234  0.5  0.2  56789  2345 pts/0    S    10:05   0:02 bash
```

```bash
top  # Interactive real-time view of processes and system info (press 'q' to quit)
```

**Example output:** (Dynamic display; shows CPU, memory, and process list updating live)

## Kill a Process by PID

Stop a running process using its Process ID (PID, found via `ps` or `top`).

```bash
kill PID  # Gracefully terminate a process (replace PID with actual number, e.g., 1234)
```

**Example:** If a process with PID 1234 is running, `kill 1234` sends a signal to stop it.

```bash
kill -9 PID  # Force kill a process if it doesn't respond (use cautiously)
```

**Example:** `kill -9 1234` immediately terminates the process, even if it's unresponsive.

## Change File Permissions

Modify who can read, write, or execute a file.

```bash
chmod 755 filename  # Set permissions: owner full access, group and others read/execute
```

**Example:** `chmod 755 script.sh` makes the script executable for all, writable only by owner.

```bash
chmod +x filename  # Add execute permission for the owner
```

**Example:** `chmod +x myprogram` allows you to run `./myprogram` if it's executable.

**Tip:** Use `ls -l filename` to check current permissions before changing them.

Experiment safely in a test environment. For more details, use `man command` (e.g., `man df`).