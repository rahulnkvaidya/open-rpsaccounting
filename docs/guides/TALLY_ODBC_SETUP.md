# Tally ODBC Setup Guide

## Tally ODBC Driver Installation Hindi/English Guide

### Prerequisites

**RPS Accounting Requirements:**
- Python 3.7 or later
- pyodbc package (automatically installed with RPS Accounting)

**Tally Requirements:**
- Tally.ERP 9 or later
- Tally ODBC Driver

---

## Step 1: Tally ODBC Driver Install Karen

### Download Kahan Se Karen:

**Official Tally Website:**
1. Visit: https://tallysolutions.com/download/
2. Find "Tally ODBC Driver" section
3. Click "Download"

**Direct Link:**
- https://tallysolutions.com/download/odbc-driver/

### Installation Steps:

1. **Installer Run Karen**
   - Downloaded file par double-click karen
   - "TallyODBCDriver.exe" run hoga

2. **Installation Wizard Follow Karen**
   - "Next" click karen
   - License agreement accept karen
   - Installation path select karen (default recommended)
   - "Install" click karen

3. **Complete Installation**
   - "Finish" click karen
   - Computer restart karen (recommended)

---

## Step 2: Verify Installation

### Windows ODBC Data Sources Check Karen:

1. **Open ODBC Manager:**
   - Press `Win + R`
   - Type: `odbcad32`
   - Press Enter

2. **Check Driver:**
   - "Drivers" tab pe jaayein
   - List mein "Tally ODBC Driver" dhundhen
   - Agar dikhe toh installation successful hai ✓

### Alternative Check (CMD):

```cmd
odbcconf /q /a {REGSVR "C:\Program Files (x86)\Tally Solutions\Tally ODBC Driver\TallyODBC.dll"}
```

---

## Step 3: Tally Configuration

### Tally Server Mode Enable Karen:

1. **Tally Open Karen**
2. **Gateway of Tally se:**
   - F12 (Configure) press karen
   - "Advanced Configuration" select karen

3. **ODBC Server Enable Karen:**
   - "Enable ODBC Server" option dhundhen
   - "Yes" select karen
   - Port number: `9000` (default)

4. **Save and Restart:**
   - Accept karen
   - Tally ko restart karen

---

## Step 4: Test Connection

### RPS Accounting se Test Karen:

```bash
cd e:\Documents\RPS Accounting
python
```

```python
from core.tally_odbc import check_tally_odbc_driver, list_tally_companies

# Check driver
print(check_tally_odbc_driver())  # Should print: True

# List companies
companies = list_tally_companies()
print(companies)  # Should show your Tally companies
```

---

## Troubleshooting

### Problem 1: Driver Not Found

**Error:**
```
Tally ODBC driver not found
```

**Solution:**
1. Verify installation kiya hai
2. ODBC Data Sources mein check karen
3. Driver ko reinstall karen

### Problem 2: Cannot Connect to Company

**Error:**
```
Failed to connect to Tally: [HY000]
```

**Solution:**
1. Tally company open hai?
2. ODBC server enabled hai?
3. Port 9000 available hai?
4. Firewall blocking toh nahi?

### Problem 3: Company Not Listed

**Error:**
```
No Tally companies found
```

**Solution:**
1. Tally data directory check karen
2. Default path: `C:\Tally.ERP9\Data\`
3. Companies exist karti hain?
4. Folder permissions check karen

### Problem 4: Access Denied

**Error:**
```
[Microsoft][ODBC Driver Manager] Access denied
```

**Solution:**
1. RPS Accounting ko Administrator mode mein run karen
2. Tally company password protected toh nahi?
3. File permissions check karen

---

## Advanced Configuration

### Custom Tally Data Location:

Agar aapka Tally data custom location mein hai:

```python
from core.tally_odbc import list_tally_companies

companies = list_tally_companies(r"D:\MyTallyData")
```

### Multiple Tally Installations:

Agar multiple Tally versions installed hain:

1. Sabse latest version ka ODBC driver use karen
2. Specific version ka driver path:
   - Tally 7.2: `C:\Program Files\Tally72\`
   - Tally 9: `C:\Program Files\Tally9\`
   - Tally.ERP 9: `C:\Program Files (x86)\Tally.ERP9\`

---

## System Requirements

### Minimum Requirements:

- **OS:** Windows 7 or later
- **Tally:** Version 7.2 or later
- **RAM:** 2 GB
- **Disk Space:** 100 MB free

### Recommended:

- **OS:** Windows 10/11
- **Tally:** Tally.ERP 9 (latest)
- **RAM:** 4 GB or more
- **Disk Space:** 500 MB free

---

## Security Notes

> [!IMPORTANT]
> **Password Protected Companies:**
> - Agar Tally company password protected hai
> - Connection time password enter karna hoga
> - Currently automatic password not supported

> [!WARNING]
> **Data Safety:**
> - Migration se pehle backup zaroor len
> - Read-only access - data change nahi hoga
> - Tally mein kuch modify nahi hoga

---

## Support

### RPS Accounting Support:
- Email: support@RPS Accounting.com
- Phone: 1800-XXX-XXXX

### Tally ODBC Support:
- Help: https://help.tallysolutions.com/
- Community: https://tallysolutions.com/community/

---

## Quick Reference

### Installation Checklist

- [ ] Download Tally ODBC Driver
- [ ] Install driver
- [ ] Verify in ODBC Data Sources
- [ ] Enable ODBC server in Tally
- [ ] Test connection from RPS Accounting
- [ ] List Tally companies successfully

### Connection Settings

| Setting | Value |
|---------|-------|
| Server | localhost |
| Port | 9000 |
| Driver | Tally ODBC Driver |

---

**Last Updated:** February 2026
**Version:** 1.0
