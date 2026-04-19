# Linux Tutorial: Viewing and Manipulating File Contents with `cat`, `head`, and `tail`

This tutorial introduces basic Linux commands for viewing and manipulating file contents in the terminal. It's designed for new users. We'll cover `cat` for displaying or concatenating files, `head` for viewing the beginning of files, and `tail` for viewing the end. Each section includes command syntax, explanations, and simple examples. Assume you have a terminal open and some sample files (e.g., create `sample.txt` with text like "Line 1\nLine 2\n..." for testing).

## 1. Displaying and Creating Files with `cat`

The `cat` command concatenates and displays file contents. It's useful for viewing entire files or combining them.

### Display the contents of a file
```bash
cat filename
```
**Example:** `cat sample.txt` (displays all lines in `sample.txt`).

### Concatenate multiple files
```bash
cat file1 file2
```
**Example:** `cat file1.txt file2.txt` (shows contents of `file1.txt` followed by `file2.txt`).

### Create a new file
```bash
cat > filename
```
**Example:** `cat > newfile.txt`, then type text and press Ctrl+D to save (creates `newfile.txt` with your input).

### Append to an existing file
```bash
cat >> filename
```
**Example:** `cat >> existing.txt`, then type text and press Ctrl+D (adds text to the end of `existing.txt`).

## 2. Displaying the First Few Lines with `head`

The `head` command shows the beginning of a file. By default, it displays the first 10 lines.

### Display the first few lines of a file
```bash
head filename
```
**Example:** `head sample.txt` (shows first 10 lines).

### Display the first N lines of a file
```bash
head -n 10 filename
```
**Example:** `head -n 5 sample.txt` (shows first 5 lines).

### Display the first N bytes of a file
```bash
head -c 100 filename
```
**Example:** `head -c 50 sample.txt` (shows first 50 bytes).

### Display all lines except the last N
```bash
head -n -10 filename
```
**Example:** `head -n -5 sample.txt` (shows all but last 5 lines).

### Display the first N lines of multiple files
```bash
head -n 10 filename1 filename2
```
**Example:** `head -n 3 file1.txt file2.txt` (shows first 3 lines of each, with headers).

### Display without headers for multiple files
```bash
head -q filename1 filename2
```
**Example:** `head -q file1.txt file2.txt` (first 10 lines of each, no file names).

### Display with headers for multiple files
```bash
head -v filename1 filename2
```
**Example:** `head -v file1.txt file2.txt` (first 10 lines with file names).

### Display specific lines using pipes
```bash
head -n 10 filename | tail -n 5
```
**Example:** `head -n 10 sample.txt | tail -n 5` (shows lines 6-10).

## 3. Displaying the Last Few Lines with `tail`

The `tail` command shows the end of a file. By default, it displays the last 10 lines.

### Display the last few lines of a file
```bash
tail filename
```
**Example:** `tail sample.txt` (shows last 10 lines).

### Display the last N lines of a file
```bash
tail -n 10 filename
```
**Example:** `tail -n 5 sample.txt` (shows last 5 lines).

### Display the last N bytes of a file
```bash
tail -c 100 filename
```
**Example:** `tail -c 50 sample.txt` (shows last 50 bytes).

### Follow a file for new lines
```bash
tail -f filename
```
**Example:** `tail -f logfile.txt` (shows last 10 lines and updates as new lines are added; press Ctrl+C to stop).

### Display all lines starting from line N
```bash
tail -n +10 filename
```
**Example:** `tail -n +5 sample.txt` (shows from line 5 to end).

### Display the last N lines of multiple files
```bash
tail -n 10 filename1 filename2
```
**Example:** `tail -n 3 file1.txt file2.txt` (shows last 3 lines of each, with headers).

### Display without headers for multiple files
```bash
tail -q filename1 filename2
```
**Example:** `tail -q file1.txt file2.txt` (last 10 lines of each, no file names).

**Tips for New Users:** Practice in a safe directory. Use `man cat`, `man head`, or `man tail` for full documentation. Always check file permissions with `ls -l`.