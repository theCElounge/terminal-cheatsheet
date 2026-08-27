# Terminal & Command Prompt Cheat Sheet

A quick reference guide for essential daily-use commands on macOS, Linux, and Windows.

---

## 📱 macOS & Linux (Terminal)

### Navigation Commands

#### `pwd`
**Print Working Directory** - Displays the full path of the current folder you're in, helping you know exactly where you are in the file system.

#### `cd <path>`
**Change Directory** - Navigates to a different folder, allowing you to move around the file system. Examples: `cd Documents`, `cd /Users/name/Projects`, `cd ~/Desktop`

#### `cd ..`
**Go Up One Level** - Moves you to the parent directory (one folder up) from your current location, useful for backtracking through nested folders.

#### `cd ~`
**Go to Home Directory** - Instantly navigates to your home folder, regardless of where you currently are in the file system.

#### `cd -`
**Go to Previous Directory** - Toggles back to the last directory you were in, helpful for switching between two frequently used locations.

### Listing & Viewing Files

#### `ls`
**List Files and Folders** - Shows all files and folders in the current directory, giving you a quick overview of what's there.
- `-l` : Long format with detailed info (permissions, size, date)
- `-a` : Show hidden files (those starting with a dot)
- `-lh` : Long format with human-readable file sizes
- `-la` : Combination of both detailed and hidden files

#### `cat <filename>`
**Display File Contents** - Prints the entire contents of a text file directly in the terminal, useful for quickly viewing small files.

#### `open <filename>`
**Open File** - Opens a file using its default application (e.g., PDFs open in Preview, images in Photos).

#### `open .`
**Open Folder in Finder** - Opens the current directory in the Finder/file manager window for visual browsing.

### Creating Files & Directories

#### `mkdir <name>`
**Make Directory** - Creates a new empty folder in the current location.
- `-p` : Create parent directories automatically if they don't exist (e.g., `mkdir -p a/b/c`)

#### `touch <filename>`
**Create Empty File** - Creates a new empty file with the specified name, or updates the timestamp if the file already exists.

### Copying, Moving & Deleting

#### `cp <source> <destination>`
**Copy File** - Creates a duplicate of a file in a new location, leaving the original intact.
- `-r` : Copy entire folders recursively (including all contents)

#### `mv <source> <destination>`
**Move or Rename** - Moves a file/folder to a new location or renames it by moving it to the same location with a new name.

#### `rm <filename>`
**Remove File** - Permanently deletes a file from the system (no trash bin, be careful!).
- `-r` : Delete folders and all their contents recursively
- `-f` : Force delete without confirmation

#### `rmdir <folder>`
**Remove Directory** - Deletes an empty folder; fails if the folder contains any files.

### Text Editing

#### `nano <filename>`
**Open Text Editor** - Opens a simple terminal-based text editor for creating or editing files. Press `Ctrl+X` to exit (it will prompt to save).

### Searching & Finding

#### `grep <search> <filename>`
**Search for Text** - Searches for lines containing a specific text pattern in a file and displays matching lines.
- `-i` : Ignore case sensitivity when searching
- `-n` : Show line numbers along with matches
- `-r` : Search recursively through all subdirectories

#### `find <path> -name <filename>`
**Find Files by Name** - Searches for files matching a specific name pattern throughout a directory and its subdirectories.

### System Information

#### `whoami`
**Show Current User** - Displays the username of the currently logged-in user.

#### `df -h`
**Disk Space Usage** - Shows how much disk space is available and used on all mounted drives in human-readable format (GB, MB, etc.).

#### `du -sh <folder>`
**Folder Size** - Calculates and displays the total size of a folder and all its contents in human-readable format.

#### `ps aux`
**List Processes** - Displays all currently running processes on the system with details like process ID, CPU usage, and memory.

#### `man <command>`
**Manual Page** - Displays the complete documentation and all available options for any command.

### Permissions & Admin

#### `sudo <command>`
**Super User Do** - Executes a command with administrator/root privileges, required for system-level operations. Often prompts for password.

#### `chmod 755 <file>`
**Change File Permissions** - Modifies who can read, write, and execute a file (755 = owner has all rights, others can read/execute).

### Piping & Redirection

#### `|` (Pipe)
**Pipe Output** - Sends the output from one command as input to another command, allowing you to chain operations together. Example: `ls -la | grep .txt`

---

## 🪟 Windows - Command Prompt (CMD)

### Navigation Commands

#### `cd <path>`
**Change Directory** - Navigates to a different folder in the file system. Examples: `cd Documents`, `cd C:\Users\Name\Projects`

#### `cd ..`
**Go Up One Level** - Moves to the parent directory above your current location.

