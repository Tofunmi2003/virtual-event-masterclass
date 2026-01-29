# ⚡ Zapier Integration Guide
## Connect Custom Form (Formspree) → Systeme.io

Since you are using the **Custom Premium Form**, we need a bridge to tell Systeme.io to send the emails. That bridge is **Zapier**.

### ✅ Prerequisites
1.  **Formspree Account**: You already have this (where you got the ID).
2.  **Systeme.io Account**: You have this.
3.  **Zapier Account**: A free account should suffice for basic testing.

---

### 🚀 Step 1: Connect via Formspree Dashboard (The "Backdoor")
Sometimes Formspree doesn't show up in the Zapier public search. Here is the fix:

1.  Go to your **[Formspree Dashboard](https://formspree.io/forms)**.
2.  Click on your form (the one with ID `mpqrddnp`).
3.  Click on the **"Integration"** or **"Plugins"** tab.
4.  Find **Zapier** and click **"Connect"** (or "+").
5.  This will force-open Zapier and create the trigger for you.

#### ⚠️ Alternative: "Webhooks by Zapier" (If above fails)
If you still can't connect:
1.  In Zapier, search for **"Webhooks by Zapier"** (Premium feature) as the Trigger.
2.  Choose "Catch Hook".
3.  Copy the **Webhook URL** Zapier gives you.
4.  Go to Formspree > Plugins > **Webhook**.
5.  Paste the Zapier URL there.

---

### 🔗 Step 2: Prepare the Action (Systeme.io)
1.  **Action App**: Search for `Systeme.io`.
2.  **Action Event**: Select `Create or Update Contact`.
3.  **Account**: Connect your Systeme.io account (you may need an API key from Systeme.io Settings > Public API Keys).
4.  **Map the Fields**:
    *   **Email**: Select `Email` from Formspree.
    *   **First Name**: Select `FirstName` from Formspree.
    *   **Last Name**: Select `LastName` from Formspree.
    *   **Phone**: Select `Phone` from Formspree.
5.  **Tag/Campaign (Crucial)**:
    *   In the "Campaign" or "Tag" field in Zapier, select your **"Masterclass" Tag**.
    *   *Note:* In Systeme.io, you should have an Automation Rule that says: *"When contact added to Tag [Masterclass] -> Subscribe to Campaign [3-Day Sequence]"*.

---

### 🏁 Step 3: Turn It Live
1.  Click **"Test & Continue"**.
2.  Check your Systeme.io "Contacts" list. Did "Test User" appear?
3.  If yes, click **"Publish Zap"**.

### 🎉 Result
*   User fills form on your site.
*   Formspree catches it + Redirects to Thank You Page (Instant).
*   Zapier sends data to Systeme.io (Instant).
*   Systeme.io sends "Welcome Email" (Instant).

You now have the best of both worlds: **Premium Design** + **Full Automation**.
