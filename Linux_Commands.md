## Navigation
- `Up Arrow`: Will show your last command
- `Down Arrow`: Will show your next command
- `Tab`: Will auto-complete your command
- `Ctrl + L`: Will clear the screen
- `Ctrl + C`: Will cancel a command
- `Ctrl + R`: Will search for a command
- `Ctrl + D`: Will exit the terminal

## List files and directories
```bash
ls # List files and directories in current directory
```
```bash
ls -l # List files and directories in long format
```
```bash
ls -a # List all files and directories, including hidden ones
```
```bash
ls -lh # List files and directories in long format with human-readable file sizes
```
```bash
ls -R # List files and directories recursively
```
```bash
ls -t # List files and directories by last modified time
```
```bash
ls -S # List files and directories by file size
```
```bash
ls -r # List files and directories in reverse order
```
```bash
ls -i # List files and directories with inode numbers
```
```bash
ls -d */ # List directories only
```
```bash
ls -F # List files and directories with indicators
```
```bash
ls -1 # List files and directories in a single column
```

## Change directory
```bash
cd /path/to/directory
```
```bash
cd .. # Change to parent directory
```
```bash
cd ~ # Change to home directory
```
```bash
cd - # Change to previous directory
```
```bash
cd / # Change to root directory 
```

## Print working directory
```bash
pwd # Print the current working directory
```

## Remove a file
```bash
rm filename # Remove a file
```
```bash
rm -i filename # Prompt before removing a file
```
```bash
rm -f filename # Force removal of a file
```
```bash
rm -r directory_name # Remove a directory and its contents
```
```bash
rm -rf directory_name # Force removal of a directory and its contents
```

## Remove an empty directory
```bash
rmdir directory_name # Remove an empty directory
```
```bash
rmdir -r directory_name # Remove a directory and its contents
```
```bash
rmdir -p directory_name # Remove parent directories if they are empty
```

## Display the contents of a file
```bash
cat filename # Display the contents of a file
```
```bash
cat file1 file2 # Concatenate multiple files
```
```bash
cat > filename # Create a new file
```
```bash
cat >> filename # Append to an existing file, adds text to the end of the file
```

## Display the first few lines of a file
```bash
head filename # Display the first few lines of a file
```
```bash
head -n 10 filename # Display the first 10 lines of a file
```
```bash
head -c 100 filename # Display the first 100 bytes of a file
```
```bash
head -n -10 filename # Display all lines except the last 10
```
```bash
head -n 10 filename1 filename2 # Display the first 10 lines of multiple files
```
```bash
head -q filename1 filename2 # Display the first few lines of multiple files without headers
```
```bash
head -v filename1 filename2 # Display the first few lines of multiple files with headers
```
```bash
head -n 10 filename | tail -n 5 # Display lines 6-10 of a file
```

## Display the last few lines of a file
```bash
tail filename # Display the last few lines of a file
```
```bash
tail -n 10 filename # Display the last 10 lines of a file
```
```bash
tail -c 100 filename # Display the last 100 bytes of a file
```
```bash
tail -f filename # Display the last 10 lines of a file and continue to display new lines as they are added
```
```bash
tail -n +10 filename # Display all lines starting from line 10
```
```bash
tail -n 10 filename1 filename2 # Display the last 10 lines of multiple files
```
```bash
tail -q filename1 filename2 # Display the last few lines of multiple files without headers
```

## Search for a string in a file
```bash
grep "search_string" filename # Search for a string in a file
```
```bash
grep -i "search_string" filename # Perform a case-insensitive search
```
```bash
grep -r "search_string" directory # Search for a string in all files in a directory
```
```bash
grep -v "search_string" filename # Display lines that do not contain the search string
```
```bash
grep -c "search_string" filename # Display the number of lines that contain the search string
```
```bash
grep -n "search_string" filename # Display the line numbers of lines that contain the search string
```
```bash
grep -l "search_string" filename # Display the names of files that contain the search string
```
```bash
grep -E "A|T|C|G" filename # Search for any occurrence of A, T, C, or G
```
```bash
grep -E "ATCG" filename # Search for the exact sequence ATCG
```
```bash
grep -E "A{2,}|T{2,}|C{2,}|G{2,}" filename # Search for any occurrence of AA, TT, CC, or GG
```
```bash
grep -E "A{3,}|T{3,}|C{3,}|G{3,}" filename # Search for any occurrence of AAA, TTT, CCC, or GGG
```

