# The command prompt

When you open a terminal you are presented with a command prompt, waiting for you to input a command. It will look something like this:
```
username@computer-name:~$ |
``` 
It gives you information about:

- Your username

- The name of your computer

- The location in your filesystem (~ indicates your home directory)
A separator, usually $ symbol

- The prompt (often blinking) waiting for your command input

### [Using user commands](User_commands.md)
### [Using sudo](sudo.md)
### Navigating the filesystem

The location of files in Unix is represented as a file path. For example:
```
/home/participant/Documents
```
Indicates the “Documents” folder of a user called “participant”. The first / at the beginning of the path indicates the root (or start) of the filesystem.

Paths can be specific in two ways:

Absolute path: specify the full path starting from the root. These paths always start with ```/```.

Relative path: specify the path starting from your current location. For example, if you are located in ```/home/participant```, the path ```Documents/resources``` would be equivalent to ```/home/participant/Documents/``` resources. Relative paths never start with ```/```.

Here are some key commands to navigate the filesystem:


- `Up Arrow`: Will show your last command
- `Down Arrow`: Will show your next command
- `Tab`: Will auto-complete your command
- `Ctrl + L`: Will clear the screen
- `Ctrl + C`: Will cancel a command
- `Ctrl + R`: Will search for a command
- `Ctrl + D`: Will exit the terminal

Some of the commands to know for navigation: 

- ```pwd``` prints your current directory 
- ```cd``` changes directory
- ```ls``` lists files and folders
- ```*``` is known as a “wildcard” and can be used to match multiple files

Here are some key commands to create directories and investigate the content of text files:

- ```mkdir``` creates a directory
- ```head``` prints the top lines of a file
- ```tail``` prints the bottom lines of a file
- ```less``` opens the file in a viewer
- ```wc``` counts lines, words and characters in a file
- ```grep``` prints lines that match a specified text pattern

## Print working directory

```bash
pwd # Print the current working directory
```

## The wildcard * can be used to match files that share part of their name. For example:

```ls reference/*.fasta```

Only matches the files with .fasta extension.

 [Using ```ls```](ls.md)

 [Using ```cd```](cd.md)

 [Using ```rm```](rm.md)

 [Using ```rmdir```](rmdir.md)

 [Using ```cat```](cat.md)

 [Using ```grep```](grep.md)

 [Using ```touch```](touch.md)

 [Using weget](weget.md)

 [Using ```echo```](echo.md)

 [Using zip tools](zip.md)


## Clear the terminal screen
```bash
clear # Clear the terminal screen
```

## Kill a process by name
```bash
kill process_name # Kill a process by name
```
```bash
kill -9 process_name # Force kill a process by name
```