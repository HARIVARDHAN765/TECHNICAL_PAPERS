# Command Line Interface (CLI) Operations

## Introduction
This technical paper provides an understanding of CLI and Git command operations in the terminal. These skills are widely used by software developers and other departments related to software development.

## 1. File and Directory Operations

### Create / Read / Update / Delete / Move

**Create files and directories**

 * mkdir d1
 * touch a.txt


**Read files**

 * cat a.txt
 * less a.txt

**Update files**

 * echo "Hello" >> a.txt
 * nano a.txt

**Delete files and directories**

 * rm a.txt
 * rm -r d1

**Move or rename**

 * mv a.txt d1/
 * mv a.txt b.txt

## 2. Disk Status

 * df -h 

## 3. Process Management

**List all processes**
 * ps aux


**Extract process IDs using pipes**

 * ps aux | grep safari | awk '{print $2}'


**Kill a process**

 * ps aux | grep firefox | awk '{print $2}' | xargs kill

## 4. Parent Process

 * ps -o ppid= -p <PID>

## 5. File Permissions

 * ls -l a.txt

### Permission Structure
- Owner (user)
- Group
- Others

### Numeric Values

 * Read (r)   - 4    
 * Write (w)  - 2    
 * Execute(x) - 1   

**Change permissions**

 * chmod 755 a.txt

**Change ownership**

 * chown user:group a.txt

## 6. Text Processing

**Extract last lines**

 * tail -n 30 file.txt

**Count occurrences of a word**

 * grep -o "word" file.txt | wc -l

**Search for a word**

 * grep "word" file.txt

## 7. Basics of sed and awk

**sed (stream editor)**

 * sed 's/old/new/g' file.txt

**awk (pattern scanning and processing)**

 * awk '{print $1}' file.txt

## 8. Paths

**Absolute Path**

 * /home/user/file.txt


**Relative Path**

 * ../file.txt

### Difference
- Absolute path: full path starting from root `/`
- Relative path: current working directory

## 9. find Command

 * find ~ -name "*java*"

Searches for files or directories containing "java" in their name.


## 10. ls Command Flags


 * ls -a     # show hidden files
 * ls -t     # sort by time
 * ls -r     # reverse order
 * ls -h     # human readable sizes
 * ls -arth  # combined flags

## 11. Terminal Control Codes

 * Ctrl + C - Terminate process 
 * Ctrl + Z - Suspend process 
 * Ctrl + D - Exit terminal 
 * Ctrl + R - Reverse search 

### Ctrl + C vs Ctrl + Z
- Ctrl + C: kills the process 
- Ctrl + Z: pauses the process 


## 12. Productivity Features

- Tab → auto-complete commands and file paths  
- Arrow keys → navigate command history  
- Ctrl + R → reverse search previously executed commands  

## 13. Sample Practice Commands

### Go into your home directory
 * cd ~

### Create a directory d1
 * mkdir d1

### Create a file a.txt inside it
 * touch d1/a.txt

### Check permissions of a.txt
 * ls -l d1/a.txt

### Three elements in permissions
 * owner
 * group
 * other

### Change permission to 755
 * chmod 755 d1/a.txt

### Create directory d2
 * mkdir d2

### Create b.txt inside d2
 * touch d2/b.txt

### Change permission of d2 and everything inside
 * chmod -R 755 d2

### Start Firefox
 * firefox 

### List all processes
 * ps aux

### Find PID of Firefox
 * ps aux | grep firefox|awk '{print $2}'

### Kill Firefox process
 * ps aux | grep firefox | awk '{print $2}' | xargs kill

### Your user in Linux
 * whoami

### Your group
 * groups

### Computer architecture
 * uname -a

### Find all "java" in filenames
 * find ~ -name "*java*"

### List all files
 * ls -arth ~

### Last 30 lines of file
 * tail -n 30 file.txt

### Word count of a word
 * grep -o "Harry" file.txt | wc -l

## 14. System Information

* whoami                # current user
* groups                # group membership
* uname -a              # system architecture
* lspci | grep audio    # audio information

## 15. Advanced Tasks

**Find files containing "java"**

 * find ~ -name "*java*"

## Difference between Service and Application
 
 ### Application
  * An application is a program used directly by the user

 ### Service
  * Runs in background (daemon)
  * Starts automatically with system
  * No direct user interaction

## Wildcards
 * ~	Home directory
 * .	Current directory
 * ..	Parent directory
 * "*"    Matches any number of characters
 * ??	Matches exactly two characters

 ## kill command flags
 * -9 Force kill

 ## File Permissions
 * user.  -u
 * group. -g
 * others -o

 ## chmod (Change Permissions)
 ### examples
  * chmod 755 file.txt 
  * chmod u+x file.txt 
  * chmod g-w file.txt

 ## Ctrl + R (Reverse Search)
  * Ctrl + R
  * ↑ → previous command
  * ↓ → next command
