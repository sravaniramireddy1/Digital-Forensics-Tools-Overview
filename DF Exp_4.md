
🔹 📖 Description

This experiment demonstrates how to analyze an email header 📨 to identify sender details, authentication checks 🔐, and anomalies 🚨 that could indicate phishing or spoofing attempts.

🔹 🛠️ Step-by-Step Procedure

1️⃣ Access the Email Header

📧 Gmail: Open the email → ⋮ (More) → Show original.

💻 Outlook: Open email → File → Properties → check Internet headers.

📨 Yahoo: Open the email → ⋮ (More) → View raw message

<img width="1877" height="839" alt="Screenshot 2025-08-29 162219" src="https://github.com/user-attachments/assets/fa67345e-52a7-4800-9253-9f150f0a0628" />

 Identify Key Header Fields

👤 From: Sender’s email.

🎯 To: Recipient’s email.

🕒 Date: Sent time.

📝 Subject: Email subject line.

🔄 Return-Path: Bounce-back address.

🌐 Received: Path of servers.

🆔 Message-ID: Unique email ID.

✅ SPF/DKIM/DMARC: Authentication results.

<img width="1647" height="758" alt="Screenshot 2025-08-29 162152" src="https://github.com/user-attachments/assets/f8005566-b16b-4534-baa3-58d020d1926a" />

Copy the Email Header

Select and copy in message header analyzer 

<img width="1826" height="591" alt="Screenshot 2025-08-31 231851" src="https://github.com/user-attachments/assets/d9741a45-2529-4144-9d99-319f09c7f40b" />

4️⃣ Analyze the ‘Received’ Fields 🌍

Shows the path of email (reverse order).

Each entry contains:

📡 Sending server hostname/IP.

💻 Receiving server hostname/IP.

⏰ Timestamp.

5️⃣ Check IP Addresses & Hostnames 🔎

Use WHOIS / IP Lookup tools 🌍.

Verify suspicious IPs ⚠️ and hostnames.

<img width="1799" height="509" alt="Screenshot 2025-08-29 162704" src="https://github.com/user-attachments/assets/435d87fd-5db5-4e33-91f6-26e2423e2117" />

6️⃣ Examine SPF, DKIM, and DMARC Results 🔐

SPF: Confirms if sender IP is valid.

✅ Pass → Authorized sender.

❌ Fail → Possible spoofing.

DKIM: Confirms message integrity.

✅ Pass → Content not altered.

❌ Fail → Content tampered.

DMARC: Combines SPF & DKIM.

✅ Pass → Authentication valid.

❌ Fail → Spoofing possible.

7️⃣ Analyze the ‘Message-ID’ 🆔

Unique per email.

Domain must match sender’s domain 🔗.

Mismatches → 🚨 Spoofing alert

✅ Result

Successfully extracted, analyzed, and interpreted email headers 📨, identifying sender info, verifying authentication 🔐, and detecting anomalies 🚨.