#### `cd \`
**Go to Root** - Navigates to the root of the current drive (e.g., `C:\`)

#### `cd /d C:\path`
**Change Drive and Directory** - Allows you to change to a different drive and navigate in one command (e.g., switch from C: to D:).

### Listing & Viewing Files

#### `dir`
**List Directory** - Shows all files and folders in the current directory with basic information.
- `/a` : Show hidden and system files
- `/s` : Show files in current folder and all subfolders recursively

#### `type <filename>`
**Display File Contents** - Prints the contents of a text file to the screen for quick viewing.

#### `cls`
**Clear Screen** - Clears all text from the command prompt window, giving you a fresh start.

### Creating Files & Directories

#### `mkdir <name>`
**Make Directory** - Creates a new folder in the current location.

#### `echo <text> > <filename>`
**Create File with Content** - Creates a new text file and adds the specified text to it (use `>>` to append to existing file).

### Copying, Moving & Deleting

#### `copy <source> <destination>`
**Copy File** - Creates a duplicate of a file in the specified location.
- `/y` : Automatically overwrite destination file without prompting

#### `xcopy <source> <destination>`
**Copy with Subfolders** - Copies folders and all their contents recursively to a new location.
- `/s` : Copy folders and subfolders
- `/i` : Assume destination is a folder

#### `move <source> <destination>`
**Move or Rename** - Moves a file/folder to a new location or renames it.

#### `del <filename>`
**Delete File** - Permanently removes a file from the system.
- `/s` : Delete files from this folder and all subfolders
- `/q` : Quiet mode (don't ask for confirmation)

#### `rmdir <folder>`
**Remove Directory** - Deletes a folder from the system.
- `/s` : Delete folder and all its contents
- `/q` : Quiet mode (don't prompt for confirmation)

### Searching

#### `findstr <search> <filename>`
**Find String** - Searches for lines containing specific text in a file and displays the matching lines.

### System Information

#### `tasklist`
**List Running Processes** - Shows all currently running programs and their process IDs (PIDs).

#### `taskkill /IM <process>`
**Close a Process** - Terminates a running process by name (e.g., `taskkill /IM notepad.exe`).

#### `systeminfo`
**System Information** - Displays detailed information about your computer (OS, hardware, network, etc.).

#### `ipconfig`
**IP Configuration** - Shows your network configuration including IP address, gateway, and DNS servers.

#### `ping <address>`
**Test Connection** - Sends a test signal to another computer or website to check if it's reachable and responsive.

#### `help <command>`
**Help Information** - Shows available options and syntax for any command.

### Redirection

#### `>` (Redirect)
**Redirect to File** - Sends the output of a command to a file instead of displaying it on screen. Example: `dir > filelist.txt`

#### `>>` (Append)
**Append to File** - Adds the output of a command to the end of an existing file without overwriting it.

---

## ⚡ Windows - PowerShell (Modern Alternative)

PowerShell is more powerful than CMD and becoming the standard. It uses verb-noun command names, but has aliases that match Unix commands.

### Navigation Commands

#### `Set-Location <path>` or `cd` (alias)
**Change Directory** - Navigates to a different folder; `cd` is an alias for easier typing.

#### `Get-Location` or `pwd` (alias)
**Current Location** - Displays the full path of the directory you're currently in.

### Listing & Viewing Files

#### `Get-ChildItem` (aliases: `ls`, `dir`)
**List Files and Folders** - Shows all files and folders in the current directory with details.
- `-Recurse` : Include all subfolders
- `-Hidden` : Show hidden files

#### `Get-Content <filename>` (aliases: `cat`, `type`)
**Display File Contents** - Shows the entire contents of a text file in the terminal.

### Creating Files & Directories

#### `New-Item -ItemType Directory -Name <name>` or `mkdir` (alias)
**Create Folder** - Creates a new directory with the specified name.

#### `New-Item -ItemType File -Name <filename>` or `touch` (alias)
**Create File** - Creates a new empty file.

### Copying, Moving & Deleting

#### `Copy-Item <source> <destination>` or `cp` (alias)
**Copy File/Folder** - Duplicates a file or folder to a new location.

#### `Move-Item <source> <destination>` or `mv` (alias)
**Move or Rename** - Relocates a file/folder or renames it.

#### `Remove-Item <path>` (aliases: `rm`, `del`)
**Delete File/Folder** - Removes files or folders from the system.
- `-Recurse` : Delete folders and all contents

### Searching

#### `Select-String <search> <filename>` (alias: `grep`)
**Search for Text** - Finds lines containing specific text in a file, similar to Unix grep.

### System Information

#### `Get-Process` (alias: `ps`)
**List Processes** - Shows all currently running processes with details like CPU and memory usage.

#### `Stop-Process -Name <process>`
**Stop a Process** - Terminates a running program by name or ID.

#### `Clear-Host` (alias: `clear`)
**Clear Screen** - Clears all text from the PowerShell window.

#### `Get-Command`
**List All Commands** - Shows all available PowerShell commands you can use.

#### `help <command>`
**Help Information** - Displays documentation and usage examples for any command.

---

## 💡 Pro Tips

- **Tab Autocomplete**: Press `Tab` in any terminal to autocomplete file and folder names
- **Command History**: Use arrow up/down keys to cycle through previously entered commands
- **Man Pages**: On macOS/Linux, type `man <command>` for complete documentation
- **PowerShell is Powerful**: Windows PowerShell offers more capabilities than CMD and supports many Unix-like commands
- **Be Careful with `rm` and `del`**: These permanently delete files without recovery options
- **Hidden Files**: On Unix systems, files starting with a dot (.) are hidden; use `-a` flag with `ls` to see them
- **Piping**: Chain commands with `|` to process output: `ls -la | grep txt`

---

**Last Updated**: August 2026
