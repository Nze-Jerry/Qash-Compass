# Installation Guide

This guide will walk you through the process of installing Qash Compass on your Windows computer.

## System Requirements

Before installing, ensure your system meets the following requirements:

- **Operating System**: Windows 10 (64-bit) or Windows 11
- **Processor**: 1 GHz or faster processor
- **RAM**: 4 GB minimum (8 GB recommended)
- **Storage**: 500 MB available disk space
- **Display**: 1366 x 768 screen resolution or higher
- **Administrator Rights**: Required for installation

## Download

1. Visit the [Releases](https://github.com/Nze-Jerry/Qash-Compass/releases) page
2. Download the latest version of `QashCompass-Setup.exe`
3. Verify the file size and checksum (provided in the release notes)

## Installation Steps

### Standard Installation

1. **Locate the Installer**
   - Navigate to your Downloads folder
   - Find `QashCompass-Setup.exe`

2. **Run the Installer**
   - Right-click on `QashCompass-Setup.exe`
   - Select "Run as administrator"
   - If prompted by Windows Defender SmartScreen, click "More info" then "Run anyway"

3. **Accept User Account Control (UAC)**
   - Click "Yes" when prompted to allow the installer to make changes

4. **Follow Installation Wizard**
   - Read and accept the License Agreement
   - Choose installation location (default: `C:\Program Files\Qash Compass`)
   - Select additional options:
     - Create Desktop shortcut (recommended)
     - Create Start Menu entry (recommended)
   - Click "Install"

5. **Complete Installation**
   - Wait for the installation to complete
   - Click "Finish" to close the installer
   - Optionally, launch Qash Compass immediately

## First Launch

After installation:

1. **Launch Application**
   - Double-click the desktop shortcut, or
   - Search for "Qash Compass" in the Start Menu

2. **Initial Setup Wizard**
   - Set your preferred currency
   - Choose your date/time format
   - Set up data encryption (optional but recommended)
   - Create your first financial account

3. **Create Your Profile**
   - Enter your name (for personalization)
   - Set your financial goals (optional)

## Silent Installation (Advanced)

For IT administrators deploying to multiple machines:

```cmd
QashCompass-Setup.exe /S /D=C:\Program Files\Qash Compass
```

Parameters:
- `/S` - Silent installation (no UI)
- `/D` - Custom installation directory (must be last parameter)

## Updating

To update to a newer version:

1. Download the latest installer from the Releases page
2. Run the new installer (existing data will be preserved)
3. Follow the installation wizard
4. Your settings and data will be automatically migrated

**Note**: Always backup your data before updating (File → Backup Data)

## Uninstallation

To remove Qash Compass:

### Using Windows Settings

1. Open Windows Settings (Win + I)
2. Go to "Apps" → "Apps & features"
3. Find "Qash Compass" in the list
4. Click "Uninstall" and confirm

### Using Control Panel

1. Open Control Panel
2. Go to "Programs and Features"
3. Find "Qash Compass"
4. Right-click and select "Uninstall"

**Important**: Uninstalling will not delete your data files. To completely remove all data:
- Navigate to `%APPDATA%\QashCompass`
- Delete the folder manually

## Data Location

Your financial data is stored at:
- **Windows 10/11**: `C:\Users\[YourUsername]\AppData\Roaming\QashCompass\`

This includes:
- Database files
- Backups
- Configuration files
- Export files

## Troubleshooting Installation

### Installer Won't Run

- **Solution**: Ensure you have administrator privileges
- **Solution**: Temporarily disable antivirus software
- **Solution**: Check if .NET Framework 4.8 or later is installed

### Installation Fails

- **Error**: "Installation directory is not writable"
  - **Solution**: Choose a different installation directory or run as administrator

- **Error**: "Another version is already installed"
  - **Solution**: Uninstall the existing version first

### Application Won't Launch

- Check Windows Event Viewer for error details
- Ensure .NET Framework is installed and up to date
- Try running in compatibility mode (Windows 8)
- Reinstall the application

## Support

If you encounter issues during installation:

1. Check the [Troubleshooting Guide](TROUBLESHOOTING.md)
2. Review [FAQ](FAQ.md)
3. Search [existing issues](https://github.com/Nze-Jerry/Qash-Compass/issues)
4. Create a new issue with:
   - Your Windows version
   - Installation error messages
   - Screenshots of the problem

## Next Steps

After successful installation:

- Read the [User Guide](USER_GUIDE.md) to get started
- Set up your first budget
- Import existing financial data (if applicable)
- Explore the features and settings
