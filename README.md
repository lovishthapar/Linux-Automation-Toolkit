# 🛠️ Linux-Automation-Toolkit
A modular, command-line Python toolkit designed to automate essential Linux system tasks including system monitoring, network diagnostics, port scanning, and backup creation — all wrapped in a clean CLI using click.

---

## 🚀 Features

- 🔍 **System Monitoring** — Track CPU, RAM, and disk usage in real-time.
- 🌐 **Network Info** — View IP, MAC, gateway, DNS, and run ping checks.
- 🛡️ **Port Scanner** — Scan open TCP ports on any target.
- 🗃️ **Backup Tool** — Create timestamped ZIP backups of directories.

---

## 🧠 Why It’s Worth It

- Combines multiple Linux admin tools into one CLI.
- Great for sysadmins, students, or devs managing Linux environments.
- Modular, testable, and extensible.

---

## 📌 Real-World Scenarios

Imagine you're given with the responsibility of maintaining 'n' numbers of Linux-based computers to keep systems running smoothly, monitor usage, 
and create regular backups - all without enterprise tools.
This is where this toolkit helps:
- Regularly checks `CPU`, `RAM`, and `disk usage` with one command, identifying overloaded or failing systems.
- `Network command` ensures all devices are online and their DNS/gateway configs are correct.
- `Port scanner` finds unnecessary open ports and secures the systems.
- Automate daily `backups` of important logs and scripts using the backup tool.

---

## 📁 Project Structure

```
Linux-Automation-Toolkit/
├── modules/               # Core functionality modules
│   ├── __init__.py
│   ├── backup_tool.py     # Handles ZIP backups of directories
│   ├── network_info.py    # Gathers IP, MAC, DNS, and ping checks
│   ├── port_scanner.py    # Scans target for open TCP ports
│   └── system_monitor.py  # Displays CPU, RAM, and disk usage
│
├── tests/                 # Unit tests for each module
│   ├── __init__.py
│   ├── test_backup_tool.py
│   ├── test_network_info.py
│   ├── test_port_scanner.py
│   └── test_system_monitor.py
│
├── config/                # Configuration and settings
│   └── settings.py
│
├── toolkit.py             # Main CLI entry point using Click
├── Makefile               # Automation commands (test, coverage, clean)
├── requirements.txt       # List of Python dependencies
├── .gitignore             # Files and folders to ignore in git
├── README.md              # This file
└── LICENSE                # Open-source license
```

---

## 🔧 Installation

### Clone the repository
```
git clone https://github.com/riaagarwal21/Linux-Automation-Toolkit
```

### Install dependencies
```
python3 -m pip install -r requirements.txt
```

### Run the toolkit
```
python3 toolkit.py --help
```

### Testing

Open your project root and use the following commands:
```
make run                               # Runs the CLI toolkit with --help to show available commands.
make test                              # Runs all unit tests using pytest.
make coverage                          # Runs tests and generates an HTML coverage report.
make coverage-view                     # Opens the generated coverage report in Chromium browser (Linux systems).
make backup source=<path> dest=<path>  # Calls the backup module through toolkit.py and zips the content of source directory.
make clean                             # Cleans up __pycache__, .pytest_cache, and htmlcov directories.
```

If you're running for the first time:
```
make run
make test
make coverage
make coverage-view
```

If you're re-running:
```
make clean
make run
make test
make coverage
make coverage-view
```

---
