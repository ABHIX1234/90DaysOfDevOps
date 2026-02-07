# Day 11 – File Ownership Challenge

## Files & Directories Created

- devops-file.txt
- team-notes.txt
- project-config.yaml
- app-logs/
- heist-project/
- heist-project/vault/gold.txt
- heist-project/plans/strategy.conf
- bank-heist/
- bank-heist/access-codes.txt
- bank-heist/blueprints.pdf
- bank-heist/escape-plan.txt

## Ownership Changes

- devops-file.txt: avnish:avnish → tokyo → berlin
- team-notes.txt: avnish:avnish → avnish:heist-team
- project-config.yaml: avnish:avnish → professor:heist-team
- app-logs/: avnish:avnish → berlin:heist-team
- heist-project/: recursive → professor:planners
- access-codes.txt → tokyo:vault-team
- blueprints.pdf → berlin:tech-team
- escape-plan.txt → nairobi:vault-team

## Commands Used

- ls -l
- chown
- chgrp
- chown owner:group
- chown -R
- useradd
- groupadd

## What I Learned

1. Every Linux file has an owner and a group.
2. `chown` can change both owner and group in one command.
3. Recursive ownership is critical for managing project directories in DevOps.
