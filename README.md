# MiniCleaner

Windows cleanup application with a graphical interface. Helps find and delete large/old files, as well as fix corrupted entries in the Windows registry.

**Languages:** [English](README.md) | [Русский](README.ru.md) | [Українська](README.uk.md)

## Features

### File Scanning and Deletion
- Search for large files by specified size
- Filter files by age
- Search for "junk" files (logs, temporary files, caches, etc.)
- Two display modes: by files or by folders
- Safe deletion with confirmation

### Windows Registry Repair
- Search for corrupted entries in startup (Run/RunOnce)
- Search for non-existent paths in Uninstall entries
- Remove problematic entries from the registry

## Requirements

- **OS**: Windows 10/11

## Installation

1. Download `MiniCleaner.exe` from the [Releases](https://github.com/Voytovich/MiniCleaner/releases) section
2. Run `MiniCleaner.exe` — no installation required

## Usage

### "Files" Tab

1. **Select folder to scan**
   - Enter path manually (e.g., `C:\`) or click "Browse..."
   - You can specify the entire drive or a specific folder

2. **Configure filters**
   - **Min. size**: minimum file size to search for (in MB)
   - **Older than**: search only for files older than the specified number of days
   - **Only suspicious junk**: search only for files with extensions (.log, .tmp, .bak, etc.)
   - **Skip system folders**: automatically excludes C:\Windows, C:\Program Files, etc.

3. **Select display mode**
   - **Files**: list of all found files
   - **Folders**: grouping by folders with total size

4. **Start scanning**
   - Click the "Scan" button
   - Progress is displayed in the status bar
   - You can cancel scanning with the "Cancel" button

5. **Delete files**
   - Check the files/folders you need in the "Delete" column
   - Click "Delete Selected"
   - Confirm deletion (this action cannot be undone!)

### "Registry" Tab

1. **Select check types**
- **Startup (Run/RunOnce)**: search for corrupted paths in startup
- **Uninstall (corrupted entries)**: search for non-existent paths in program uninstall entries

2. **Start scanning**
   - Click "Scan Registry"
   - Wait for scanning to complete

3. **Fix entries**
   - Check the problematic entries
   - Click "Fix Selected"
- **Warning**: modifying the registry may affect the system. It is recommended to create a restore point before fixing.

## Supported "Junk" File Types

The application automatically identifies the following file types as potential junk:

- `.log`, `.tmp`, `.temp`, `.bak`, `.old`, `.cache`
- `.ds_store`, `.crdownload`, `.part`, `.dmp`, `.err`
- `.chk`, `.swp`, `.gid`, `.~lock`, `.thumbs`
- `.ini`, `.etl`, `.sqm`, `.msi`, `.msp`

## Color Indication

In the results table, files are displayed in color depending on size:
- **Red**: ≥ 1 GB
- **Orange**: ≥ 100 MB
- **Yellow**: ≥ 10 MB

## Security

- **File deletion is irreversible** — make sure the selected files are really not needed
- **Registry changes** may affect system operation — create a restore point before fixing
- The application does not require administrator rights for scanning, but some registry operations may require elevated privileges

## Excluded Folders (when option is enabled)

When the "Skip system folders" option is enabled, the following are automatically excluded:
- `C:\Windows`
- `C:\Program Files`
- `C:\Program Files (x86)`
- `C:\ProgramData`
- `C:\$Recycle.Bin`
- `C:\Users\All Users`

## Troubleshooting

### Application won't start
- Make sure you are using Windows 10/11
- Check if antivirus is blocking the application
- Try running as administrator

### Scanning is slow
- This is normal for large drives
- Use filters (minimum size, age) to speed up
- Exclude system folders

### No access to some files/folders
- Some system files are protected by Windows
- Run the application as administrator to access protected files

## License

This project is distributed under the **MIT License**. 

You are free to use, modify, and distribute this code, including commercial use. See the [LICENSE](LICENSE) file for details.

## Author

Oleksii Voitovych

