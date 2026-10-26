# Test Environment Setup Guide

## Application Access

### Application Details

**Application Name:** ParaBank Demo Banking Application  
**Application URL:** https://parabank.parasoft.com/parabank/index.htm  
**Application Type:** Web-based Banking Demo  
**Application Owner:** Parasoft  
**Access Level:** Public (no special access required)  
**Authentication:** Required (use test credentials)

### Important Notes

⚠️ This is a **DEMO/TEST application only**  
⚠️ Not a real bank  
⚠️ Do not use real personal information  
⚠️ Database may reset periodically

---

## Hardware Requirements

### Minimum Requirements
- **CPU:** Intel Core i5 / AMD Ryzen 5 equivalent
- **RAM:** 4 GB minimum
- **Storage:** 500 MB free space (for logs and evidence)
- **Network:** Stable internet connection (1 Mbps minimum)
- **Peripherals:** Mouse, keyboard, monitor

### Recommended Setup
- **CPU:** Intel Core i7 / AMD Ryzen 7 or better
- **RAM:** 8 GB or more
- **Storage:** 1+ GB SSD space
- **Network:** High-speed connection (10+ Mbps)
- **Monitor:** 1920x1080 or higher resolution

---

## Software Requirements

### Operating System
- **Windows:** Windows 10, Windows 11
- **macOS:** macOS 10.15 (Catalina) or later
- **Linux:** Ubuntu 20.04 LTS or later

### Web Browser

**Primary Browser:** Google Chrome
- Version: 90 or later
- Download: https://www.google.com/chrome/

**Secondary Browser:** Mozilla Firefox
- Version: 88 or later
- Download: https://www.mozilla.org/firefox/

**Optional Browser:** Apple Safari
- Version: 14 or later
- Available on macOS only

### Required Applications
- **Spreadsheet Software:** Microsoft Excel or LibreOffice Calc
  - For viewing/editing test cases
  - Version: Latest or recent (Excel 2016+, LibreOffice 7.0+)

- **Text Editor:** Any text editor
  - For viewing/editing CSV and markdown files
  - Examples: Notepad++, VS Code, Sublime Text

### Optional Tools
- **Screenshot Tool:** SnagIt, Greenshot, or built-in OS tool
- **Screen Recorder:** OBS Studio or built-in screen capture
- **Browser Developer Tools:** Built-in (F12 in most browsers)

---

## Browser Configuration

### Chrome Setup

1. **Clear Cache & Cookies:**
   - Press `Ctrl + Shift + Delete` (Windows) or `Cmd + Shift + Delete` (Mac)
   - Select "All time"
   - Check "Cookies and other site data"
   - Click "Clear data"

2. **Enable JavaScript:**
   - Open Chrome Settings → Privacy and security → Site Settings
   - Verify JavaScript is enabled

3. **Allow Pop-ups:**
   - Settings → Privacy and security → Site Settings → Pop-ups and redirects
   - Add parabank.parasoft.com to allowed list

4. **Disable Extensions (optional):**
   - Settings → Extensions
   - Toggle off ad blockers for this site

### Firefox Setup

1. **Clear History:**
   - Press `Ctrl + Shift + Delete`
   - Select "Everything"
   - Click "Clear Now"

2. **Enable JavaScript:**
   - About → Preferences → Privacy & Security
   - Verify JavaScript is enabled (default)

3. **Allow Pop-ups:**
   - Preferences → Privacy & Security → Permissions
   - Add site to exceptions

---

## Network Requirements

### Internet Connection
- **Speed:** Minimum 1 Mbps, Recommended 10+ Mbps
- **Stability:** Consistent connection (no frequent dropouts)
- **Latency:** < 200ms preferred
- **Bandwidth:** Minimum 5 GB/month per 8-hour test session

### Firewall & Proxy
- Ensure parabank.parasoft.com is not blocked
- Configure proxy settings if needed
- Whitelist domain: `*.parasoft.com`

---

## Test Data Setup

### Required Files
- **Location:** `test-data/Test_Data.csv`
- **Format:** Comma-separated values
- **Contains:** Test credentials and data

### Test Credentials

Use credentials from `test-data/Test_Data.csv` for testing:

