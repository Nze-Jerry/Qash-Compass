# Assets Directory

This directory contains visual assets for the Qash Compass documentation and distribution materials.

## Directory Structure

```
assets/
├── screenshots/     # Application screenshots for documentation
├── icons/          # Application icons and logos
└── guides/         # Visual guides and tutorials
```

## Screenshots

When adding screenshots:

1. **Resolution**: Minimum 1366x768, preferably 1920x1080
2. **Format**: PNG for UI screenshots, JPEG for photos
3. **File Naming**: Use descriptive names (e.g., `dashboard-overview.png`, `add-transaction-dialog.png`)
4. **Privacy**: Ensure no real financial data is visible
5. **Content**: Show relevant features clearly

## Recommended Screenshots

Consider adding:

- Dashboard overview
- Transaction list
- Add transaction dialog
- Budget management screen
- Reports and charts
- Settings panels
- Account management
- Import/export dialogs

## Icons

Application icons and branding materials:

- App icon (various sizes: 16x16, 32x32, 48x48, 256x256)
- Taskbar icon
- Installer icon
- File association icons

## Usage in Documentation

Reference screenshots in documentation using relative paths:

```markdown
![Dashboard Overview](../assets/screenshots/dashboard-overview.png)
```

## Guidelines

- Keep file sizes reasonable (compress large images)
- Use consistent styling and theme (light/dark mode)
- Update screenshots when UI changes significantly
- Include alt text for accessibility

## Contributing

When contributing screenshots:

1. Ensure they follow the guidelines above
2. Add them to the appropriate subdirectory
3. Update documentation to reference new screenshots
4. Include in pull request description what the screenshots show
