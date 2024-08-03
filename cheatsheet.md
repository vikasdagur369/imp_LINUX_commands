# Linux Commands Cheat Sheet

## Basic Commands

- `pwd` - Present working directory.
- `whoami` - Current user.
- `date` / `date +%T` - Date and time.
- `date +%H:%M` - Hours:minutes.
- `ls` - List files in the current directory.
- `ls -lt` - Additional details about files in the current directory.
- `ls -ltr` - Latest modified file shown at the bottom.
- `ls -lh` - Human-readable format details of files.
- `clear` - Clear terminal.

## File Operations

- `cat index.html` - Show content of file.
- `less test.csv` 
  - Opens file. 
  - ` /xyz` - Find "xyz" in file.
  - `shift + G` - Go to the end of the file.
  - `?xyz` - Reverse search, bottom to top.
  - `q` - Exit.
- `more test.csv` - View file page by page.
- `touch new.html` - Create a new file.
- `rm new.html` - Delete file.
- `vi new.html` 
  - Create and edit a new file.
  - `i` - Enter edit mode.
  - `:wq` - Save and exit.
- `nano file_name` - Edit file with nano editor.
- `mkdir folder_name` - Create folder.
- `rmdir folder_name` or `rm -rf folder_name` - Delete folder.
- `cd ..` - Go back to the previous directory.

## Directory Operations

- `/` - Root directory, all folders are under this.
- `cp index.html /dest/path` - Copy file to another folder.
- `cp index.html .` - Copy file in the current directory.
- `cp index.html index1.html` - Copy and rename file.
- `mv index.html folder_name/` - Move file to another folder.
- `mv file1 file2` - Rename file.

## Viewing Files

- `head -5 index.html` - Show first 5 lines of file.
- `tail -5 index.html` - Show last 5 lines of file.
- `sort file_name` or `sort -r file_name` - Sort file alphabetically.
- `sort file_name | uniq` - Remove duplicates from file.
- `split -l 3 file_name` - Split file into three different files.
- `grep "word" file_name` - Search for a word in file.
- `grep "word1 | word2" file_name` - Search for multiple words in file.

## Wildcards

- `ls a*` - List files starting with "a".
- `touch file{1..10}` - Create files file1, file2, ..., file10.

## File Information

- `wc -l file_name` - Number of lines in file.
- `cmp file1 file2` - Compare files.
- `diff -u file1 file2` - Show differences between files.
- `find /path/ -name file_name` - Find a file.
- `locate file_name` - Locate a file (run `updatedb` first).

## History and Utilities

- `history` - Show command history.
- `bc` - Open calculator.
- `cal 20xx` - Show calendar for a year.
- `uptime` - Show server uptime.
- `script` - Save terminal session to file (use `CTRL + D` to exit).
- `alias l="long_command"` - Create a shortcut for a command.

## Compression and Archiving

- `gzip -k file_name` - Compress file and keep original.
- `gzip -d file_name` or `gunzip file_name` - Uncompress file.
- `tar -czf compressed_folder_name folder_to_compress` - Compress folder.
- `tar -xzf compressed_folder_name` - Uncompress folder.
- `zip newfiles.zip file1 file2` - Compress files into zip.
- `unzip newfiles.zip` - Uncompress zip file.

## Downloading Files

- `wget url-of-file` - Download file from URL.
- `wget -O file_name URL_of_file` - Download and save as file_name.

## Calling APIs

- `curl URL_of_Api` - Call API.

## Application Installation

- `sudo yum or apt install app_name` - Install application.
- `rpm -qa | grep app_name` - Check if app is installed.
- `dnf list installed` - List all installed applications.
- `apt search app_name` - Check if app is available for installation.
- `systemctl start/stop/status service_name` - Manage services.
- `systemctl list-units --type=service --all` - List all services with status.
- `printenv` - List all environment variables.
- `export JAVA_HOME="/usr/lib/jvm/java_v"`
- `export PATH=$JAVA_HOME/bin:$PATH` - Temporary environment variable.
- `vi .bashrc` -> `export var_name` -> `source .bashrc` - Permanent environment variable.

## Text Processing

- `awk -F, '{print $col_no., $col_no}' file_name` - Print specific columns.
- `cut -c1-2 file.txt` - Print first 2 characters of each line.
- `sed -n '5p' file.txt` - Print 5th line of file.
- `sed -n 's/from/to/g' file.txt` - Replace all instances in file.
- `tr [:lower:] [:upper:] < test.txt` - Convert text to uppercase.
- `truncate -s 50M file_name` - Set file size to 50MB.

## User Management

- `su` - Switch to root user.
- `ifconfig` - Provides IP address of current machine.
- `ssh userName@IPaddress` - Access remote server.
- `scp file_name username@10.000.0:/home/folder` - Transfer file to another server.

## Permissions

- `ls -ltr` - Show file permissions.
- `chmod a+rwx file.txt` - Change file permissions.
- `chown user_name file_name` - Change file owner.

## System Information

- `free -h` - Show free RAM space.
- `top` - Check memory and CPU utilization.
- `du` - Show storage utilization of folder.
- `df` - Show filesystem info.
- `hostname` - Show hostname of Linux server.
- `lscpu` - Show CPU info.
- `arch` - Show architecture of Linux server.
- `lsblk` - List storage devices and partitions.
- `uname -a` or `cat /etc/os-release` - Show OS name.
- `ps -ef | grep java` - Check if process is running.
- `pgrep app_name` - Show process ID.
- `kill -9 1234` - Kill process by ID.
- `pkill process_name` - Kill process by name.
- `jobs` - Show active jobs.
- `ping www.xyz.com` - Check if server is accessible.
- `netsat -putan | grep 80` - Check if port is open.
- `reboot` / `shutdown` - Reboot or shut down server.

## User and Group Management

- `useradd new_user_name` - Add user.
- `passwd` - Change current user password.
- `groupadd group_name` - Create group.
- `userdel user_name` or `groupdel group` - Delete user or group.
- `usermod -G group_name user_name` - Add user to group.
