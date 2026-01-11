# Troubleshooting Guide

This guide helps you resolve common issues with Qash Compass.

## Table of Contents

- [Installation Issues](#installation-issues)
- [Launch Problems](#launch-problems)
- [Data Issues](#data-issues)
- [Performance Issues](#performance-issues)
- [Display Issues](#display-issues)
- [Backup & Restore Issues](#backup--restore-issues)
- [Import/Export Issues](#importexport-issues)
- [Error Messages](#error-messages)

## Installation Issues

### Installer Won't Run

**Symptoms**: Double-clicking the installer does nothing or shows an error.

**Solutions**:
1. Right-click installer → "Run as administrator"
2. Check if you have sufficient disk space (500+ MB)
3. Temporarily disable antivirus software
4. Download the installer again (may have been corrupted)
5. Ensure .NET Framework 4.8 or later is installed

### "Installation directory is not writable"

**Solution**:
- Run installer as administrator
- Choose a different installation directory
- Check disk permissions

### "Another version is already installed"

**Solution**:
1. Uninstall existing version first:
   - Settings → Apps → Qash Compass → Uninstall
2. Run the new installer

### Installation Fails Silently

**Solution**:
1. Check Windows Event Viewer:
   - Windows Logs → Application
   - Look for errors around installation time
2. Try running from Command Prompt:
   ```cmd
   QashCompass-Setup.exe /log install.log
   ```
3. Review install.log for specific errors

## Launch Problems

### Application Won't Start

**Symptoms**: Clicking icon does nothing, or app crashes immediately.

**Solutions**:

1. **Check .NET Framework**:
   - Press Win + R, type `appwiz.cpl`, press Enter
   - Look for ".NET Framework 4.8" or later
   - If not installed, download from Microsoft

2. **Run in Compatibility Mode**:
   - Right-click Qash Compass shortcut
   - Properties → Compatibility tab
   - Check "Run this program in compatibility mode for:"
   - Select "Windows 8"
   - Click OK

3. **Check Windows Event Viewer**:
   - Win + X → Event Viewer
   - Windows Logs → Application
   - Look for Qash Compass errors

4. **Reset Configuration**:
   - Navigate to: `%APPDATA%\QashCompass\`
   - Rename `config.json` to `config.json.old`
   - Try launching again

5. **Reinstall**:
   - Uninstall Qash Compass
   - Backup data folder: `%APPDATA%\QashCompass\`
   - Download fresh installer
   - Reinstall

### "Application is already running"

**Symptoms**: Error message says app is already running but you don't see it.

**Solutions**:
1. Open Task Manager (Ctrl + Shift + Esc)
2. Look for "QashCompass.exe" in Processes
3. End the process
4. Try launching again

### Application Crashes on Startup

**Solutions**:
1. Check crash logs:
   - `%APPDATA%\QashCompass\logs\`
   - Open most recent log file
2. Try starting in safe mode:
   - Hold Shift while launching (if supported)
3. Delete cache:
   - `%APPDATA%\QashCompass\cache\`
   - Delete all files in this folder

## Data Issues

### Transactions Not Showing

**Symptoms**: You added transactions but can't see them.

**Solutions**:
1. Check date filter at top of page - expand date range
2. Check account filter - select "All Accounts"
3. Clear search box if you've filtered results
4. Press F5 to refresh the view

### Incorrect Account Balances

**Solutions**:
1. Go to Accounts → Select account → "Recalculate Balance"
2. Check for duplicate transactions:
   - Go to Transactions
   - Sort by date and amount
   - Remove duplicates
3. Verify opening balance is correct
4. Run database check: Settings → Advanced → Database Maintenance → "Verify Integrity"

### Lost Data After Update

**Solutions**:
1. Check if data folder exists: `%APPDATA%\QashCompass\`
2. Look for automatic backups: `%APPDATA%\QashCompass\backups\`
3. Restore from most recent backup:
   - File → Restore Data
   - Select backup file

### Can't Edit or Delete Transactions

**Solutions**:
1. Check if transaction is locked (older than lock period)
2. Settings → Security → Transaction Lock Period
3. Temporarily disable lock to edit

## Performance Issues

### Slow Application Startup

**Solutions**:
1. Optimize database:
   - Settings → Advanced → Database Maintenance
   - Click "Optimize Database"
2. Reduce number of startup items:
   - Settings → General → Uncheck unnecessary startup tasks
3. Check disk space - ensure at least 1GB free

### Slow Transaction Loading

**Solutions**:
1. Limit date range being displayed
2. Optimize database (see above)
3. Archive old transactions (export then delete)
4. Close other running applications

### Application Freezes

**Symptoms**: Application becomes unresponsive.

**Solutions**:
1. Wait - may be processing large dataset
2. If frozen >5 minutes, end process:
   - Task Manager → QashCompass.exe → End Task
3. Restart application
4. Run database repair:
   - Settings → Advanced → Database Maintenance → "Repair Database"

## Display Issues

### Blurry Text

**Solutions**:
1. Right-click QashCompass shortcut → Properties
2. Compatibility tab → "Change high DPI settings"
3. Check "Override high DPI scaling behavior"
4. Select "Application" from dropdown

### UI Elements Cut Off

**Solutions**:
1. Increase screen resolution (minimum 1366x768)
2. Adjust Windows display scaling:
   - Settings → System → Display
   - Try different scaling (100%, 125%, 150%)
3. Maximize application window

### Dark Mode Not Working

**Solutions**:
1. Settings → Display → Theme
2. Restart application after changing theme
3. Check Windows theme settings aren't overriding

## Backup & Restore Issues

### Backup Fails

**Symptoms**: Error when creating backup.

**Solutions**:
1. Check destination folder permissions
2. Ensure sufficient disk space
3. Try different backup location
4. Close other applications accessing data

### Can't Restore Backup

**Symptoms**: Error when restoring from backup file.

**Solutions**:
1. Verify backup file isn't corrupted:
   - Check file size (should be > 0 bytes)
2. Ensure using correct file type (`.qcbackup`)
3. Try older backup file
4. Check if backup was created with newer version

### Automatic Backup Not Working

**Solutions**:
1. Settings → Backup → Verify settings:
   - Automatic backup enabled
   - Valid backup location
   - Correct frequency
2. Check backup logs:
   - `%APPDATA%\QashCompass\logs\backup.log`
3. Ensure application runs long enough for backup to occur

## Import/Export Issues

### Import Fails

**Solutions**:
1. Verify file format is supported (CSV, QIF)
2. Check file encoding (UTF-8 recommended)
3. Ensure required columns are present
4. Check for special characters in data
5. Try importing smaller batches

### Export Incomplete

**Solutions**:
1. Check date range filter before exporting
2. Verify account selection (All Accounts vs. specific)
3. Check category filters
4. Ensure export location is writable

### CSV Import Shows Incorrect Data

**Solutions**:
1. Review field mapping during import
2. Check date format matches expectations
3. Verify decimal separator (period vs. comma)
4. Preview imported data before finalizing

## Error Messages

### "Database is locked"

**Cause**: Another instance accessing the database or previous crash.

**Solutions**:
1. Close all Qash Compass windows
2. Task Manager → End QashCompass.exe processes
3. Restart application
4. If persists, restart computer

### "Database is corrupted"

**Cause**: Unexpected shutdown, disk errors, or software bug.

**Solutions**:
1. Settings → Advanced → Database Maintenance → "Repair Database"
2. If repair fails, restore from backup:
   - File → Restore Data
   - Select most recent backup
3. If no backup available, contact support

### "Insufficient permissions"

**Cause**: Windows user account doesn't have necessary permissions.

**Solutions**:
1. Run Qash Compass as administrator (once):
   - Right-click → "Run as administrator"
2. Check folder permissions:
   - `%APPDATA%\QashCompass\`
   - Ensure your user has read/write access
3. Reinstall application

### "Failed to save transaction"

**Solutions**:
1. Check disk space
2. Verify database isn't read-only:
   - `%APPDATA%\QashCompass\data.db`
   - Right-click → Properties → Uncheck "Read-only"
3. Run database repair
4. Try restarting application

## Advanced Troubleshooting

### Collecting Diagnostic Information

When reporting issues, include:

1. **Application Version**:
   - Help → About Qash Compass

2. **Windows Version**:
   - Win + R → `winver`

3. **Error Logs**:
   - `%APPDATA%\QashCompass\logs\`
   - Include most recent log files

4. **Database Size**:
   - `%APPDATA%\QashCompass\data.db`
   - Right-click → Properties → Size

5. **Screenshots**:
   - Of error messages
   - Of unexpected behavior

### Clean Install

If all else fails:

1. **Backup Data**:
   - File → Backup Data
   - Save to safe location

2. **Uninstall**:
   - Settings → Apps → Qash Compass → Uninstall

3. **Remove Residual Files**:
   - Delete: `%APPDATA%\QashCompass\`
   - Delete: `C:\Program Files\Qash Compass\` (if exists)

4. **Restart Computer**

5. **Reinstall**:
   - Download latest installer
   - Install fresh

6. **Restore Data**:
   - File → Restore Data
   - Select backup file

### Database Maintenance Commands

For advanced users:

1. **Vacuum** (reclaim space):
   - Settings → Advanced → Database Maintenance → "Vacuum Database"

2. **Reindex** (rebuild indexes):
   - Settings → Advanced → Database Maintenance → "Rebuild Indexes"

3. **Integrity Check**:
   - Settings → Advanced → Database Maintenance → "Verify Integrity"

## Getting Help

If you've tried everything and still have issues:

1. **Search Existing Issues**:
   - [GitHub Issues](https://github.com/Nze-Jerry/Qash-Compass/issues)
   - Someone may have solved your problem

2. **Create New Issue**:
   - Include diagnostic information
   - Describe steps to reproduce
   - Attach logs and screenshots
   - Mention what you've already tried

3. **Community Support**:
   - [GitHub Discussions](https://github.com/Nze-Jerry/Qash-Compass/discussions)
   - Other users may help

## Emergency Data Recovery

If you can't access your data:

1. Data location: `%APPDATA%\QashCompass\`
2. Database file: `data.db`
3. Backup files: `backups\*.qcbackup`
4. Copy these files to safe location
5. Contact support with details

---

**Note**: Most issues can be resolved with a database repair or restoration from backup. Always keep regular backups of your financial data!
