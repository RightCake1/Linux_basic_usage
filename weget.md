# Linux Terminal Tutorial for New Users: Downloading Files and Package Management

This tutorial covers basic Linux commands for downloading files from the internet using `wget` and managing packages on Debian/Ubuntu systems using `apt`. These commands are run in the terminal. Always use `sudo` for administrative tasks, and be cautious with downloads from untrusted sources.

## Downloading Files with wget

`wget` is a command-line tool to download files from the web. It's useful for fetching resources directly to your system.

### Basic Download
Download a single file from a URL.

```bash
wget http://example.com/file
```

**Example:** Download a sample text file.  
```bash
wget http://example.com/sample.txt
```
This saves `sample.txt` in your current directory.

### Download with Custom Filename
Save the downloaded file with a different name using the `-O` option.

```bash
wget -O new_filename http://example.com/file
```

**Example:** Download and rename a file.  
```bash
wget -O myfile.zip http://example.com/archive.zip
```
This downloads `archive.zip` and saves it as `myfile.zip`.

### Resume a Partial Download
Resume downloading a file that was interrupted, using the `-c` option.

```bash
wget -c http://example.com/file
```

**Example:** Resume downloading a large file.  
```bash
wget -c http://example.com/large.iso
```
If the download stopped midway, this continues from where it left off.

### Download an Entire Directory
Recursively download a directory and its contents with the `-r` option.

```bash
wget -r http://example.com/directory
```

**Example:** Download a website's images folder.  
```bash
wget -r http://example.com/images/
```
This creates a local `example.com` directory with the mirrored content. Note: Use sparingly to avoid overloading servers.

