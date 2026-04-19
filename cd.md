# Linux Tutorial: The `cd` Command

The `cd` (change directory) command is used to navigate between directories in the Linux terminal. It's essential for moving around the file system. Below, we'll cover common uses with examples. Assume you're starting in `/home/user/Documents` for these examples.

## 1. Change to a Specific Directory
Use `cd` followed by the absolute or relative path to the directory.

```bash
cd /path/to/directory
```

**Example:**  
If you want to go to `/home/user/Pictures`:  
```bash
cd /home/user/Pictures
```
Before: `/home/user/Documents`  
After: `/home/user/Pictures` (check with `pwd`)

## 2. Change to Parent Directory
Use `cd ..` to move up one level in the directory tree.

```bash
cd ..  # Change to parent directory
```

**Example:**  
From `/home/user/Documents`:  
```bash
cd ..
```
Before: `/home/user/Documents`  
After: `/home/user` (check with `pwd`)

## 3. Change to Home Directory
Use `cd ~` to quickly return to your home directory.

```bash
cd ~  # Change to home directory
```

**Example:**  
From any location, like `/var/log`:  
```bash
cd ~
```
Before: `/var/log`  
After: `/home/user` (assuming your home is `/home/user`)

## 4. Change to Previous Directory
Use `cd -` to switch back to the directory you were in before the last `cd` command.

```bash
cd -  # Change to previous directory
```

**Example:**  
If you were in `/home/user/Documents`, then did `cd /tmp`, then:  
```bash
cd -
```
Before: `/tmp`  
After: `/home/user/Documents`

## 5. Change to Root Directory
Use `cd /` to go to the root of the file system.

```bash
cd /  # Change to root directory
```

**Example:**  
From `/home/user/Documents`:  
```bash
cd /
```
Before: `/home/user/Documents`  
After: `/`

**Tip:** Always use `pwd` (print working directory) to confirm your current location. Practice these in a safe environment, like a virtual machine, to avoid confusion.