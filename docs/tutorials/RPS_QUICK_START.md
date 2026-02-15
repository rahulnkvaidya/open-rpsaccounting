# RPS Accounting - Quick Start Guide

## 🚀 5-Minute Setup

### Step 1: Launch Application
Double-click **RPS Accounting** icon or run:
```bash
python main.py
```

### Step 2: Create Your First Company
1. Click **File → Create New Company**
2. Enter:
   - Company Name
   - Financial Year Start (e.g., 01-04-2025)
   - Financial Year End (e.g., 31-03-2026)
3. Click **Create**

### Step 3: Setup Basic Ledgers
1. Go to **Masters → Ledgers**
2. Create these essential ledgers:
   - **Cash** (Group: Cash-in-Hand)
   - **Bank** (Group: Bank Accounts)
   - **Sales** (Group: Sales Accounts)
   - **Purchase** (Group: Purchase Accounts)

### Step 4: Make Your First Entry
1. Press **F3** for Receipt Voucher
2. Enter date and amount
3. Select Cash/Bank (Debit)
4. Select Sales (Credit)
5. Add narration
6. Press **Ctrl+S** to Save

### Step 5: View Your First Report
1. Go to **Reports → Day Book**
2. Select date range
3. View all transactions

**Congratulations!** You've set up RPS Accounting. 🎉

---

## 📋 Main Menu Overview

### File Menu
- **Create New Company** - Start a new company
- **Switch Company** - Change active company
- **Backup Company** - Backup your data
- **Restore Company** - Restore from backup

### Masters Menu
- **Ledgers** - Create/edit ledgers
- **Ledger Groups** - Manage ledger groups
- **Inventory Items** - Add products/services
- **Voucher Types** - Customize voucher types

### Vouchers Menu
- **F3** - Receipt (Money In)
- **F4** - Contra (Bank/Cash Transfer)
- **F5** - Payment (Money Out)
- **F6** - Journal (Adjustments)
- **F8** - Sales/Billing
- **F9** - Purchase

### Reports Menu (15 Reports)
- **Day Book** - All transactions
- **Ledger Report** - Account-wise transactions
- **Sales Report** - All sales invoices
- **Purchase Report** ⭐ NEW
- **Receivables (Debtors)** ⭐ NEW
- **Payables (Creditors)** ⭐ NEW
- **Cash Flow Statement** ⭐ NEW
- **Trial Balance** - All ledger balances
- **Balance Sheet** - Financial position
- **Profit & Loss** - Income & Expenses
- **GST Summary** - Tax reports

---

## ⌨️ Keyboard Shortcuts

### Voucher Entry
| Key | Function |
|-----|----------|
| **F3** | Receipt Voucher |
| **F4** | Contra Voucher |
| **F5** | Payment Voucher |
| **F6** | Journal Voucher |
| **F8** | Sales/Billing |
| **F9** | Purchase |
| **Ctrl+S** | Save |
| **Ctrl+P** | Save & Print |
| **Escape** | Go Back/Cancel |

### Billing Screen
| Key | Function |
|-----|----------|
| **Ctrl+Plus** | Add New Item Row |
| **F2** | Focus Date Field |
| **Enter** | Next Field |

### Purchase Order
| Key | Function |
|-----|----------|
| **Ctrl+S** | Save PO |
| **Ctrl+P** | Save & Print |
| **Ctrl+Plus** | Add Item Row |
| **Escape** | Go Back |

---

## 🎯 Common Tasks

### Daily Cash Receipt
1. Press **F3**
2. Enter amount
3. Debit: Cash
4. Credit: Sales/Customer
5. **Ctrl+S** to save

### Bank Payment
1. Press **F5**
2. Enter amount
3. Debit: Expense/Supplier
4. Credit: Bank
5. **Ctrl+S** to save

### Create Sales Invoice
1. Press **F8**
2. Select customer
3. Add items (Ctrl+Plus for more rows)
4. System calculates total
5. **Ctrl+S** to save
6. **Ctrl+P** to print

### Create Purchase Order
1. **Purchase Order → Create New PO**
2. Select vendor
3. Add items
4. **Ctrl+S** to save
5. **Ctrl+P** to print

### View Outstanding Debtors
1. **Reports → Receivables (Debtors)**
2. Select "As of Date"
3. View who owes you money

### View Outstanding Creditors
1. **Reports → Payables (Creditors)**
2. Select "As of Date"
3. View whom you owe money

---

## 💡 Pro Tips

### Auto-Focus Feature
- When adding new invoice/PO items, cursor automatically jumps to item field
- Press Enter to move to next field
- No need to click with mouse!

### Date Entry
- Format: DD-MM-YYYY (e.g., 13-02-2026)
- Press F2 to quickly focus date field

### Narration
- Always add clear narration for easy tracking
- Example: "Cash sales for Feb 13" or "Electricity bill payment"

### Regular Backups
- **File → Backup Company** weekly
- Before year-end closing
- Before major data entry

---

## 🆘 Quick Troubleshooting

| Problem | Solution |
|---------|----------|
| Can't save voucher | Check if all ledgers selected |
| Report shows no data | Verify date range is correct |
| Print not working | Check if voucher is saved first |
| Blank screen on startup | Restart application |

---

## 📚 Next Steps

1. **Read Full User Manual**: [USER_MANUAL.md](USER_MANUAL.md)
2. **Learn All Features**: [FEATURE_TUTORIALS.md](FEATURE_TUTORIALS.md)
3. **Check FAQ**: [FAQ.md](FAQ.md)
4. **Watch Videos**: Help → Video Tutorials

---

**Version:** 2.0 | **Updated:** February 2026  
**Software:** RPS Accounting - Complete Accounting Solution
