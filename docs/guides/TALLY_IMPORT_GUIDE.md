# Tally Import User Guide

## Tally se RPS Accounting mein Data Import Kaise Kare

Is guide se aap Tally accounting software se RPS Accounting mein apna data easily import kar sakte hain.

---

## Step 1: Tally se Data Export Karen

### Ledgers Export Karne Ke Liye:

1. **Tally Software** open karen
2. **Gateway of Tally** se:
   - **Display** → **Account Books** → **List of Accounts** pe jaayein
3. **Alt + E** press karein (Export option)
4. **Excel** format select karein
5. File save karen (e.g., `tally_ledgers.xlsx`)

### Vouchers/Daybook Export Karne Ke Liye:

1. **Gateway of Tally** se:
   - **Display** → **Day Book** pe jaayein
2. Date range select karen (jitne transactions chahiye)
3. **Alt + E** press karein (Export option)
4. **Excel** format select karein  
5. File save karen (e.g., `tally_daybook.xlsx`)

---

## Step 2: RPS Accounting mein Import Karen

### RPS Accounting Application Open Karen

1. RPS Accounting software start karen
2. Apni company select karen

### Ledgers Import Karen

1. Menu se **Settings** → **Import/Export** pe jaayein
2. **Import from Tally (Excel)** button click karen (orange color)
3. **Import Ledgers from Tally Excel** option select karen
4. Apni Excel file select karen (`tally_ledgers.xlsx`)
5. Import process start ho jayega
6. Success message dikhayi dega: "Successfully imported: X"

### Vouchers Import Karen

1. Menu se **Settings** → **Import/Export** pe jaayein
2. **Import from Tally (Excel)** button click karen
3. **Import Vouchers from Tally Excel** option select karen
4. Apni Excel file select karen (`tally_daybook.xlsx`)
5. Import process start ho jayega
6. Success message dikhayi dega

---

## Important Notes

### ✅ Kya Support Karta Hai:

- **Ledgers** - All ledgers with opening balance
- **Vouchers** - Payment, Receipt, Journal, Contra, Sales, Purchase
- **Auto-creation** - Agar ledger ya group missing hai, automatically create ho jayega
- **Validation** - Import se pehle data validate hota hai

### ⚠️ Dhyan Dene Waali Baatein:

1. **Backup** - Import se pehle apna database backup le len
2. **Small Test** - Pehle 5-10 ledgers/vouchers se test karen
3. **Date Format** - Dates proper format mein honi chahiye
4. **Duplicate Names** - Agar ledger already exist karta hai, skip ho jayega

### 📋 Excel Format Requirements:

**Ledgers Excel File:**
- Columns: Name, Group, Opening Balance, Dr/Cr
- Headers automatically detect honge

**Vouchers Excel File:**
- Columns: Date, Voucher Type, Particulars, Debit, Credit, Narration
- System automatically vouchers group karega

---

## Verification Steps

Import ke baad verify karen:

### 1. Ledgers Check Karen

**Reports** → **Trial Balance** → Verify that:
- All ledgers imported successfully
- Opening balances match with Tally
- Total Debit = Total Credit

### 2. Vouchers Check Karen

**Reports** → **Day Book** → Verify that:
- All vouchers imported
- Dates are correct
- Amounts match with Tally

### 3. Individual Ledger Check

**Reports** → **Ledger Report** → Select any ledger:
- Check transactions
- Verify closing balance

---

## Troubleshooting

### Problem: "No Data Found"
**Solution:** 
- Excel file check karen - proper format mein hai?
- Headers (column names) check karen
- Pehli row mein data hai ya header hai?

### Problem: "Validation Errors"
**Solution:**
- Error message padhen - kaunsi row mein problem hai
- Excel file ko manually check karen
- Empty rows delete karen

### Problem: "Group Not Found"
**Solution:**
- Tally se pehle Groups export karen
- Ya manually RPS Accounting mein groups create karen
- System automatically Suspense group use karega

### Problem: "Unbalanced Vouchers"
**Solution:**
- Voucher entries check karen
- Debit aur Credit same hone chahiye
- Excel file mein formula errors check karen

---

## Support Information

### Demo Video:
- Menu → Help → Video Tutorials

### Need Help?
- **Email:** support@RPS Accounting.com
- **Phone:** 1800-XXX-XXXX

### Additional Resources:
- **User Manual:** Settings → Help → User Guide
- **FAQs:** Settings → Help → Frequently Asked Questions

---

## Tips for Smooth Import

1. **Start Small** - Pehle 5-10 entries se test karen
2. **Clean Data** - Export se pehle Tally mein unwanted entries delete karen
3. **Backup** - Hamesha backup len before import
4. **Verify** - Import ke baad data verify zaroor karen
5. **Groups First** - Pehle ledgers, phir vouchers import karen

---

**Last Updated:** February 2026
**Version:** 1.0 (Initial Tally Import Feature)
