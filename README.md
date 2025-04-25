# Malware Detection and Removal Tool

**Created by Jacob Pugh and Brandon Magana**

---

## Overview

This project is a lightweight, modular command-line tool designed for **malware detection and removal**. It scans files, directories, and running processes for malicious activity, using a local SQLite database to manage scan histories, quarantines, and malware signatures.

---

## Key Features

- **Signature-Based File Scanning**  
  Match file hashes against a malware signature database.

- **Process Hook Detection**  
  Analyze running processes for signs of memory tampering.

- **Historical File Size Anomaly Detection**  
  Detect abnormal growth trends in file sizes over time.

- **File Quarantine System**  
  Securely isolate infected files in a quarantine folder.

- **Scan Overview Reports**  
  Generate clear reports showing scan results and malicious detections.

- **Automatic Signature Updates**  
  Pull the latest malware signatures from Malware Bazaar.

---

## Basic Usage

- **Scan a file or directory:**
  ```bash
  python main.py scan path/to/file_or_directory
  ```

- **Scan running processes:**
  ```bash
  python main.py scan --process_scan
  ```

- **Update malware signatures:**
  ```bash
  python main.py update
  ```

- **Generate a scan report:**
  ```bash
  python main.py report path/to/report.txt
  ```

---

## Structure

```
├── main.py                 # CLI entry point
├── database_handler.py      # Database management
├── structs.py               # Dataclasses
├── quarantine.py            # File quarantine logic
├── utils.py                 # Utilities (hashing, logging)
├── scanners/                # Different scanning modules
└── database/                # SQL scripts and schema
```

---

## About

This tool was developed by **Jacob Pugh** and **Brandon Magana** as part of a cybersecurity final project, completed in April 2025.
