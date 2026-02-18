![Uni-Chronicle Logo](https://github.com/user-attachments/assets/445f98f4-1abc-41fa-8eb9-f193f81b99fa)

## Uni-Chronicle : An automated shell solution for academic file management on Ubuntu.

![Version](https://img.shields.io/badge/version-1.0.0-512DA8?style=flat)
![Shell](https://img.shields.io/badge/Shell-Bash-1B5E20?logo=gnubash&logoColor=white&style=flat)
![OS](https://img.shields.io/badge/OS-Ubuntu-E95420?logo=ubuntu&logoColor=white&style=flat)
![Automation](https://img.shields.io/badge/Automation-Cron%20Jobs-00796B?style=flat)
![Backup](https://img.shields.io/badge/Backup-Rsync%20%7C%20Zip-0288D1?style=flat)
![License](https://img.shields.io/badge/License-Academic-4CAF50?style=flat)

### Overview

Uni-Chronicle is a Linux-based automation suite that keeps semester assets organized, backed up, and share-ready. Through a modular Bash workflow, students can create structured course directories, schedule cron-powered backups, extract resource bundles, and wind down a semester without manual cleanup.

### Why Uni-Chronicle?

- eliminates chaotic course folders and scattered files
- enforces reliable, timestamped backups
- packages assignments or lab resources on demand
- prevents missed cleanups at semester end
- centralizes logs and configuration for easy auditing

### System Architecture

- `config.txt` captures semester metadata.
- `log_file.txt` records every operation with timestamps.
- Cron handles recurring backups with duplicate protection.
- Directory generators scaffold theory and lab trees.
- Resource packager/restore scripts manage sharable archives.

### System Flow Diagram

![Uni-Chronicle system flow](main/System%20Flow%20Diagram.png)

Initial setup flows through directory creation, backup scheduling, resource extraction, and final termination, covering the full academic lifecycle.

### Core Features

**1. Semester Setup**

- creates a parent folder per semester (e.g., `Spring_2024`)
- provisions theory folders (Assignments, Presentations, Mid-Essentials, Final-Essentials, Others)
- provisions lab folders (Reports, Projects, Presentations, Lab Tasks, Others)

**2. Backup Management**

- daily cron-driven backups and on-demand snapshots
- compressed, timestamped archives with restore prompts
- duplicate cron entries are automatically prevented

**3. Resource Extraction & Sharing**

- pick course(s) and resource types to export
- leverages `rsync` + `zip` for packaging
- auto-renames deliverables to avoid collision

**4. Schedule Management**

- inspect backup schedule status
- edit backup time windows
- purge cron jobs cleanly when needed

**5. Semester Termination**

- archives the entire semester
- purges retired backups and directories
- clears scheduled cron entries to prep for next term

### User Interface

- menu-driven CLI with numeric navigation
- color-coded feedback (green for success, red for issues) for non-technical usability

### Technologies Used

- Bash scripting on Ubuntu
- Cron for automation
- `zip` and `rsync` for backup packaging
- core GNU/Linux file system commands

### Performance & Reliability

- validated across multiple semester structures and stress scenarios
- dependable backup execution with accurate restore routines
- strong error logging and defensive input handling

### How to Use

```bash
git clone https://github.com/yourusername/Uni-Chronicle.git
cd Uni-Chronicle
chmod +x main.sh
./main.sh
```

The setup wizard collects semester names, course lists, backup locations, and preferred backup times, then writes them to `config.txt` while logging all actions.

### Project Workflow

1. requirement analysis
2. system design
3. UI and feature development
4. testing and debugging
5. documentation and deployment

### Academic Value

Uni-Chronicle showcases shell scripting for real academic logistics: automation, cron scheduling, file system design, and end-to-end problem solving for student workflows.
