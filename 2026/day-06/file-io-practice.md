# Day 06 – Linux File Read & Write Practice

## File Created

notes.txt

## Commands Practiced

1. touch notes.txt  
   → Creates an empty file named notes.txt

2. echo "This is Line 1" > notes.txt  
   → Writes the first line (overwrites file if exists)

3. echo "This is Line 2" >> notes.txt  
   → Appends a new line to the file

4. echo "This is Line 3" | tee -a notes.txt  
   → Displays output and appends it to the file

5. cat notes.txt  
   → Displays the full content of the file

6. head -n 2 notes.txt  
   → Displays the first 2 lines of the file

7. tail -n 2 notes.txt  
   → Displays the last 2 lines of the file

## Key Learning

Redirection ( > , >> ) and tee are essential for handling logs and config files in DevOps.
