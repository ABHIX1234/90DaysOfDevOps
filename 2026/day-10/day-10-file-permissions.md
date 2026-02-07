# Day 10 Challenge – File Permissions & File Operations

## Files Created

- devops.txt
- notes.txt
- script.sh
- project/

## Permission Changes

### script.sh

- Before: -rw-r--r--
- After: -rwxr-xr-x

### devops.txt

- Before: -rw-r--r--
- After: -r--r--r--

### notes.txt

- Permission set to: 640

### project/

- Permission set to: 755

## Commands Used

- touch devops.txt
- echo "text" > notes.txt
- vim script.sh
- chmod +x script.sh
- chmod a-w devops.txt
- chmod 640 notes.txt
- mkdir project
- chmod 755 project

## What I Learned

1. Linux permissions control who can read, write, and execute files.
2. chmod can be used with symbols (+x, -w) or numbers (755, 640).
3. Execute permission is required to run scripts.
