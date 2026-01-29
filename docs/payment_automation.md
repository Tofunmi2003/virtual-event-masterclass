# 💳 Payment Automation Guide: Getting Emails After PayPal

You are using **PayPal Buttons**, which take payment perfectly but **do not speak to Systeme.io** by default.
This means a user could pay $199 and NOT get their "Platinum" email automatically.

To fix this, we need a bridge.

## Method 1: The "Zapier Bridge" (Recommended)
This requires a Zapier account (Starter plan usually required for PayPal triggers).

1.  **Trigger**: PayPal
    *   Event: **"Successful Sale"**
    *   Connect your PayPal account.
2.  **Filter (Optional)**:
    *   If you sell multiple things, add a Filter step: "Only continue if 'Item Name' contains 'Platinum'".
3.  **Action**: Systeme.io
    *   Event: **"Create or Update Contact"**.
    *   **Email**: Map from PayPal "Payer Email".
    *   **Tag**: Add tag "Platinum Client".

**Result:**
User Pays -> PayPal tells Zapier -> Zapier tells Systeme -> Systeme sends "Welcome Platinum" email.

---

## Method 2: The "Manual Import" (Free)
If you don't want to pay for Zapier, you can do this manually once a day.

1.  Log in to **PayPal**.
2.  See a new sale for $199 from `john@example.com`.
3.  Log in to **Systeme.io** -> Contacts.
4.  **Add Contact** manually (enter `john@example.com`).
5.  **Add Tag**: "Platinum Client".
    *   *Ensure you have an Automation Rule in Systeme that says "When tag Platinum Client added -> Send Platinum Welcome Email".*

## Method 3: The "Systeme Native" Way (Best Long Term)
Instead of using PayPal buttons, create an **Order Form** inside Systeme.io.
1.  Connect PayPal *to* Systeme.io (in Settings > Payment Gateways).
2.  Create an "Order Form" page in your completion funnel.
3.  Set the price to $199.
4.  **Replace my buttons** on the website to link to this Systeme.io Order Form URL.
    *   *Benefit:* Systeme handles everything automatically without Zapier.
