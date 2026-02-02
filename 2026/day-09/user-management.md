# Day 09 – Linux User & Group Management Challenge

## Users & Groups Created

- Users: tokyo, berlin, professor, nairobi
- Groups: developers, admins, project-team

## Group Assignments

- tokyo → developers, project-team
- berlin → developers, admins
- professor → admins
- nairobi → project-team

## Directories Created

- /opt/dev-project → group: developers → permissions: 775
- /opt/team-workspace → group: project-team → permissions: 775

## Commands Used

- useradd -m
- passwd
- groupadd
- usermod -aG
- mkdir
- chgrp
- chmod
- groups
- ls -ld
- sudo -u username command

## What I Learned

- Linux group management is essential for team-based access control
- Shared directories require correct group ownership and permissions
- sudo -u is useful to test real user access without logging out
