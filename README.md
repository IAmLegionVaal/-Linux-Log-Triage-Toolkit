# Linux Log Triage Toolkit

A read-only Bash toolkit for collecting and summarising Linux journal, authentication, kernel, boot, and application error evidence.

## Features

- Configurable time window and keyword filtering
- Critical and error-level journal entries
- Authentication failures and sudo activity
- Kernel warnings, storage errors, OOM events, and service failures
- Boot-specific error review
- Top recurring messages and affected units
- Text, CSV, and JSON summary outputs

## Usage

```bash
chmod +x src/linux_log_triage.sh
sudo ./src/linux_log_triage.sh --hours 24
```

Keyword example:

```bash
sudo ./src/linux_log_triage.sh --hours 72 --keyword "disk|I/O|ext4"
```

## Safety

The script only reads logs and creates local report files. It does not rotate, clear, compress, or alter system logs.

## Privacy

Logs can contain usernames, IP addresses, hostnames, file paths, and application data. Review and sanitise reports before external sharing.

## Author

Dewald Pretorius — L2 IT Support Engineer
