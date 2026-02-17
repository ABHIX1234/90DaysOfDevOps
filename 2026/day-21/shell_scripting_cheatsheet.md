# 🐚 Shell Scripting Cheat Sheet

Your quick reference guide for Bash scripting (DevOps Ready 🚀)

---

# 📌 Quick Reference Table

| Topic    | Key Syntax               | Example                            |
| -------- | ------------------------ | ---------------------------------- |
| Variable | `VAR="value"`            | `NAME="DevOps"`                    |
| Argument | `$1`, `$2`               | `./script.sh arg1`                 |
| If       | `if [ condition ]; then` | `if [ -f file ]; then`             |
| For loop | `for i in list; do`      | `for i in 1 2 3; do`               |
| Function | `name() { ... }`         | `greet() { echo "Hi"; }`           |
| Grep     | `grep pattern file`      | `grep -i "error" log.txt`          |
| Awk      | `awk '{print $1}' file`  | `awk -F: '{print $1}' /etc/passwd` |
| Sed      | `sed 's/old/new/g' file` | `sed -i 's/foo/bar/g' config.txt`  |

---

# 1️⃣ Basics

## Shebang

Defines interpreter.

```bash
#!/bin/bash
```

## Run Script

```bash
chmod +x script.sh
./script.sh
bash script.sh
```

## Comments

```bash
# Single line comment
ls -l  # Inline comment
```

## Variables

```bash
NAME="Avnish"
echo $NAME
echo "$NAME"   # Expands
echo '$NAME'   # Literal
```

## User Input

```bash
read -p "Enter name: " NAME
```

## Command Line Arguments

```bash
echo $0   # Script name
echo $1   # First arg
echo $#   # Total args
echo $@   # All args
echo $?   # Last exit status
```

---

# 2️⃣ Operators & Conditionals

## String

```bash
[ "$a" = "$b" ]
[ -z "$a" ]   # Empty
[ -n "$a" ]   # Not empty
```

## Integer

```bash
[ $a -eq $b ]
[ $a -gt 5 ]
```

## File Tests

```bash
[ -f file ]
[ -d dir ]
[ -r file ]
```

## If Syntax

```bash
if [ condition ]; then
  echo "True"
elif [ condition ]; then
  echo "Else If"
else
  echo "False"
fi
```

## Logical Operators

```bash
[ -f file ] && echo "Exists"
[ -f file ] || echo "Missing"
! [ -f file ]
```

## Case

```bash
case $1 in
  start) echo "Starting" ;;
  stop) echo "Stopping" ;;
  *) echo "Invalid" ;;
esac
```

---

# 3️⃣ Loops

## For (List)

```bash
for i in 1 2 3; do
  echo $i
done
```

## For (C-style)

```bash
for ((i=1;i<=5;i++)); do
  echo $i
done
```

## While

```bash
while [ $i -le 5 ]; do
  echo $i
  ((i++))
done
```

## Until

```bash
until [ $i -gt 5 ]; do
  echo $i
  ((i++))
done
```

## Break / Continue

```bash
break
continue
```

## Loop Files

```bash
for file in *.log; do
  echo $file
done
```

## Read Command Output

```bash
while read line; do
  echo $line
done < file.txt
```

---

# 4️⃣ Functions

## Define & Call

```bash
greet() {
  echo "Hello"
}

greet
```

## Arguments

```bash
add() {
  echo $(($1 + $2))
}
add 2 3
```

## Return

```bash
return 0   # Exit status
echo "value"  # Output value
```

## Local Variable

```bash
myfunc() {
  local VAR="test"
}
```

---

# 5️⃣ Text Processing

## Grep

```bash
grep -i "error" file
grep -r "pattern" .
grep -c "error" file
grep -n "error" file
grep -v "info" file
grep -E "error|fail" file
```

## Awk

```bash
awk '{print $1}' file
awk -F: '{print $1}' /etc/passwd
awk 'BEGIN {print "Start"} {print $1} END {print "Done"}' file
```

## Sed

```bash
sed 's/old/new/g' file
sed -i 's/foo/bar/g' file
sed '2d' file
```

## Cut

```bash
cut -d":" -f1 /etc/passwd
```

## Sort

```bash
sort file
sort -n file
sort -r file
sort file | uniq
```

## Uniq

```bash
uniq file
uniq -c file
```

## Tr

```bash
tr 'a-z' 'A-Z'
tr -d ' '
```

## WC

```bash
wc -l file
wc -w file
wc -c file
```

## Head / Tail

```bash
head -n 5 file
tail -n 5 file
tail -f file
```

---

# 6️⃣ Useful One-Liners

## Delete files older than 7 days

```bash
find /path -type f -mtime +7 -delete
```

## Count lines in all .log files

```bash
wc -l *.log
```

## Replace string in multiple files

```bash
sed -i 's/old/new/g' *.conf
```

## Check service status

```bash
systemctl is-active nginx
```

## Disk usage alert (>80%)

```bash
df -h | awk '$5+0 > 80 {print $0}'
```

## Real-time error monitoring

```bash
tail -f app.log | grep --line-buffered "ERROR"
```

---

# 7️⃣ Error Handling & Debugging

## Exit Codes

```bash
exit 0   # Success
exit 1   # Failure
echo $?  # Last status
```

## Strict Mode

```bash
set -e      # Exit on error
set -u      # Unset variable error
set -o pipefail  # Catch pipe errors
set -x      # Debug mode
```

## Trap

```bash
trap 'echo "Cleaning up"' EXIT
```

---

# ✅ Pro Tip

Always start production scripts with:

```bash
#!/bin/bash
set -euo pipefail
```

---

🚀 Built for quick revision during DevOps projects.

#90DaysOfDevOps #DevOpsKaJosh #TrainWithShubham
