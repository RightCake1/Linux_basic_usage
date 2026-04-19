# Linux File and Directory Listing Tutorial

A beginner-friendly guide to the `ls` command with practical examples.

## Basic Commands

### `ls`
Lists all files and directories in the current directory.
```bash
ls
```
**Example output:**
```
Documents  Downloads  file.txt  folder/
```

### `ls -l`
Displays detailed information including permissions, owner, size, and modification date.
```bash
ls -l
```
**Example output:**
```
drwxr-xr-x  user  group  4096  Jan 15 10:30  Documents
-rw-r--r--  user  group  2048  Jan 14 09:15  file.txt
```

### `ls -a`
Lists all files and directories, including hidden ones (starting with `.`).
```bash
ls -a
```

### `ls -lh`
Combines detailed listing with file sizes in KB, MB, GB format.
```bash
ls -lh
```

### `ls -R`
Lists files and directories recursively in all subdirectories.
```bash
ls -R
```

### `ls -t`
Lists files sorted by last modified time (newest first).
```bash
ls -t
```

### `ls -S`
Lists files sorted by size (largest first).
```bash
ls -S
```

### `ls -r`
Reverses the sort order (oldest first, smallest first, etc.).
```bash
ls -r
```

### `ls -i`
Displays inode numbers for each file and directory.
```bash
ls -i
```

### `ls -d */`
Lists only directories, excluding files.
```bash
ls -d */
```

### `ls -F`
Appends type indicators: `/` for directories, `*` for executables, `@` for links.
```bash
ls -F
```

### `ls -1`
Lists one file or directory per line.
```bash
ls -1
```

## Combining Options
You can combine multiple options:
```bash
ls -lhS      # Long format, human-readable sizes, sorted by size
ls -ltr      # Long format, sorted by time, in reverse order
```