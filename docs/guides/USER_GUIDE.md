# Payroll System - Complete User Guide

## 📋 Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Employee Management](#employee-management)
4. [Payroll Processing](#payroll-processing)
5. [Leave Management](#leave-management)
6. [Attendance Management](#attendance-management)
7. [Reports](#reports)
8. [Tax Management](#tax-management)
9. [Year-End Processing](#year-end-processing)
10. [Employee Self-Service Portal](#employee-self-service-portal)
11. [Advanced Features](#advanced-features)

---

## Introduction

### What is the Payroll System?

The RPS Accounting Payroll System is a comprehensive, enterprise-grade solution for managing employee payroll, leave, attendance, and tax compliance. It's designed specifically for Indian businesses with full support for:

- Indian tax laws (FY 2025-26)
- Form 16 generation
- Professional Tax
- PF, ESI, and other statutory deductions
- Leave carry-forward as per Indian labor laws

### Key Features

✅ **Employee Management** - Complete employee lifecycle management  
✅ **Automated Payroll** - Bulk processing with voucher integration  
✅ **Salary Slips** - PDF generation with password protection  
✅ **Leave Management** - Accrual, approval, tracking, carry-forward  
✅ **Attendance Import** - Excel, CSV, biometric device support  
✅ **Tax Compliance** - TDS calculation, Form 16 generation  
✅ **Reports** - 10+ comprehensive reports  
✅ **Employee Portal** - Self-service access for employees  
✅ **Email/WhatsApp** - Automated salary slip distribution  

---

## Getting Started

### Installation & Setup

1. **Install Python** (3.8 or higher)
   ```bash
   python --version
   ```

2. **Install Required Libraries**
   ```bash
   pip install customtkinter pandas weasyprint PyPDF2
   ```

3. **Launch Application**
   ```bash
   cd E:\Documents\RPS Accounting
   python main.py
   ```

### First-Time Setup

#### Step 1: Configure Company Details
1. Go to **Settings → Company Settings**
2. Enter:
   - Company Name
   - Address
   - PAN, TAN (for tax compliance)
   - Upload company logo
3. Click **Save**

#### Step 2: Configure Email (for salary slip sharing)
1. Go to **Settings → Email Configuration**
2. Enter SMTP details:
   - **Gmail**: smtp.gmail.com, Port 587
   - **Outlook**: smtp.office365.com, Port 587
3. Enable "App Password" for Gmail users
4. Click **Test Email** to verify
5. Click **Save**

#### Step 3: Add Employees
See [Employee Management](#employee-management) section below.

---

## Employee Management

### Adding a New Employee

**Step-by-Step:**

1. Click **👤 Manage Employees** button
2. Click **Add Employee**
3. Fill in the form:

**Basic Details:**
- Employee ID (unique identifier)
- Name
- Email (for salary slips)
- Phone (for WhatsApp)
- Designation
- Department
- Date of Joining

**Salary Details:**
- Basic Salary
- HRA (House Rent Allowance)
- Other Allowances

**Statutory Details:**
- PAN (for tax calculation)
- UAN (Universal Account Number for PF)
- Bank Account Details

4. Click **Save**

### Adding Allowances & Deductions

**For Individual Employee:**

1. Select employee from list
2. Click **View Details**
3. **Allowances Tab:**
   - Click **Add Allowance**
   - Enter: Name, Amount, Type (Fixed/Percentage)
   - Click **Save**

4. **Deductions Tab:**
   - Click **Add Deduction**
   - Enter: Name, Amount, Type
   - Common deductions: PF, ESI, Professional Tax, Loans
   - Click **Save**

**Using Templates (Bulk):**

1. Click **📋 Templates** button
2. Click **Create Template**
3. Enter template name (e.g., "Standard Allowances")
4. Add allowances/deductions
5. Click **Save Template**
6. To apply: Select template → Choose employees → Click **Apply**

### Editing Employee Details

1. Go to **Manage Employees**
2. Select employee
3. Click **Edit**
4. Modify details
5. Click **Update**

### Deactivating Employees

When an employee leaves:

1. Select employee
2. Click **Deactivate Employee**
3. Confirm action

**Note:** Historical data is preserved. Employee won't appear in future payroll processing.

---

## Payroll Processing

### Monthly Payroll Processing (Recommended Method)

**Step-by-Step:**

1. **Prepare Data** (before processing):
   - Import attendance for the month
   - Approve all leave requests
   - Update any salary changes

2. **Process Payroll:**
   - Click **📄 Bulk Process Payroll**
   - Select **Month** (e.g., January)
   - Select **Year** (e.g., 2026)
   - Review employee list
   - Click **Process All**

3. **System Automatically:**
   - Calculates gross salary
   - Applies allowances
   - Calculates deductions (PF, TDS, PT)
   - Computes net salary
   - Creates accounting vouchers
   - Generates salary slips

4. **Review:**
   - Check **Payroll Reports** for accuracy
   - Verify total payroll amount
   - Review individual salary slips

### Processing Individual Employee

For mid-month joiners or corrections:

1. Click **💰 Process Payroll**
2. Select employee
3. Select month and year
4. Enter days worked (if partial month)
5. Click **Process**

### Reprocessing Payroll

If you need to reprocess:

1. System will warn: "Payroll already exists"
2. Click **Yes** to confirm
3. Existing records will be updated
4. Vouchers will be regenerated

**⚠️ Warning:** Reprocessing affects accounting vouchers. Coordinate with accounts team.

---

## Leave Management

### Setting Up Leave Balances

**For New Employees:**

1. Click **🏖️ Leave Management**
2. Click **Set Opening Balances**
3. Select:
   - Employee
   - Year (e.g., 2026)
   - Leave Type (Earned Leave, Sick Leave, etc.)
4. Enter opening balance
5. Click **Save**

**Typical Opening Balances:**
- Earned Leave: 15 days
- Sick Leave: 7 days
- Casual Leave: 7 days

### Monthly Leave Accrual

System automatically accrues leave monthly:
- Earned Leave: 1.25 days/month (15 days/year)
- Configure in database if different policy

### Processing Leave Requests

**Admin Approval:**

1. Go to **Leave Management**
2. Click **Pending Approvals** tab
3. Review request details:
   - Employee name
   - Leave type
   - From/To dates
   - Number of days
   - Reason
4. Click **Approve** or **Reject**
5. Add remarks (optional)
6. Click **Submit**

**Employee Self-Application:**

Employees can apply through **Employee Portal** (see section below).

### Leave Reports

**Employee Leave Balance Report:**

1. Click **📊 Leave Balance Reports**
2. Go to **Leave Balances** tab
3. Select year
4. Click **Load Balances**
5. View all employees' current balances
6. Export to Excel if needed

**Leave Usage Report:**

1. Go to **Leave Usage Report** tab
2. Select date range
3. Click **Generate Report**
4. See month-wise leave consumption

---

## Attendance Management

### Importing Attendance from Excel/CSV

**Step-by-Step:**

1. **Prepare Your File:**

Example Excel format:
```
Employee ID | Date       | Status
101         | 01/01/2026 | Present
101         | 02/01/2026 | Absent
102         | 01/01/2026 | Present
```

Supported status values:
- Present, P, 1
- Absent, A, 0
- Half Day, HD, 0.5
- Leave, L

2. **Import Process:**
   - Click **📥 Import Attendance**
   - Click **Browse File**
   - Select your Excel/CSV file
   - **Preview** shows first few rows
   - **Map Columns:**
     - Employee ID Column → Select from dropdown
     - Date Column → Select from dropdown
     - Status Column → Select from dropdown
   - Click **Import**

3. **Review Results:**
   - Success count
   - Error count (if any)
   - Error details

### Biometric Device Integration

Most biometric devices export to Excel/CSV. Common formats supported:

**Format 1: Attendance Log**
```
Emp ID, Name, Date, In Time, Out Time
101, Rahul, 01/01/2026, 09:00, 18:00
```

**Format 2: Daily Summary**
```
Emp ID, Date, Status, Hours
101, 01/01/2026, P, 9.0
```

**Import Steps:**
1. Export from biometric device
2. Open in Excel
3. Ensure columns: Employee ID, Date, Status
4. Save as .xlsx or .csv
5. Import using steps above

### Manual Attendance Entry

For small teams or corrections:

1. Go to **Leave Management**
2. Mark leave as "Approved"
3. System treats approved leave as attendance
4. For absences: No entry needed (defaults to absent)

---

## Reports

### Payroll Reports

**Monthly Payroll Report:**

1. Click **📊 Payroll Reports**
2. Go to **Monthly Report** tab
3. Select month and year
4. Click **Load Report**
5. View:
   - Employee-wise salary breakdown
   - Gross, deductions, net salary
   - Total payroll cost
6. Export to Excel/CSV

**Year-to-Date (YTD) Report:**

1. Go to **YTD Report** tab
2. Select year and month (up to)
3. Click **Load Report**
4. Shows cumulative data from April to selected month

**Annual Summary:**

1. Go to **Annual Summary** tab
2. Select financial year
3. View complete year's payroll data

### Leave Reports

**All Employee Leave Balances:**

1. Click **📊 Leave Balance Reports**
2. Select year
3. View opening, accrued, used, closing balances
4. Export to Excel

**Employee-Specific Leave Report:**

1. Go to **Employee Leave Report** tab
2. Select employee and year
3. View detailed leave history

### Custom Reports

**Comparison Report:**

1. Go to **Comparison Report** tab
2. Select two months to compare
3. View month-over-month changes

---

## Tax Management

### Employee Tax Declarations

**For Each Employee (Annual Process):**

1. Click **💰 Tax & Form 16**
2. Go to **Employee Tax Declarations** tab
3. Select employee
4. **Choose Tax Regime:**
   - **New Regime**: Lower rates, no deductions
   - **Old Regime**: Higher rates, allows deductions

5. **If Old Regime, Enter:**
   - **HRA Details:**
     - Annual rent paid
     - Check "Metro City" if applicable
   - **Section 80C:** PF, LIC, ELSS (max ₹1.5L)
   - **Section 80D:** Health insurance (max ₹25K)
   - **Section 80G:** Donations
   
6. **Other Income:**
   - Interest income
   - Rental income
   - Previous employer income (if joined mid-year)
   - Previous employer TDS

7. Click **Save Declaration**

**Best Practice:** Collect declarations in April/May each year.

### Tax Calculator

**To Help Employees Choose Regime:**

1. Go to **Tax Calculator** tab
2. Select employee
3. Click **Calculate Tax**
4. View detailed breakdown:
   - Gross income
   - Deductions (if Old regime)
   - Taxable income
   - Tax liability
   - Monthly TDS

5. Compare Old vs New regime
6. Recommend best option to employee

### Form 16 Generation

**Year-End Process (After March 31st):**

1. Ensure all payroll processed for the year
2. Verify all tax declarations saved
3. Go to **Generate Form 16** tab
4. Select:
   - Employee
   - Financial Year (e.g., 2025-26)
5. Click **Generate Form 16 PDF**
6. PDF saved with password = Employee's PAN
7. Folder opens automatically
8. Email Form 16 to employee

**Form 16 Contains:**
- **Part A:** Quarterly TDS summary
- **Part B:** Salary computation, tax calculation
- **Annexure:** Month-wise salary and TDS details

### TDS Deduction

**Automatic Process:**

- TDS calculated automatically during payroll processing
- Based on:
  - Annual projected income
  - Tax regime selected
  - Deductions claimed
  - FY 2025-26 tax slabs
- Distributed monthly across remaining months
- Shown in salary slip as "Income Tax Deducted"

---

## Year-End Processing

### Leave Carry-Forward

**Annual Process (March/April):**

**Step 1: Configure Settings (One-time)**

1. Click **📅 Year-End Carry-Forward**
2. Go to **Carry-Forward Settings** tab
3. For each leave type:
   - Enable/disable carry-forward
   - Set maximum days
   
**Recommended Settings:**
- Earned Leave: 15 days max ✅
- Sick Leave: 0 days (no carry-forward)
- Casual Leave: 0 days (no carry-forward)

4. Click **Save Settings**

**Step 2: Year-End Processing**

1. Go to **Year-End Processing** tab
2. Select:
   - From year: 2025
   - To year: 2026
3. Click **Preview Carry-Forward**
4. **Review Preview:**
   - Employee-wise breakdown
   - Days carried forward
   - Days lapsed
   - Total summary
5. If satisfied, click **Process Carry-Forward**
6. Confirm action
7. System creates next year's opening balances

**Example:**
```
Employee: Rahul Kumar
Earned Leave Balance (2025): 20 days
Max Carry-Forward: 15 days
Result:
  - Carried to 2026: 15 days ✅
  - Lapsed: 5 days ❌
```

### Financial Year Closing

**Checklist:**

- [ ] Process December payroll
- [ ] Process January-March payroll
- [ ] Generate all Form 16s
- [ ] Process leave carry-forward
- [ ] Generate annual reports
- [ ] Backup database
- [ ] Archive payroll documents

---

## Employee Self-Service Portal

### Admin Setup

**Setting Employee Passwords:**

1. Click **🏢 Employee Portal**
2. Click **Manage Employee Access**
3. Select employee
4. Click **Set Password**
5. Enter password (or auto-generate)
6. Click **Save**
7. Share credentials with employee

### Employee Login

**For Employees:**

1. Admin clicks **🏢 Employee Portal** → **Launch Portal**
2. Employee enters:
   - Employee ID
   - Password
3. Click **Login**

### Portal Features

**Dashboard Tabs:**

**1. Salary Slips:**
- View all salary slips
- Select month/year
- View HTML slip
- Download PDF (password: Employee ID)

**2. Leave Balance:**
- View current leave balances
- See opening, accrued, used, closing
- Visual cards for each leave type

**3. Apply Leave:**
- Select leave type
- Choose from/to dates
- Enter reason
- Submit request
- Admin receives for approval

**4. Attendance Records:**
- View monthly attendance
- See present/absent days
- Month-wise summary

**5. Profile:**
- View personal details
- Contact information
- Bank details
- PAN, UAN

---

## Advanced Features

### Custom Allowance/Deduction Templates

**Creating Templates:**

1. Click **📋 Templates**
2. Click **Create Template**
3. Enter template name
4. Add multiple allowances/deductions:
   - Name
   - Amount
   - Type (Fixed/Percentage/One-time)
5. Click **Save Template**

**Applying Templates:**

1. Select template from list
2. Click **Apply to Employees**
3. Select employees (or Select All)
4. Click **Apply**
5. Allowances/deductions added to selected employees

**Use Cases:**
- Standard allowances for all employees
- Department-specific allowances
- Grade-based deductions
- One-time bonuses

### Automatic Payroll Reminders

**Setup:**

1. Click **⏰ Reminders**
2. Enable **Payroll Reminders**
3. Configure:
   - Reminder day (e.g., 25th of each month)
   - Recipient emails (HR, Accounts)
   - Email subject and message
4. Click **Save Settings**

**How It Works:**
- System runs daily at 9 AM
- Checks if payroll processed for current month
- If not, sends reminder email
- Stops after payroll is processed

**Test Reminder:**
- Click **Send Test Reminder** to verify email

### Bulk Salary Slip Sharing

**Email All Employees:**

1. Click **📧 Share Salary Slips**
2. Select month and year
3. Check **Select All**
4. Click **Bulk Email**
5. System sends individual emails to all employees
6. Progress bar shows status

**WhatsApp Sharing:**

1. Same as email
2. Click **Bulk WhatsApp**
3. Opens WhatsApp Web for each employee
4. You need to click "Send" for each (WhatsApp limitation)

---

## Tips & Best Practices

### Monthly Workflow

**Recommended Timeline:**

| Day | Activity |
|-----|----------|
| 1-5 | Import attendance for previous month |
| 5-10 | Process leave requests |
| 20-25 | Review salary changes, additions |
| 25-28 | Process bulk payroll |
| 28-30 | Review salary slips, reports |
| 30-31 | Email salary slips to employees |
| Month-end | Generate and archive reports |

### Data Backup

**Critical:**
- Backup `database` folder daily during payroll month
- Weekly backups during normal operations
- Before year-end processing
- Before any bulk operations

**How to Backup:**
1. Close application
2. Copy entire `database` folder
3. Rename with date: `database_backup_2026-01-31`
4. Store in safe location (cloud/external drive)

### Security Best Practices

1. **Password-protect salary slips** ✅ (automatic)
2. **Limit access** to payroll system
3. **Regular backups** of database
4. **Secure email** configuration (use app passwords)
5. **Employee portal** passwords should be strong
6. **Regular audits** of payroll data

### Performance Optimization

**For Large Employee Counts (100+):**

1. Process payroll during off-peak hours
2. Close unnecessary applications
3. Ensure 4GB+ RAM available
4. Consider batch processing (50 employees at a time)
5. Regular database maintenance

---

## Troubleshooting

### Common Issues

**Issue: Email not sending**
- Check SMTP settings
- Verify internet connection
- For Gmail: Use App Password, not regular password
- Test with **Test Email** button

**Issue: PDF generation fails**
- Ensure WeasyPrint installed: `pip install weasyprint`
- Check if company logo path is correct
- Verify sufficient disk space

**Issue: Portal login fails**
- Verify password is set for employee
- Check if employee ID is correct (case-sensitive)
- Ensure employee is active

**Issue: Reports show no data**
- Verify payroll is processed for selected period
- Check date range selection
- Refresh report

### Getting Help

1. Check [FAQ](PAYROLL_FAQ.md)
2. Review error messages in terminal
3. Check system logs
4. Contact IT support with:
   - Steps to reproduce
   - Screenshots
   - Error messages

---

## Appendix

### Tax Slabs (FY 2025-26)

**New Regime:**
| Income Range | Tax Rate |
|--------------|----------|
| ₹0 - ₹3,00,000 | 0% |
| ₹3,00,001 - ₹7,00,000 | 5% |
| ₹7,00,001 - ₹10,00,000 | 10% |
| ₹10,00,001 - ₹12,00,000 | 15% |
| ₹12,00,001 - ₹15,00,000 | 20% |
| Above ₹15,00,000 | 30% |

**Old Regime:**
| Income Range | Tax Rate |
|--------------|----------|
| ₹0 - ₹2,50,000 | 0% |
| ₹2,50,001 - ₹5,00,000 | 5% |
| ₹5,00,001 - ₹10,00,000 | 20% |
| Above ₹10,00,000 | 30% |

Plus 4% Health & Education Cess on tax amount.

### Professional Tax (Maharashtra)

| Monthly Gross Salary | PT Amount |
|---------------------|-----------|
| Up to ₹7,500 | ₹0 |
| ₹7,501 - ₹10,000 | ₹175 |
| Above ₹10,000 | ₹200 |

Maximum annual PT: ₹2,500

---

**Document Version:** 1.0  
**Last Updated:** February 2026  
**For Support:** Contact your system administrator
