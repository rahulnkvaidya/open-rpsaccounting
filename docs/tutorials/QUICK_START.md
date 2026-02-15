# Payroll System - Quick Start Guide

## 🚀 5-Minute Setup

### Step 1: Launch Application
```bash
python main.py
```

### Step 2: Add First Employee
1. Click **👤 Manage Employees**
2. Click **Add Employee**
3. Fill: Name, ID, Email, Basic Salary
4. Click **Save**

### Step 3: Process First Payroll
1. Click **📄 Bulk Process Payroll**
2. Select current month/year
3. Click **Process All**

### Step 4: View Salary Slip
1. Click **📧 Share Salary Slips**
2. Select month/year
3. Click **Preview** to see salary slip

**Done!** You've processed your first payroll. 🎉

---

## 📊 Main Menu Overview

### Row 1: Employee & Payroll
- **👤 Manage Employees** - Add/edit employees
- **💰 Process Payroll** - Individual payroll
- **📄 Bulk Process** - All employees at once
- **📧 Share Slips** - Email/WhatsApp salary slips

### Row 2: Leave & Attendance
- **🏖️ Leave Management** - Approve leaves, set balances
- **📊 Leave Reports** - View leave balances
- **📅 Year-End** - Carry-forward leaves
- **📥 Import Attendance** - From Excel/CSV

### Row 3: Advanced
- **📊 Reports** - Payroll reports
- **📋 Templates** - Allowance/deduction templates
- **⏰ Reminders** - Auto payroll reminders
- **🏢 Portal** - Employee self-service
- **💰 Tax & Form 16** - Tax management

---

## 🎯 Common Tasks

### Monthly Payroll (5 steps)
1. Import attendance → **📥 Import Attendance**
2. Approve leaves → **🏖️ Leave Management**
3. Process payroll → **📄 Bulk Process Payroll**
4. Review reports → **📊 Payroll Reports**
5. Email slips → **📧 Share Salary Slips**

### Add Custom Allowance
1. **Manage Employees** → Select employee
2. **View Details** → **Allowances** tab
3. **Add Allowance** → Enter name & amount
4. **Save**

### Generate Form 16
1. **💰 Tax & Form 16** → **Generate Form 16** tab
2. Select employee & financial year
3. **Generate Form 16 PDF**
4. PDF saved (password = PAN)

### Year-End Leave Carry-Forward
1. **📅 Year-End Carry-Forward**
2. **Year-End Processing** tab
3. Select years (e.g., 2025 → 2026)
4. **Preview** → **Process**

---

## ⚙️ Initial Setup (One-time)

### 1. Company Details
**Settings → Company Settings**
- Company name, address
- PAN, TAN
- Upload logo

### 2. Email Configuration
**Settings → Email Configuration**
- SMTP: smtp.gmail.com
- Port: 587
- Email & App Password
- **Test Email**

### 3. Tax Settings (Already configured)
- FY 2025-26 slabs pre-loaded
- Old & New regime support
- Professional Tax (Maharashtra)

---

## 💡 Pro Tips

### Bulk Operations
- Use **Templates** for standard allowances
- **Bulk Process** saves time vs individual
- **Select All** in salary slip sharing

### Reports
- Export to Excel for analysis
- YTD reports for cumulative data
- Comparison reports for trends

### Employee Portal
- Set passwords: **🏢 Employee Portal** → **Manage Access**
- Employees can view slips, apply leave
- Reduces HR workload

### Backups
- Copy `database` folder weekly
- Before year-end processing
- Before bulk operations

---

## 🆘 Quick Troubleshooting

| Problem | Solution |
|---------|----------|
| Email not sending | Check SMTP settings, use App Password for Gmail |
| Portal login fails | Set password in Employee Portal Management |
| No data in reports | Ensure payroll processed for selected period |
| PDF generation error | Install: `pip install weasyprint PyPDF2` |

---

## 📚 More Help

- **Detailed Guide:** [USER_GUIDE.md](USER_GUIDE.md)
- **FAQ:** [PAYROLL_FAQ.md](PAYROLL_FAQ.md)
- **Support:** Contact your IT team

---

**Version:** 1.0 | **Updated:** Feb 2026