## Display disk usage
```bash
df -h # Display disk usage in human-readable format
```
```bash
df -i # Display inode usage
```
```bash
df -T # Display filesystem type
```
```bash
df -hT # Display disk usage with filesystem type in human-readable format
```
```bash
du -Sh # Display the total disk usage of a folder
```
```bash
du -h # Display the disk usage of each file in the folder
```

## Display memory usage
```bash
free -h # Display memory usage in human-readable format
```
```bash
free -m # Display memory usage in megabytes
```
```bash
free -g # Display memory usage in gigabytes
```
```bash
free -t # Display total memory usage
```

## Display running processes
```bash
ps aux
```
```bash
top # Display real-time system information including running processes
```

## Kill a process by PID
```bash
kill PID
```
```bash
kill -9 PID # Force kill a process
```

## Change file permissions
```bash
chmod 755 filename
```
```bash
chmod +x filename # Add execute permission
```
```bash
chmod +rwx filename # Add read, write, and execute permission
```

## Download a file from the internet
```bash
wget http://example.com/file
```
```bash
wget -O new_filename http://example.com/file # Save the file with a different name
```
```bash
wget -c http://example.com/file # Resume a partially downloaded file
```
```bash
wget -r http://example.com/directory # Download an entire directory
```

## Update package list (Debian/Ubuntu)
```bash
sudo apt update
```

## Upgrade installed packages (Debian/Ubuntu)
```bash
sudo apt upgrade
```

## Install a package (Debian/Ubuntu)
```bash
sudo apt install package_name
```

## Create an empty file or update the timestamp of an existing file
```bash
touch filename # Create an empty file
```
```bash
touch file1 file2 # Create multiple files at once
```
```bash
touch file{1..10} # Create multiple files using brace expansion
```
```bash
touch -d "2020-01-01 12:00:00" filename # Update the timestamp of a file
```
```bash
touch -d tomorrow filename # Update the timestamp of a file to tomorrow
```

## Display a message
```bash
echo "Hello, World!" # Display a message
```
```bash
echo file > filename # Write text to a file
```
```bash
echo file >> filename # Append text to a file
```

## Edit a file using nano
```bash
nano filename # Open a file in the nano text editor
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

## Compress files and directories
```bash
zip archive_name.zip file1 file2 # Compress multiple files into a zip archive
```
```bash
zip -r archive_name.zip directory # Compress a directory and its contents into a zip archive
```
```bash
zip -u archive_name.zip file1 # Update a zip archive with new files
```
```bash
zip -d archive_name.zip file1 # Remove a file from a zip archive
```
```bash
tar -czvf archive_name.tar.gz directory # Compress a directory into a tar.gz archive
```
```bash
tar -xzvf archive_name.tar.gz # Extract a tar.gz archive
```

## Extract files from a zip archive
```bash
unzip archive_name.zip # Extract all files from a zip archive
```
```bash
unzip archive_name.zip -d destination_directory # Extract files to a specific directory
```
```bash
unzip -l archive_name.zip # List the contents of a zip archive
```
```bash
unzip -t archive_name.zip # Test the integrity of a zip archive
```

## Clear the terminal screen
```bash
clear # Clear the terminal screen
```

## View the contents of a file one screen at a time
```bash
less filename # View the contents of a file
```

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

## Open a file with the default application
```bash
xdg-open filename # Open a file with the default application (Linux)
```

## Kill a process by name
```bash
kill process_name # Kill a process by name
```
```bash
kill -9 process_name # Force kill a process by name
```
