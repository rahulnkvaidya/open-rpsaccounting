# Gmail App Password Setup Guide for RPS Accounting

RPS Accounting uses SMTP to send emails (Payroll Reminders, Attendance Alerts, etc.).
If you are using a **Gmail** account, you cannot use your regular login password. You must generate and use a secure **App Password**.

## Step-by-Step Instructions

### 1. Enable 2-Step Verification
*App Passwords only work if 2-Step Verification is enabled.*

1.  Go to your [Google Account Settings](https://myaccount.google.com/).
2.  Click on **Security** in the left navigation panel.
3.  Under "Signing in to Google", select **2-Step Verification**.
4.  If it is not "On", click it and follow the steps to enable it (using your phone number or authenticator app).

### 2. Generate an App Password

1.  Stay in the **Security** section of your Google Account.
2.  Scroll to the bottom or search for **"App passwords"** in the search bar at the top of the page.
3.  Click on **App passwords**. You may be asked to sign in again.
4.  **Select app**: Choose "Mail".
5.  **Select device**: Choose "Windows Computer".
6.  Click **Generate**.

### 3. Configure RPS Accounting

1.  Google will display a **16-character password** in a yellow bar (e.g., `abcd efgh ijkl mnop`).
2.  **Copy** this password.
3.  Open **RPS Accounting**.
4.  Go to **Settings** -> **Sync Settings** -> **Email / SMTP Settings**.
5.  **SMTP User**: Enter your full Gmail address (e.g., `yourname@gmail.com`).
6.  **SMTP Password**: Paste the **16-character App Password** you just copied.
7.  **SMTP Host**: `smtp.gmail.com`
8.  **SMTP Port**: `587`
9.  **Use TLS**: On
10. Click **Save SMTP Settings**.
11. Click **Send Test Email** to verify it works.

## Troubleshooting

-   **Error 534 / Application-specific password required**: This confirms you are using your regular password instead of an App Password. Follow the steps above to fix it.
-   **Timeout**: Check your internet connection.
-   **Authentication Failed**: Ensure there are no leading/trailing spaces in the password.

---
*For further assistance, please contact RPS Accounting Support.*
