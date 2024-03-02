# OS Commands 

## Keyboard commands
- Ctrl + r - history
- Ctrl + c - stop the current command
- Ctrl + l - clears the screen
- !! - run previous command 

## Basic commands
- Echo - returns the input, ' ' for multi space text
- clear - clears the terminal
- reset - clears the terminal, resets all the settings
- --help, -h - print help
- man \<topic> - prints the manual 
- apropos \<string> - searches for short descriptions
- whatis \<string> - returns all the sections, where the *man* is found
- 

## User commands
- newgrp \<group> - change the active group in the current session
- id -u - returnds the UID
- whoami - the name of the user
- who - all logged users
- su \<user> - login shell from the user
- sudo -u \<user> \<command> - exectutes a command from user perspective

## Directory and file commands
- pwd - prints the current directory
- cd \<path> - moves the current directory
- ls - prints all objects in the current path
- ls -s - prints all hidden files
- ls -l - shows more information
- realpath \<path> - converts random path in absolute
- basename \<path> - returns the base name of the file
- dirname \<path> - retunrds the directory of the file
- ~ - home directory
- . - same directory 
- .. - previous directory
- touch \<path> - creates empty file
- mkdir \<path> - creates empty directory
- mkdir -p - creates all the directories needed for the given
- cp \<from> \<to> - copy a file 
- cp -r - copy the directory
- mv \<from> \<to> - renames/moves the file
- rm \<path> - deletes file
- rmdir - deletes empty directory
- rm -r \<path> - delete directory recursively 
- rm -rf \<path>- force delete

## Date and time commands
- date - prints the current day of week, day, mont, hh:mm:ss, time zone, year
- date +'\<format>' - formated date (" %Y-%m-%d%H:%M:%S")
- date -d - changes the format
- date +'%s' - seconds from 1970...
- date +'%s.%N' - seconds and nanoseconds
- date -d '@12313213' - date after ... seconds

## Inodes
- ls -l -i - inode

## Attributes, files
- mtime - last modification
- atime - last access
- ctime - last attribute change
- stat \<file> == ls -l - shows information about the attributes
- stat -c or --format - isolate specific attribute
- stat -c '%s' \<file> - size
- stat -c '%U' - name of the user owner
- stat -c '%Y' - last modification

## Ownership and rights
- chown \<user>:\<group> \<file> - changes the user:group
- chown \<user> \<file>
- chown \<group> \<file>
- chgrp - changes the group
- chmod u=rwx,g=rx,o= - gives specific rights
- chmod a=rwx - for all types
- chmod g+x - adds rights
- chmod u-w - removes rights
- chmod 755 - specifict rights
- chmod -r - recursively 
- umask - rights to remove 

## Hardlinks and symlinks
- ln \<new_path> \<current_path> - creates hardlink
- ls -l, stat, find - how much links a file has
- Hardlinks - Multiple files for the same data
- ln -s \<new_path> \<current_path> - creates a symlink
- Symlinks - can point to directory, can be linked, can points to unexistend file (broken symlink)
- realpath \<path> - derefers all symlinks
- basename \<path> - works like a string, doesn't care about symlinks
- dirname - -%-
- readlink \<path> - derefers the current link
- stat - doesn't work with links
- stat -L - works

## Storage
- df \<path> - prints statistics about teh storage of the file system
- -h == --human-readalbe 
- -H == --si
- -i == --inodes
- -T == --print-type
- du \<path> - recursively prints the taken storage 
- -h == --human-readalbe
- --si
- -s == --summarize
- -a

## More about files
- cat - print the content of a file
- less - shows content of file scrollable
- more - shows content of file scrollable only forward
- grep - search in file
- sort - sorts data
- head - first few lines
- head -n - number of lines
- tail - last few lines
- fzf - fuzzy finder

## Fun combinations
- compgen -c | fzf | xargs man - gives searchable manual for all the commands




