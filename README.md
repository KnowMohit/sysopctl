# sysopctl - System Operations Control Tool

## Overview
`sysopctl` is a command-line tool designed to manage system operations, such as analyzing logs and backing up files. This tool simplifies critical system management tasks, enabling users to efficiently analyze log data and perform backups.

## Installation
To install `sysopctl`, clone the repository and navigate to the project directory:
bash
git clone <repository-url>
cd sysopctl_project


- **Instruction to Replace Repository URL**: Make sure to replace `<repository-url>` with the actual URL of your GitHub repository.

### Step 4: Usage

**Purpose**: Explain how to use the commands available in your tool.

## Usage
### Analyze Logs
To analyze the last 10 critical log entries, use the following command:

bash
sysopctl logs analyze


# Screenshots

1. Manual Page
![Screenshot (63)](https://github.com/user-attachments/assets/d6ce92c8-dfa8-46f2-b097-00ce0f74e87f)
![Screenshot (64)](https://github.com/user-attachments/assets/64404a70-7c28-403a-8643-d390a1ba1bfc)

2. Help Option
![Screenshot (65)](https://github.com/user-attachments/assets/741f5939-d5a0-498e-be25-d3049bc10cbe)

3. Version Info
![Screenshot (66)](https://github.com/user-attachments/assets/e4e04e9c-cae4-418e-841a-893aa7bde59a)

4. Service List
![Screenshot (67)](https://github.com/user-attachments/assets/ed0a2fe7-b49a-4184-a11e-d453e9cabf10)

5. System Load
![Screenshot (68)](https://github.com/user-attachments/assets/28a19769-a81a-4af5-b717-24448c8b4cc4)

6. Service Start/Stop
![Screenshot (69)](https://github.com/user-attachments/assets/1a774cea-17a8-4780-8d55-ba6b98c6fac6)

7. Disk Usage
![Screenshot (70)](https://github.com/user-attachments/assets/e61dc0f2-e39f-4f39-8307-852232e70ac1)

8. Monitor System
![Screenshot (72)](https://github.com/user-attachments/assets/7df9de6e-49ae-49af-b2b3-64cae6d0af05)
![Screenshot (73)](https://github.com/user-attachments/assets/248acb47-b549-4253-a649-ff22d3d9b063)

9. Analyze System Log
![Screenshot (74)](https://github.com/user-attachments/assets/fdf206e7-9361-4835-801e-76971f88de89)

10. Backup System Files
![Screenshot (75)](https://github.com/user-attachments/assets/5ba08a73-b81e-4605-9fb8-91e7d8e3bd5f)

# System Architecture & Workflow
[xenonStack.drawio.pdf](https://github.com/user-attachments/files/17398712/xenonStack.drawio.pdf)

# Workflow for sysopctl logs analyze-
Start
Input Command: User inputs sysopctl logs analyze.
Process: Execute journalctl -p crit -n 10.
Output: Display critical logs.
End

## Workflow for sysopctl backup <path>
Start
Input Command: User inputs sysopctl backup <path>.
Validation: Check if the path is valid.
If valid: Proceed to backup.
If invalid: Show error message.
Process: Use rsync to back up the specified path to /backup/.
Output: Display backup completion message.
End

## System Architecture for sysopctl

# Components:
User Interface: Command line interface where users input commands.
Sysopctl: Main utility handling user commands.
Rsync: For backup operations.
Journalctl: For log analysis.
Backup Directory: Where files are stored.

# Relationship:
Users interact with the User Interface.
User commands are processed by sysopctl.
sysopctl invokes rsync or journalctl as needed.
Backup files are stored in the Backup Directory.
