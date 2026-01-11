# Security Policy

## Reporting a Vulnerability

The security of Qash Compass and user data is our top priority. We appreciate your efforts to responsibly disclose your findings.

### How to Report

If you discover a security vulnerability, please **DO NOT** create a public GitHub issue.

Instead, please report it privately by:

1. **GitHub Security Advisory**: Use the [Security tab](https://github.com/Nze-Jerry/Qash-Compass/security/advisories/new) to create a private security advisory
2. **GitHub Issues**: For less critical security concerns, you may create a private issue

### What to Include

Please include the following in your report:

- **Description** of the vulnerability
- **Steps to reproduce** the issue
- **Potential impact** of the vulnerability
- **Affected versions** (if known)
- **Suggested fix** (if you have one)
- **Your contact information** for follow-up

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Fix Timeline**: Varies by severity (critical issues within 30 days)

### Disclosure Policy

- Please allow us reasonable time to fix the issue before public disclosure
- We will credit security researchers who responsibly disclose vulnerabilities (unless you prefer to remain anonymous)
- We will coordinate disclosure timing with you

## Security Best Practices for Users

### Data Security

1. **Enable Encryption**: Settings → Security → Enable Data Encryption
2. **Use Strong Password**: If encryption is enabled, use a strong, unique password
3. **Regular Backups**: Keep encrypted backups in a secure location
4. **Keep Updated**: Always use the latest version

### System Security

1. **Official Sources Only**: Download Qash Compass only from official sources:
   - [GitHub Releases](https://github.com/Nze-Jerry/Qash-Compass/releases)
   - Official website (if available)

2. **Verify Downloads**: Check file hashes provided in release notes

3. **Administrator Rights**: Only run installer as administrator, not the application itself

4. **Antivirus**: Keep your antivirus software up to date

### Privacy Protection

1. **Offline-First**: Qash Compass works completely offline
2. **No Telemetry**: No usage data is collected or transmitted
3. **Local Storage**: All data stays on your computer
4. **Screen Sharing**: Be cautious when sharing your screen with financial data visible

## Known Security Considerations

### Application Security

- **Local Data Storage**: Data is stored locally in `%APPDATA%\QashCompass\`
- **Optional Encryption**: Users can enable encryption for data at rest
- **No Network Access**: Application does not make network connections
- **Windows Authentication**: Relies on Windows user account security

### User Responsibilities

- **Physical Security**: Secure your computer with a password/PIN
- **Backup Security**: Store backups in secure locations
- **Password Management**: Remember encryption passwords (cannot be recovered)
- **Screen Lock**: Use Windows screen lock when away from computer

## Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Security Features

Qash Compass includes the following security features:

- **AES-256 Encryption**: Optional encryption for database
- **Local-Only Storage**: No cloud or network transmission
- **No Telemetry**: No data collection or tracking
- **Secure Deletion**: Proper data deletion when removing items
- **Session Timeout**: Optional auto-lock after inactivity

## Out of Scope

The following are generally considered out of scope:

- Issues requiring physical access to an unlocked computer
- Social engineering attacks
- Issues in third-party dependencies (please report to the respective projects)
- Vulnerabilities in outdated versions

## Legal

- We do not support or condone security research that violates laws
- Testing should only be performed on your own installation
- Do not access other users' data without permission

## Recognition

We maintain a security hall of fame to recognize security researchers who help make Qash Compass more secure. If you wish to be listed (or remain anonymous), please let us know in your report.

---

Thank you for helping keep Qash Compass and our users safe!
