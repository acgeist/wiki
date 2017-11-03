[Wiki Homepage](index.md)
# Linux 
### Permissions  

See the current permissions in a given directory by executing `ls -l`. This will yield something that looks like the following:
```
total 40
-rw-r--r-- 1 fore fore 1171 Oct 28 07:13 allmark.md
-rw-r--r-- 1 fore fore  329 Oct 28 09:36 apache.md
-rw-r--r-- 1 fore fore  101 Oct 28 07:14 bash.md
-rw-r--r-- 1 fore fore  109 Oct 28 07:14 c.md
-rw-r--r-- 1 fore fore  103 Oct 28 07:14 github.md
-rw-r--r-- 1 fore fore  493 Oct 28 09:53 index.md
-rwxrw-r-- 1 fore fore  321 Oct 28 09:50 linux.md
-rw-r--r-- 1 fore fore 3969 Oct 28 07:14 markdown.md
-rw-rw-r-- 1 fore fore   31 Oct 28 09:41 set_permissions.sh
-rw-rw-r-- 1 fore fore  202 Oct 28 09:55 vim.md
```
In order of output, these fields detail:
* file permissions
* number of links
* owner name
* owner group
* file size
* time of last modification
* file/directory name.

There are three permission groups: owner, group, and all users.  Each group has three permission types: read, write, ane execute.  Therefore for the file "linux.md" above, the owner (fore) can read, write, and execute the file.  The group (fore) can also read and write the file.  All users can read the file.

The `chmod` command is used to edit permissions for a given (set of) file(s) or directory.  The syntax abbreviates the owner as `u`, the group as `g`, and all users as `a`.  This is followed by a `+` or `-` which tells the system whether permissions are being granted or denied.  Finally, read, write, and execute are denoted by `r`, `w`, and `x` respectively.  
Take for example a file that currently has permissions `\_rw\_rw\_rw` (i.e. the owner, group, and all users have read and write permission).  To remove the read and write permissions from the all users group, we would execute: `chmod a-rw filename`.  To restore the permissions, we would execute: `chmod a+rw filename`.  
Alternatively, we can use binary references to set file permissions.  This is done by entering three integers, representing the owner, group, and all users.  Each number represents the sum of the permissions being granted, where read is equal to 4, write is equal to 2, and execute is equal to 1.  Therefore to set a file to have permissions `-rwxr-----`, we would execute `chmod 740 filename`.

The user can be change with the `chown` command: `chown owner filename`.  
The group is changed using: `chown owner:group filename`.

\*To make my ad-hoc markdown wiki work with apache, I set the top-level directory to `drwxr-xr-x` (`sudo chmod 755 /var/www/html/wiki`).  Within the folder, I set all the markdown files to -rw-r--r-- (`sudo chmod 644 /var/ww/html/wiki/*.md`).  
I also made a 1-line bash script to update this automatically as new files are added:  
```bash
#!/bin/sh
sudo chmod 644 *.md
```

#### Quick Reference:
u - Owner  
g - Group  
a - All Users  

r - read  
w - write  
x - execute  

r = 4  
w = 2  
x = 1

---
##### References  
[Understanding Linux File Permissions](https://www.linux.com/learn/understanding-linux-file-permissions)  
[What do the fields in ls -l mean?](https://unix.stackexchange.com/questions/103114/what-do-the-fields-in-ls-al-output-mean)

---
This page was last updated: Sat 28 Oct 2017 10:55:57 AM EDT 
