# RPS Accounting - Frequently Asked Questions (FAQ)

## 📚 General Questions

### Q: What is RPS Accounting?
**A:** RPS Accounting is a complete double-entry accounting software for Indian businesses. It supports voucher entry, billing, inventory, GST compliance, and comprehensive financial reports.

### Q: Is it suitable for my business?
**A:** Yes! RPS Accounting is suitable for:
- Small businesses
- Retail shops
- Service providers
- Manufacturing units
- Trading companies
- Any business needing accounting

### Q: Does it support GST?
**A:** Yes, full GST support including:
- GST invoicing
- HSN codes
- Tax calculations (CGST, SGST, IGST)
- GST Summary reports

---

## 💾 Company & Data Management

### Q: How do I create a new company?
**A:** File → Create New Company → Enter company details → Set financial year → Click Create.

### Q: Can I manage multiple companies?
**A:** Yes! Create multiple companies and switch between them using File → Switch Company.

### Q: How do I backup my data?
**A:** File → Backup Company → Choose location → Click Backup. Do this weekly!

### Q: How do I restore from backup?
**A:** File → Restore Company → Select backup file → Click Restore.

### Q: Where is my data stored?
**A:** In the `database` folder inside the application directory. Each company has its own database file.

---

## 📊 Ledgers & Masters

### Q: What is a Ledger?
**A:** A ledger is an account (e.g., Cash, Bank, Sales, Purchase, Customer name, Supplier name).

### Q: What are Ledger Groups?
**A:** Groups categorize ledgers:
- **Cash-in-Hand** - Cash accounts
- **Bank Accounts** - Bank accounts
- **Sundry Debtors** - Customers (who owe you)
- **Sundry Creditors** - Suppliers (whom you owe)
- **Sales Accounts** - Income from sales
- **Purchase Accounts** - Purchase expenses

### Q: How do I create a ledger?
**A:** Masters → Ledgers → Add Ledger → Enter name → Select group → Save.

### Q: Can I delete a ledger?
**A:** Yes, but only if it has no transactions. Otherwise, you can deactivate it.

---

## 📝 Voucher Entry

### Q: What is the difference between Receipt and Payment?
**A:**
- **Receipt (F3)**: Money coming IN (Debit Cash/Bank)
- **Payment (F5)**: Money going OUT (Credit Cash/Bank)

### Q: What is a Contra voucher?
**A:** Transfer between Cash and Bank accounts (e.g., depositing cash in bank).

### Q: What is a Journal voucher?
**A:** General adjustments between any ledgers (not involving cash/bank directly).

### Q: How do I edit a voucher?
**A:** Open Day Book or Ledger Report → Click on the voucher → Make changes → Ctrl+S to save.

### Q: How do I delete a voucher?
**A:** Open the voucher → Click Delete button → Confirm deletion.

### Q: Can I edit/delete old vouchers?
**A:** Yes, but it's recommended to make adjusting entries instead of deleting old vouchers for audit trail.

---

## 🧾 Billing & Invoicing

### Q: How do I create a sales invoice?
**A:** Press F8 → Select customer → Add items → System calculates total → Ctrl+S to save.

### Q: How do I add more item rows?
**A:** Press Ctrl+Plus or click "Add Item" button. Cursor auto-focuses on the new row!

### Q: How do I print an invoice?
**A:** Press Ctrl+P (Save & Print) or save first, then click Print button.

### Q: Can I add discounts?
**A:** Yes, there's a discount field in the billing screen. Enter amount or percentage.

### Q: How do I add GST to invoices?
**A:** Select items with HSN codes and GST rates. System automatically calculates CGST/SGST/IGST.

---

## 📦 Purchase Orders

### Q: How do I create a Purchase Order?
**A:** Purchase Order → Create New PO → Select vendor → Add items → Ctrl+S to save.

### Q: Can I print Purchase Orders?
**A:** Yes! Press Ctrl+P to save and print, or click "Save & Print" button.

