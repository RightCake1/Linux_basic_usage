
# The `rm` Command - Removing Files and Directories

The `rm` command is used to delete files and directories in Linux. **Warning:** Deleted files cannot be easily recovered, so use this command carefully.

## Basic Syntax

```bash
rm [options] filename
```

---

## Commands and Examples

### 1. Remove a Single File

```bash
rm filename
```

**Example:**
```bash
rm document.txt
```

Permanently deletes `document.txt` without confirmation.

---

### 2. Remove a File with Confirmation

```bash
rm -i filename
```

**Example:**
```bash
rm -i document.txt
```

Prompts: `remove regular file 'document.txt'?` before deletion. Type `y` to confirm or `n` to cancel.

---

### 3. Force Remove a File

```bash
rm -f filename
```

**Example:**
```bash
rm -f important.txt
```

Removes a file without prompting, even if it's read-only.

---

### 4. Remove a Directory and Contents

```bash
rm -r directory_name
```

**Example:**
```bash
rm -r old_project
```

Recursively deletes the `old_project` directory and all files inside it.

---

### 5. Force Remove a Directory and Contents

```bash
rm -rf directory_name
```

**Example:**
```bash
rm -rf old_project
```

Forcefully deletes a directory and all contents without prompting. **Use with caution!**

---

## Quick Tips

- Combine flags: `rm -ri` for interactive recursive removal
- Use wildcards carefully: `rm *.log` removes all `.log` files
- Consider `rm -i` when learning to add safety confirmation
