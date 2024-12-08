# Linux_Maintenance

This Python script is designed to automate essential maintenance tasks on a Linux system, helping to keep it running smoothly by performing updates, cleanup, and performance tuning. It is suitable for personal and server environments.

# Features

- Updates package lists and installs available updates using the system's package manager.
- Removes unused packages and cleans up package cache.
- Deletes files from /tmp and /var/tmp to free up disk space.
- Truncates old log files in /var/log to save disk space.
- Removes cache files for common browsers and applications (e.g., Chrome, Firefox).
- Clears DNS cache to refresh network configurations.
- Optimizes the vm.swappiness kernel parameter for better performance.
- Generates a disk usage report and saves it in the home directory for review.
- Empties the recycle bin for the current user.

# Requirements

Software Dependencies

    Python 3.x
    os, shutil, and subprocess

# Permissions

The script requires elevated privileges to perform some tasks. Use sudo to run it:

    sudo python3 linux_maintenance.py

# Installation and Usage

- Download the Script

- Make the Script Executable
  
      sudo chmod +x linux_maintenance.py

- Run the Script
  
      sudo python3 linux_maintenance.py

# View Logs and Reports

- Logs for script actions are saved in ~/maintenance_log.txt.
- Disk usage reports are saved in the home directory as disk_usage_report.txt.

# Customization

- You can add or remove directories for temporary file or cache cleanup by editing the corresponding sections in the script.
- Adjust the vm.swappiness parameter value in the script to customize how aggressively the kernel swaps memory. The default is set to 10 for performance optimization.

# Known Issues

- The script may not detect and clean caches for non-standard browsers or applications.
- Some cleanup actions might require manual adjustments for non-default system configurations.