### Q: What's the difference between PO and Purchase Voucher?
**A:**
- **Purchase Order**: Intent to buy (doesn't affect accounts)
- **Purchase Voucher (F9)**: Actual purchase (creates accounting entry)

---

## 📈 Reports

### Q: Which reports are available?
**A:** 15 reports including:
- Day Book, Ledger Report
- Sales Report, Purchase Report
- Receivables (Debtors), Payables (Creditors)
- Trial Balance, Balance Sheet, Profit & Loss
- Cash Flow Statement, GST Summary

### Q: How do I view who owes me money?
**A:** Reports → Receivables (Debtors) → Select date → View outstanding amounts.

### Q: How do I view whom I owe money?
**A:** Reports → Payables (Creditors) → Select date → View outstanding amounts.

### Q: Can I export reports to Excel?
**A:** Yes, most reports have an "Export to Excel" button.

### Q: Reports show no data. Why?
**A:** Check:
1. Date range is correct
2. Vouchers are saved for that period
3. Company is selected

---

## 🔧 Technical Issues

### Q: Application shows blank screen on startup
**A:** This has been fixed in the latest version. Restart the application.

### Q: Dark mode creates duplicate sidebar
**A:** This has been fixed. Toggle dark mode from Settings.

### Q: Keyboard shortcuts not working
**A:** Make sure:
1. You're in the correct screen
2. No popup is open
3. Focus is not in a text field (press Escape first)

### Q: Print preview not showing
**A:** Ensure the voucher/invoice is saved first (Ctrl+S), then try printing.

---

## 💰 Accounting Concepts

### Q: What is Debit and Credit?
**A:**
- **Debit (Dr)**: Receiving/Asset increase/Expense
- **Credit (Cr)**: Giving/Liability increase/Income

**Examples:**
- Cash sales: Dr Cash, Cr Sales
- Cash purchase: Dr Purchase, Cr Cash
- Customer payment: Dr Cash, Cr Customer

### Q: What is Trial Balance?
**A:** A report showing all ledger balances. Total Debit should equal Total Credit.

### Q: What is Balance Sheet?
**A:** Shows financial position (Assets vs Liabilities) on a specific date.

### Q: What is Profit & Loss?
**A:** Shows income and expenses for a period, resulting in profit or loss.

### Q: What is Cash Flow Statement?
**A:** Shows actual cash inflows and outflows categorized into Operating, Investing, and Financing activities.

---

## 🎓 Best Practices

### Q: How often should I backup?
**A:** 
- **Daily** during busy periods
- **Weekly** minimum
- **Before** year-end closing
- **Before** any bulk operations

### Q: Should I use narration?
**A:** Yes! Always add clear narration for easy tracking and audit trail.

### Q: What naming convention for ledgers?
**A:**
- Customers: "Customer - ABC Company"
- Suppliers: "Supplier - XYZ Traders"
- Expenses: "Electricity Expense", "Rent Expense"
- Clear, descriptive names

### Q: How to organize ledgers?
**A:** Use proper groups:
- All customers in "Sundry Debtors"
- All suppliers in "Sundry Creditors"
- All expenses in appropriate expense groups

---

## 🆘 Getting Help

### Q: Where can I find more help?
**A:**
1. **Quick Start Guide**: docs/RPS_QUICK_START.md
2. **User Manual**: docs/RPS_USER_MANUAL.md (coming soon)
3. **Keyboard Shortcuts**: docs/KEYBOARD_SHORTCUTS.md
4. **Video Tutorials**: Help → Video Tutorials (in-app)

### Q: How do I report a bug?
**A:** Contact your IT support team with:
- Steps to reproduce
- Screenshots
- Error messages (if any)

### Q: Is there a tutorial video?
**A:** Yes! Access from Help → Video Tutorials in the application.

---

**Version:** 1.0 | **Updated:** February 2026  
**Software:** RPS Accounting
