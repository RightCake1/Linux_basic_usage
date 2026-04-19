## Package Management with apt (Debian/Ubuntu)

`apt` is the package manager for Debian-based systems like Ubuntu. It simplifies installing, updating, and upgrading software from repositories. This tutorial covers basic commands for new Linux users. Always run commands with `sudo` for administrative privileges.

### Update Package List
Refresh the list of available packages from repositories to ensure you have the latest information.

```bash
sudo apt update
```

**Example:** Before installing new software, update your package list.  
```bash
sudo apt update
```
Run this regularly to keep your package information current.

### Upgrade Installed Packages
Upgrade all installed packages to their latest versions for security and improvements.

```bash
sudo apt upgrade
```

**Example:** Upgrade your system packages.  
```bash
sudo apt upgrade
```
You may be prompted to confirm; type 'y' and press Enter to proceed. This keeps your system secure.

### Install a Package
Install a specific package by its name.

```bash
sudo apt install package_name
```

**Example:** Install the text editor Vim.  
```bash
sudo apt install vim
```
Replace `package_name` with the actual name, such as `firefox` for the web browser. Use `apt search keyword` to find packages if unsure.

**Tip:** Remember to run `sudo apt update` before installing or upgrading. For more details, use `man apt` in the terminal.

## Find files and directories with root privileges
```bash
sudo find /path/to/search -name "filename" # Find files by name
```
```bash
sudo find /path/to/search -type d -name "directory_name" # Find directories by name
```
```bash
sudo find /path/to/search -type f -name "filename" # Find files by name
```
```bash
sudo find /path/to/search -exec rm {} \; # Find and delete files
```