**Example:**
```
Username: testuser1
Password: password123
```

⚠️ **Important:**
- These are demo-only credentials
- Not real user accounts
- Database may reset periodically
- Do not reuse credentials for other purposes

---

## Environment Checklist

Before starting test execution, verify:

### Connectivity
- [ ] Internet connection is stable
- [ ] Can access external websites
- [ ] parabank.parasoft.com is accessible

### Browser
- [ ] Chrome/Firefox installed and updated
- [ ] Cache and cookies cleared
- [ ] Pop-ups enabled for the site
- [ ] JavaScript enabled
- [ ] No blocking extensions active

### Applications
- [ ] Spreadsheet application available
- [ ] Text editor available
- [ ] Screenshot tool ready
- [ ] File explorer/manager ready

### Test Data
- [ ] Test_Data.csv file accessible
- [ ] Test credentials verified
- [ ] Test cases (Excel/CSV) opened and reviewed
- [ ] Execution_Log.csv template ready

### Documentation
- [ ] Test_Plan.md reviewed
- [ ] Test_Scenarios.md understood
- [ ] Test_Environment.md (this file) read
- [ ] Test cases reviewed and understood

### Working Directory
- [ ] Project folder on desktop or easily accessible
- [ ] Subfolders created (if needed):
  - `evidence/screenshots/`
  - `execution/logs/`
  - `defects/images/`

### Performance
- [ ] System resources sufficient (>50% RAM available)
- [ ] No background heavy processes
- [ ] Computer not in power-saving mode
- [ ] Display timeout set to 30+ minutes

---

## Resetting Environment Between Sessions

### Quick Reset (5 minutes)

1. **Clear Browser:**
   ```
   Chrome: Ctrl + Shift + Delete → Clear data
   Firefox: Ctrl + Shift + Delete → Clear Now
   ```

2. **Close Browser:**
   - Completely close the browser

3. **Clear OS Cache:**
   - Windows: Empty Recycle Bin
   - macOS: Empty Trash

4. **Restart Browser:**
   - Open new browser window
   - Navigate to ParaBank

### Full Reset (15 minutes)

1. Perform Quick Reset (above)
2. Clear browser password suggestions:
   - Chrome: Settings → Passwords and autofill
   - Disable "Offer to save passwords"
3. Clear downloaded files cache
4. Verify fresh login page loads
5. Test with new credentials from test-data/Test_Data.csv

---

## Troubleshooting

### "Site Cannot Be Reached"
- [ ] Check internet connection
- [ ] Verify URL is correct: https://parabank.parasoft.com/parabank/index.htm
- [ ] Check if firewall is blocking the site
- [ ] Try different browser
- [ ] Wait a few minutes (server might be temporarily down)

### "Page Takes Too Long to Load"
- [ ] Check internet speed (run speedtest.net)
- [ ] Try another browser
- [ ] Clear browser cache completely
- [ ] Try during off-peak hours
- [ ] Check system resources (Resource Monitor)

### "JavaScript Not Working"
- [ ] Verify JavaScript is enabled in browser settings
- [ ] Disable browser extensions
- [ ] Clear cookies for the site
- [ ] Try in Incognito/Private mode

### "Cannot Login with Test Credentials"
- [ ] Verify credentials from test-data/Test_Data.csv
- [ ] Check if database has been reset
- [ ] Try creating new account via Registration
- [ ] Clear browser cookies for the site
- [ ] Check for error messages on login page

### "Evidence Screenshots Not Saving"
- [ ] Verify save location has write permissions
- [ ] Check available disk space
- [ ] Use different screenshot tool
- [ ] Verify folder path exists

---

## Environment Sign-off

**Tester Name:** ___________________  
**Date:** ___________________  
**Time:** ___________________  

### Verification
- [ ] All checklist items verified
- [ ] Application URL accessible
- [ ] Test credentials working
- [ ] Test cases opened and understood
- [ ] Logging tools ready
- [ ] No blocking issues identified

**Signature:** ___________________  
**Environment Status:** ☐ Ready to Test / ☐ Issues Found

---

**Last Updated:** 2026-09-11  
**Version:** 1.0  
**Status:** Active
