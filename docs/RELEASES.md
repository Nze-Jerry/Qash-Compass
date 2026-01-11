# Releases

This document provides information about Qash Compass releases and how to download them.

## Latest Release

Check the [Releases page](https://github.com/Nze-Jerry/Qash-Compass/releases) for the latest version.

## Release Channels

### Stable
- **Recommended for most users**
- Fully tested and production-ready
- Released when new features are stable
- Version format: `X.Y.Z` (e.g., 1.0.0)

### Pre-release (Beta)
- For early adopters and testers
- May contain bugs or incomplete features
- Help us test new features
- Version format: `X.Y.Z-beta.N` (e.g., 1.1.0-beta.1)

## Download

### Current Stable Release: v1.0.0

**Windows 10/11 (64-bit)**
- [Download QashCompass-Setup.exe](https://github.com/Nze-Jerry/Qash-Compass/releases/latest)
- File size: ~50 MB
- SHA256: (will be provided in actual release)

### What's Included

- Windows installer (.exe)
- Release notes
- SHA256 checksums
- Digital signature (future releases)

## Verify Downloads

To ensure your download is authentic:

1. Compare file size with the one listed in release notes
2. Verify SHA256 checksum:
   ```cmd
   certutil -hashfile QashCompass-Setup.exe SHA256
   ```
3. Compare output with checksum in release notes

## Installation

See the [Installation Guide](docs/INSTALLATION.md) for detailed instructions.

## Release Notes

### Version 1.0.0 (2026-01-11)

**Initial Release**

Features:
- Offline personal finance management
- Budget tracking and management
- Expense categorization and tracking
- Income recording
- Financial reports and visualizations
- Multi-currency support
- Data export to CSV/Excel
- Local data storage with optional encryption

System Requirements:
- Windows 10 (64-bit) or Windows 11
- 4 GB RAM minimum
- 500 MB disk space

Known Issues:
- None

## Upgrade Guide

### From Previous Versions

Currently version 1.0.0 is the first release. Future updates will preserve your data automatically.

**Upgrade Steps** (for future releases):
1. Backup your data: File → Backup Data
2. Download new installer
3. Run installer (your data will be preserved)
4. Launch updated application

## Release Schedule

We aim to release updates on the following schedule:

- **Major versions** (X.0.0): Annually or as needed
- **Minor versions** (1.X.0): Quarterly (new features)
- **Patch versions** (1.0.X): As needed (bug fixes)

## Beta Program

Interested in testing pre-release versions?

1. Watch this repository for release announcements
2. Download beta versions from the Releases page
3. Report issues on GitHub
4. Provide feedback in Discussions

**Note**: Beta versions should not be used for production financial data. Always backup before testing beta versions.

## Archive

All previous releases are available on the [Releases page](https://github.com/Nze-Jerry/Qash-Compass/releases).

## Support

For issues with specific releases:
- Check [Troubleshooting Guide](docs/TROUBLESHOOTING.md)
- Review [FAQ](docs/FAQ.md)
- Create an [issue](https://github.com/Nze-Jerry/Qash-Compass/issues) with your version number

## Changelog

Detailed changes for each version: [CHANGELOG.md](CHANGELOG.md)

---

**Note**: This is a distribution repository for pre-built binaries. The source code is proprietary and not available in this repository.
