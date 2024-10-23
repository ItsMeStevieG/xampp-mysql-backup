# XAMPP MySQL Backup for Windows v1.0

XAMPP MySQL Backup for Windows v1.0 by **Steven Graham** is a batch script that allows you to easily back up all MySQL databases on your local XAMPP server. It offers an option to back up either all databases (including system schemas) or only user-created databases (excluding system schemas and phpMyAdmin).

## Features
- **Simple to Use**: Just run the script and follow the prompts.
- **Flexible Backup Options**: Choose between backing up all databases or only user-created databases.
- **Automatic Timestamp**: Backup file names are automatically generated with a timestamp in `YYYYMMDD-HHMMSS` format.
- **XAMPP Path Flexibility**: Specify a custom XAMPP path or use the default (`C:\xampp`).

## Requirements
- Windows OS
- XAMPP installed
- MySQL databases hosted on XAMPP

## Installation
1. Download the script `backup.bat` from this repository.
2. Save the script in the backup destination folder.

## Usage
1. **Run the Script**: Double-click `backup.bat` or run it from the command prompt.
2. **Enter the XAMPP Path**: You will be prompted to enter the path to your XAMPP installation. The default is `C:\xampp`, so you can press Enter if this is correct.
3. **Enter MySQL Password**: You will be prompted to enter the MySQL root password. If no password is set, simply press Enter.
4. **Select Backup Type**: You will be prompted to choose the type of backup:
    - `1` for all databases (including system schemas).
    - `2` for only user-created databases (excluding system schemas and phpMyAdmin). The default option is `1`.
5. **Backup File Created**: The script will generate a backup file in the format `xampp_mysql_backup_YYYYMMDD-HHMMSS.sql` in the folder where the script is run.

### Example
```bash
XAMPP MySQL Backup for Windows v1.0 by Steven Graham
==================================================
Enter the path to XAMPP (default is C:\xampp): C:\xampp
Enter MySQL root password (press Enter for none):
Do you want to back up:
1. All databases (including system schemas) [default]
2. Only user-created databases (excluding system schemas and phpmyadmin)
Enter 1 or 2 (default is 1): 1
Backup complete! The dump is saved to xampp_mysql_backup_20241023-112758.sql
```

### Command Line Execution
You can also run the script from the command prompt:
```bash
C:\path\to\backup.bat
```
### File Structure
```plaintext
.
├── backup.bat           # Main script to back up MySQL databases
└── README.md            # Documentation (this file)
```
### Troubleshooting
* **MySQL not found:** Ensure you enter the correct path to your XAMPP installation. The MySQL binaries should be located in `C:\xampp\mysql\bin` or similar.
* **Access Denied:** Ensure you have the correct MySQL root password, or that MySQL is running in XAMPP.
### License
This project is open-source and free to use under the MIT License. See the [[LICENSE.md](LICENSE.md)](https://github.com/ItsMeStevieG/xampp-mysql-backup/tree/main?tab=MIT-1-ov-file) file for more information.
