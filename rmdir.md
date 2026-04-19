## rmdir Command Tutorial

The `rmdir` command in Linux is used to remove empty directories. It will not remove directories that contain files or other directories. For removing directories with contents, use `rm -r` instead (not covered here, as this tutorial focuses on `rmdir`).

### Basic Usage: Remove an Empty Directory
```bash
rmdir directory_name
```
This command removes the specified empty directory. If the directory is not empty or does not exist, it will display an error.

**Example:**
```bash
mkdir mydir  # Create an empty directory
ls -d mydir  # Verify it exists
rmdir mydir  # Remove it
ls -d mydir  # Error: No such file or directory
```

### Remove Parent Directories if Empty
```bash
rmdir -p directory_name
```
This option removes the specified directory and its parent directories if they become empty after removal. It's useful for cleaning up nested empty directories.

**Example:**
```bash
mkdir -p parent/child/grandchild  # Create nested empty directories
ls -R parent  # Verify structure
rmdir -p parent/child/grandchild  # Remove grandchild, then child, then parent if empty
ls parent  # Error: No such file or directory
```

Note: `rmdir` does not have a `-r` option for recursive removal of non-empty directories. Use `rm -r` for that purpose.