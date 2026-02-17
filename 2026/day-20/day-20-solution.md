# Day 20 – Bash Scripting Challenge

## Log Analyzer and Report Generator

## Objective

Automate log file analysis and generate a structured summary report.

---

## Approach

### Step 1: Input Validation

- Used `$#` to validate arguments
- Used `-f` to verify file existence
- Exit with error messages if validation fails

### Step 2: Error Count

- Used `grep -Eci "ERROR|Failed"`
- Counted total error-related lines

### Step 3: Critical Events

- Used `grep -n "CRITICAL"`
- Displayed line numbers with matching lines

### Step 4: Top 5 Error Messages

- Extracted ERROR lines using `grep`
- Removed timestamps using `awk`
- Used:
  - `sort`
  - `uniq -c`
  - `sort -rn`
  - `head -5`

### Step 5: Report Generation

- Generated dynamic filename using:
  `date +%Y-%m-%d`
- Used block redirection `{ } > file`
- Included:
  - Date
  - File name
  - Total lines
  - Error count
  - Top errors
  - Critical events

### Step 6: Archive

- Used `mkdir -p archive`
- Moved file using `mv`

---

## Commands Used

- grep
- awk
- sort
- uniq
- wc
- head
- date
- mkdir
- mv

---

## Key Learnings

1. How to combine multiple Unix tools into a production-ready automation script.
2. Defensive scripting using `set -euo pipefail`.
3. Structured report generation using redirection and command substitution.

---

## Outcome

Successfully built a real-world log analyzer that:

- Processes logs automatically
- Generates reports
- Archives processed logs

#90DaysOfDevOps #DevOpsKaJosh #TrainWithShubham
