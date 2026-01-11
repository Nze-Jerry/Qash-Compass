# Frequently Asked Questions (FAQ)

## General Questions

### What is Qash Compass?

Qash Compass is an offline desktop application for Windows that helps you manage your personal finances. It allows you to track income, expenses, budgets, and financial goals without requiring an internet connection.

### Is Qash Compass free?

Please check the current pricing and licensing information on the official website or in the release notes.

### What platforms does Qash Compass support?

Currently, Qash Compass is available exclusively for Windows 10 and Windows 11 (64-bit).

### Is my data safe?

Yes! Your financial data is stored only on your computer. Qash Compass doesn't send any data to external servers or require an internet connection. You can also enable optional encryption for additional security.

## Installation & Setup

### Do I need an internet connection?

No internet connection is required to use Qash Compass. You only need internet to download the installer initially.

### Can I install Qash Compass on multiple computers?

Yes, you can install Qash Compass on multiple computers. However, your data is stored locally on each machine and won't automatically sync between them.

### How do I transfer my data to another computer?

1. On the old computer: File → Backup Data
2. Copy the `.qcbackup` file to the new computer
3. On the new computer: File → Restore Data
4. Select the backup file

### What are the system requirements?

- Windows 10 (64-bit) or Windows 11
- 4 GB RAM (8 GB recommended)
- 500 MB disk space
- 1366x768 screen resolution or higher

## Using Qash Compass

### How do I add a transaction?

Click the "+ Add Transaction" button, select Income or Expense, fill in the details (amount, category, date), and click Save.

### Can I attach receipts to transactions?

Yes! When adding an expense, click "Attach Receipt" and select an image file from your computer.

### How do I create a budget?

Go to Budgets → "+ New Budget", select a category or overall budget type, enter the amount and period, then click "Create Budget".

### Can I track multiple bank accounts?

Yes! You can add unlimited accounts of different types (checking, savings, credit cards, cash, investments).

### How do I categorize transactions?

When adding a transaction, select a category from the dropdown menu. You can customize categories in Settings → Categories.

### Can I set up recurring transactions?

Yes! When adding income or expense, check the "Recurring" option and set the frequency (weekly, monthly, etc.).

### How do I view my spending trends?

Go to the Reports section and select "Spending by Category" or "Income vs. Expenses" to see visual charts and trends.

## Data & Security

### Where is my data stored?

Your data is stored locally at:
`C:\Users\[YourUsername]\AppData\Roaming\QashCompass\`

### Can I encrypt my data?

Yes! You can enable encryption in Settings → Security. You'll need to set a password that you must remember - lost passwords cannot be recovered.

### How do I backup my data?

**Manual**: File → Backup Data → Choose location → Save

**Automatic**: Settings → Backup → Enable "Automatic Backup" → Set frequency

### How often should I backup?

We recommend backing up at least once a week, or more frequently if you make many transactions.

### Can I recover a lost password?

No. If you enable encryption and forget your password, your data cannot be recovered. Store your password securely!

### Is my data sent anywhere online?

No. Qash Compass is completely offline. Your data never leaves your computer.

## Features

### Can I use multiple currencies?

Yes! You can set a default currency and assign different currencies to individual accounts or transactions.

### Can I import data from other apps?

Yes! Qash Compass supports importing from:
- CSV files
- Quicken (QIF format)
- Microsoft Money

Go to File → Import to get started.

### Can I export my data?

Yes! You can export to CSV or Excel formats. Go to File → Export and choose your desired format.

### Does Qash Compass have mobile apps?

Currently, Qash Compass is desktop-only for Windows. Mobile apps may be considered for future releases.

### Can I generate reports?

Yes! The Reports section offers various reports:
- Income vs. Expenses
- Spending by Category
- Net Worth Trend
- Cash Flow
- Budget Performance

All reports can be exported to PDF, CSV, or Excel.

## Troubleshooting

### The application won't launch

- Ensure .NET Framework 4.8 or later is installed
- Try running in compatibility mode (Windows 8)
- Check Windows Event Viewer for error messages
- Reinstall the application

### I can't see all my transactions

- Check the date filter at the top of the page
- Ensure the correct account is selected
- Use the search function to find specific transactions

### My budgets aren't updating

- Ensure transactions are properly categorized
- Check that the budget period is current
- Refresh the budget view (F5)

### Backup/Restore isn't working

- Ensure you have write permissions to the backup location
- Check that you're using a valid `.qcbackup` file
- Make sure you have enough disk space

### The database is corrupted

1. Go to Settings → Advanced → Database Maintenance
2. Click "Repair Database"
3. If that doesn't work, restore from a recent backup

### How do I reset the application?

Settings → Advanced → Reset Application

**Warning**: This resets settings but preserves your data. To completely remove all data, uninstall the application and delete the data folder manually.

## Updates & Support

### How do I update Qash Compass?

1. Download the latest installer from the Releases page
2. Run the installer (your data will be preserved)
3. Follow the installation wizard

### Will updates delete my data?

No. Your data is preserved when updating to newer versions.

### Where can I report bugs?

Report bugs on our [GitHub Issues page](https://github.com/Nze-Jerry/Qash-Compass/issues).

### How do I request features?

Create a feature request on [GitHub Issues](https://github.com/Nze-Jerry/Qash-Compass/issues) with the "enhancement" label.

### Is there a user community?

Yes! Visit [GitHub Discussions](https://github.com/Nze-Jerry/Qash-Compass/discussions) to connect with other users.

### How can I get support?

1. Check this FAQ
2. Review the [User Guide](USER_GUIDE.md)
3. Check the [Troubleshooting Guide](TROUBLESHOOTING.md)
4. Search [existing issues](https://github.com/Nze-Jerry/Qash-Compass/issues)
5. Create a new issue with details

## Performance

### How much data can Qash Compass handle?

Qash Compass can handle thousands of transactions efficiently. Database optimization tools are available in Settings → Advanced.

### The application is running slowly

1. Go to Settings → Advanced → Database Maintenance
2. Click "Optimize Database"
3. Close and restart the application
4. Consider archiving old transactions

### How do I archive old transactions?

Currently, transactions remain in the database. You can filter by date range in reports to focus on recent data.

## Privacy

### Does Qash Compass collect any data?

No. Qash Compass does not collect, transmit, or store any user data externally. Everything stays on your computer.

### Does it require any permissions?

Only standard file system permissions to read/write data to the local application folder.

### Can I use Qash Compass for business?

Qash Compass is designed for personal finance. For business accounting, consider dedicated business accounting software.

---

## Still have questions?

If your question isn't answered here:

- Check the [User Guide](USER_GUIDE.md) for detailed instructions
- Visit [GitHub Discussions](https://github.com/Nze-Jerry/Qash-Compass/discussions)
- Create an issue on [GitHub](https://github.com/Nze-Jerry/Qash-Compass/issues)
