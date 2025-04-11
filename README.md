# OS Networking Final Project 2025
## Malware Detection and Removal System

### Team Members:
- **Member 1**: Jacob Pugh - jacobdean.pugh@calbaptist.edu
- **Member 2**: Brandon Magana - brandon.magana@calbaptist.edu

### Platform:
- **Operating System**: Windows 10/11
- **Programming Language**: Python 3.10
- **Execution**: Command Line Interface (CLI)

### Project Goals:
Create a CLI tool that performs the following:
- Detects a potential malware infection on a Windows system.
- Quarantines the infected files.
- Removes the infected files.
- Provides a report of the actions taken.

### Feature Plan:

#### Detection:
- Scan the system for known malware signatures.
- Use Malwarebytes DB to identify potential threats.
- Check for suspicious file behavior (e.g., unusual file access patterns, registry changes).

#### Quarantine:
- Move infected files to a secure location to prevent further damage.
- Startup Script Scanner: Check for suspicious startup scripts and remove them.

#### Removal:
- Delete infected files from the quarantine location.
- Remove any registry entries associated with the malware.
- Remove any scheduled tasks associated with the malware.
- Remove any network connections associated with the malware.
- Remove any services associated with the malware.
- Remove any drivers associated with the malware.

#### Report:
- Generate a report of the actions taken, including:
    - List of detected malware.
    - List of quarantined files.
    - List of removed files.
    - List of registry entries removed.
    - List of scheduled tasks removed.
    - List of network connections removed.
    - List of services removed.
    - List of drivers removed.
- Recommendations for further action (e.g., system restore, antivirus scan).

### File Structure:
```
malware_tool/
│
├── main.py               # Entry point
├── scanner.py            # Custom hash scanner
├── quarantine.py         # Move/remove suspicious files
├── autorun_check.py      # SysInternals startup scan
├── advisory.py           # Recommendations
├── utils.py              # Logging, hashing, etc.
├── hashes.db             # List of known malicious hashes
├── quarantine/           # Encrypted/isolated storage for flagged files
└── report.txt            # Output log
```

### Timeline:
| Week         | Tasks                                                                 |
|--------------|----------------------------------------------------------------------|
| Week 1 (4/10–4/14) | Set up project repo, hash scanner, logging system                |
| Week 2 (4/15–4/20) | Quarantine, removal, SysInternals integration                   |
| Week 3 (4/21–4/24) | Advisory system, CLI polish, testing                            |
| 4/25 (Deadline)    | Final test and submission                                       |