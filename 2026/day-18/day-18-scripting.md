# 📘 Day 18 – Shell Scripting: Functions & Advanced Concepts

## Overview

Today I learned how to write cleaner, reusable, and production-safe shell scripts using:

- ✅ Functions
- ✅ Return values
- ✅ Local variables
- ✅ Strict mode (`set -euo pipefail`)
- ✅ Real-world system reporting script

---

# Functions in Shell Script

Functions help organize code and make it reusable.

## 🔹 Basic Syntax

```bash
greet() {
    echo "Hello $1"
}

greet "Avnish"
```

---

# Return Values in Bash

In Bash:

- `return` gives exit status (0–255)
- `0` → success
- non-zero → failure

## 🔹 Example

```bash
check_file() {
    if [ -f "$1" ]; then
        return 0
    else
        return 1
    fi
}

check_file "test.txt"

if [ $? -eq 0 ]; then
    echo "File exists"
else
    echo "File not found"
fi
```

---

# Local Variables

Using `local` inside functions prevents variable conflicts.

## 🔹 Example

```bash
greet() {
    local name="$1"
    echo "Hello $name"
}
```

### Why Important?

- Prevents overwriting global variables
- Makes script modular
- Best practice in production scripts

---

# 4️ Strict Mode (Production Safety)

```bash
set -euo pipefail
```

## 🔹 Meaning

| Option        | Purpose                               |
| ------------- | ------------------------------------- |
| `-e`          | Exit immediately if command fails     |
| `-u`          | Exit if undefined variable is used    |
| `-o pipefail` | Fail if any command in pipeline fails |

## 🔹 Why Use It?

- Prevents silent failures
- Makes debugging easier
- Production-safe scripting
- DevOps best practice

---

# 5️⃣ Real-World Example – System Report Script

```bash
#!/bin/bash
set -euo pipefail

system_report() {
    echo "---- CPU Usage ----"
    top -bn1 | head -n 5

    echo ""
    echo "---- Memory Usage ----"
    free -h

    echo ""
    echo "---- Disk Usage ----"
    df -h
}

system_report
```

---

# Key Takeaways

- Functions improve readability and reusability
- Always use `local` inside functions
- Use return codes properly
- Always enable strict mode in production scripts
- Validate inputs before execution

---

**Why use functions in shell scripting?**

Answer:

- Code reusability
- Better readability
- Easier debugging
- Modular automation scripts

---

# Final Learning Outcome

Today I moved from writing basic scripts to writing structured, production-ready shell scripts — an essential skill for DevOps Engineers.
