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