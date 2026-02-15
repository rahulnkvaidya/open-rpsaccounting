# Payroll System - Frequently Asked Questions (FAQ)

## Table of Contents
1. [Getting Started](#getting-started)
2. [Employee Management](#employee-management)
3. [Payroll Processing](#payroll-processing)
4. [Salary Slips](#salary-slips)
5. [Leave Management](#leave-management)
6. [Attendance](#attendance)
7. [Tax & Form 16](#tax--form-16)
8. [Year-End Processing](#year-end-processing)
9. [Troubleshooting](#troubleshooting)

---

## Getting Started

### Q1: How do I start the payroll system?
**A:** Open terminal/command prompt, navigate to the RPS Accounting folder, and run:
```bash
python main.py
```

### Q2: What are the system requirements?
**A:** 
- Python 3.8 or higher
- Required libraries: customtkinter, pandas, weasyprint, PyPDF2
- Windows/Mac/Linux operating system
- 100MB free disk space

### Q3: Where is the data stored?
**A:** All data is stored in SQLite database files in the `database` folder. No external database server required.

---

## Employee Management

### Q4: How do I add a new employee?
**A:** 
1. Click **👤 Manage Employees**
2. Click **Add Employee**
3. Fill in employee details (Name, ID, Designation, Salary, etc.)
4. Click **Save**

### Q5: Can I add custom allowances for specific employees?
**A:** Yes! After adding an employee:
1. Select the employee from the list
2. Click **View Details**
3. In the **Allowances** section, click **Add Allowance**
4. Enter allowance name and amount
5. Click **Save**

### Q6: How do I deactivate an employee who has left?
**A:** 
1. Go to **Manage Employees**
2. Select the employee
3. Click **Deactivate Employee**
4. Confirm the action

**Note:** Deactivated employees won't appear in payroll processing but their historical data is preserved.

---

## Payroll Processing

### Q7: What's the difference between "Process Payroll" and "Bulk Process Payroll"?
**A:** 
- **Process Payroll**: Process one employee at a time
- **Bulk Process Payroll**: Process all active employees at once (recommended for monthly payroll)

### Q8: How do I process monthly payroll?
**A:** 
1. Click **📄 Bulk Process Payroll**
2. Select **Month** and **Year**
3. Review the employee list
4. Click **Process All**
5. System will calculate salary, deductions, and create vouchers automatically

### Q9: Can I reprocess payroll for a month?
**A:** Yes, but the system will warn you if payroll already exists for that month. Reprocessing will update the existing records.

### Q10: How are deductions calculated?
**A:** Deductions are calculated based on:
- Employee-specific deductions (PF, ESI, Loans)
- Income Tax (TDS) - calculated automatically based on tax declarations
- Professional Tax - based on state (default: Maharashtra)

---

## Salary Slips

### Q11: How do I generate salary slips?
**A:** Salary slips are automatically generated when you process payroll. To view/share:
1. Click **📧 Share Salary Slips**
2. Select **Month** and **Year**
3. Choose employees
4. Select **Email** or **WhatsApp**
5. Click **Send**

### Q12: Are salary slips password-protected?
**A:** Yes! All salary slip PDFs are password-protected. The password is the employee's **Employee ID** by default.

### Q13: Can I customize the salary slip format?
**A:** The salary slip includes:
- Company logo and letterhead
- Employee details
- Earnings breakdown
- Deductions breakdown
- Net salary
- Month-wise summary

The format follows standard Indian payroll practices.

### Q14: How do I bulk email salary slips?
**A:** 
1. Go to **Share Salary Slips**
2. Select the month
3. Check **Select All** to select all employees
4. Click **Bulk Email**
5. System will send individual emails to all employees

**Note:** Ensure email settings are configured in Settings → Email Configuration.

---

## Leave Management

### Q15: What leave types are supported?
**A:** Default leave types:
- Earned Leave (EL)
- Sick Leave (SL)
- Casual Leave (CL)
- Loss of Pay (LOP)

You can add custom leave types in the database.

### Q16: How do I set opening leave balances?
**A:** 
1. Click **🏖️ Leave Management**
2. Click **Set Opening Balances**
3. Select employee, year, and leave type
4. Enter opening balance
5. Click **Save**

### Q17: How does monthly leave accrual work?
**A:** 
- System automatically accrues leave monthly based on company policy
- Default: 1.25 days of Earned Leave per month (15 days/year)
- Configure in database: `employee_leave_balances` table

### Q18: How do I approve/reject leave requests?
**A:** 
1. Go to **Leave Management**
2. Click **Pending Approvals** tab
3. Select the leave request
4. Click **Approve** or **Reject**
5. Add remarks (optional)

### Q19: Can employees apply for leave themselves?
**A:** Yes! Through the **Employee Self-Service Portal**:
1. Click **🏢 Employee Portal**
2. Employee logs in with their credentials
3. Goes to **Apply Leave** tab
4. Fills the form and submits

---

## Attendance

### Q20: How do I import attendance from Excel?
**A:** 
1. Click **📥 Import Attendance**
2. Click **Browse** and select your Excel/CSV file
3. Map columns (Employee ID, Date, Status)
4. Preview the data
5. Click **Import**

### Q21: What file formats are supported for attendance import?
**A:** 
- Excel (.xlsx, .xls)
- CSV (.csv)
- Tab-separated (.txt)
- Common biometric device export formats

### Q22: What's the expected format for attendance files?
**A:** Minimum required columns:
- Employee ID or Employee Name
- Date (any common format: DD/MM/YYYY, YYYY-MM-DD, etc.)
- Status (Present/Absent/Half Day/Leave)

Example:
```
Employee ID, Date, Status
101, 01/01/2025, Present
102, 01/01/2025, Absent
```

---

## Tax & Form 16

### Q23: How do I configure employee tax declarations?
**A:** 
1. Click **💰 Tax & Form 16**
2. Go to **Employee Tax Declarations** tab
3. Select employee
4. Choose tax regime (Old/New)
5. Enter HRA, 80C, 80D details
6. Click **Save Declaration**

### Q24: What's the difference between Old and New tax regime?
**A:** 
**New Regime (Default):**
- Lower tax rates
- No deductions (except standard deduction ₹50,000)
- Simpler calculation

**Old Regime:**
- Higher tax rates
- Allows deductions: HRA, 80C (₹1.5L), 80D (₹25K), etc.
- Better for those with high deductions

### Q25: How do I generate Form 16?
**A:** 
1. Click **💰 Tax & Form 16**
2. Go to **Generate Form 16** tab
3. Select employee and financial year
4. Click **Generate Form 16 PDF**
5. PDF will be saved with password (employee's PAN)

### Q26: When should I generate Form 16?
**A:** Generate Form 16 at the end of the financial year (after March 31st) for the previous financial year.

### Q27: How is TDS calculated?
**A:** TDS is calculated automatically based on:
1. Annual projected income
2. Tax regime selected
3. Deductions claimed (if Old regime)
4. Tax slabs for FY 2025-26
5. Distributed monthly across remaining months

---

## Year-End Processing

### Q28: How do I carry forward leave balances to next year?
**A:** 
1. Click **📅 Year-End Carry-Forward**
2. Go to **Year-End Processing** tab
3. Select "from year" and "to year"
4. Click **Preview Carry-Forward** to see results
5. Review the preview
6. Click **Process Carry-Forward** to execute

### Q29: What happens to unused leave?
**A:** Depends on leave type settings:
- **Earned Leave**: Carries forward up to max limit (default: 15 days)
- **Sick Leave**: Typically lapses (default: 0 days carry-forward)
- **Casual Leave**: Typically lapses (default: 0 days carry-forward)

Configure limits in **Carry-Forward Settings** tab.

### Q30: Can I change carry-forward limits?
**A:** Yes!
1. Go to **Year-End Carry-Forward**
2. Click **Carry-Forward Settings** tab
3. For each leave type:
   - Enable/disable carry-forward
   - Set maximum days
4. Click **Save Settings**

---

## Troubleshooting

### Q31: Salary slip email is not sending. What should I check?
**A:** 
1. Go to **Settings → Email Configuration**
2. Verify SMTP settings:
   - SMTP Server (e.g., smtp.gmail.com)
   - Port (587 for TLS, 465 for SSL)
   - Email and password
3. For Gmail: Enable "App Passwords" in Google Account settings
4. Test email by clicking **Test Email**

### Q32: Employee portal login not working?
**A:** 
1. Ensure password is set for the employee:
   - Go to **Employee Portal Management**
   - Select employee
   - Click **Set Password**
2. Verify employee is active
3. Check if employee ID is correct

### Q33: Payroll reports showing zero data?
**A:** 
1. Ensure payroll is processed for the selected period
2. Check if employees have salary records
3. Verify date range selection
4. Try refreshing the report

### Q34: How do I backup my data?
**A:** 
1. Close the application
2. Copy the entire `database` folder
3. Store it in a safe location
4. Recommended: Daily backups during payroll processing

### Q35: Can I restore from backup?
**A:** Yes!
1. Close the application
2. Replace the `database` folder with your backup
3. Restart the application

### Q36: System is slow when processing bulk payroll?
**A:** This is normal for large employee counts (100+). Tips:
- Process during off-peak hours
- Close other applications
- Ensure sufficient RAM (4GB+ recommended)
- Consider processing in smaller batches

### Q37: How do I update tax slabs for a new financial year?
**A:** Tax slabs are stored in the `tax_settings` table. To update:
1. Open database using SQLite browser
2. Update `tax_settings` table
3. Or contact support for assistance

### Q38: Can multiple users access the system simultaneously?
**A:** The current version uses SQLite which supports single-user access. For multi-user:
- Consider upgrading to PostgreSQL/MySQL backend
- Or use network file sharing (with caution - may cause data conflicts)

---

## Best Practices

### Q39: What's the recommended monthly payroll workflow?
**A:** 
1. **Day 1-5**: Import attendance for the month
2. **Day 20-25**: Review and approve leave requests
3. **Day 25-28**: Process bulk payroll
4. **Day 28-30**: Review salary slips
5. **Day 30-31**: Email salary slips to employees
6. **Month-end**: Generate payroll reports

### Q40: How often should I backup data?
**A:** 
- **Daily**: During payroll processing month
- **Weekly**: During normal operations
- **Monthly**: After payroll completion
- **Yearly**: Before year-end processing

### Q41: Should I use Old or New tax regime for employees?
**A:** Recommend employees to:
1. Use **Tax Calculator** in the system
2. Compare tax liability in both regimes
3. Choose based on their deductions
4. Generally:
   - High deductions (HRA, 80C) → Old Regime
   - Low deductions → New Regime

---

## Support

### Q42: Where can I get help?
**A:** 
- Check this FAQ first
- Review the User Guide (USER_GUIDE.md)
- Check system logs for error messages
- Contact your system administrator

### Q43: How do I report a bug?
**A:** 
1. Note the exact steps to reproduce
2. Take screenshots if applicable
3. Check error messages in terminal/console
4. Report to your IT team with details

---

**Last Updated:** February 2026  
**Version:** 1.0 - Enterprise Payroll System
