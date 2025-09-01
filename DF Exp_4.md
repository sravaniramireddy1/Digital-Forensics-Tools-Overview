
📖 Description

**This experiment demonstrates how to analyze an email header to identify sender details, authentication checks that could indicate phishing or spoofing attempts**.

🔹 🛠️ Step-by-Step Procedure

1️⃣ Access the Email Header

💠 Open the gmail and Open any mail that you want to analyze 

💠 After selecting the email click on more then click show original.

<img width="1877" height="839" alt="Screenshot 2025-08-29 162219" src="https://github.com/user-attachments/assets/fa67345e-52a7-4800-9253-9f150f0a0628" />

 2️⃣ Identify Key Header Fields

🔹 From: Sender’s email

🔹 To: Recipient’s email

🔹 Date: Time the email was sent

🔹 Subject: Email subject line

🔹 Return-Path: Bounce-back address

🔹 Received: Path of servers

🔹 Message-ID: Unique identifier for the email

🔹 SPF/DKIM/DMARC: Authentication results.

<img width="1647" height="758" alt="Screenshot 2025-08-29 162152" src="https://github.com/user-attachments/assets/f8005566-b16b-4534-baa3-58d020d1926a" />

3️⃣ Copy the Email Header

Select and copy in message header analyzer 

<img width="1826" height="591" alt="Screenshot 2025-08-31 231851" src="https://github.com/user-attachments/assets/d9741a45-2529-4144-9d99-319f09c7f40b" />

4️⃣ Analyze the ‘Received’ Fields 🌍

🔹 The Received field shows the path of the email in reverse order.

🔹 Each entry has: sending server IP/hostname, receiving server IP/hostname, and a timestamp.

🔹 Check IPs and hostnames using WHOIS or IP lookup tools.

🔹 Verify any suspicious IPs or hostnames.

<img width="1799" height="509" alt="Screenshot 2025-08-29 162704" src="https://github.com/user-attachments/assets/435d87fd-5db5-4e33-91f6-26e2423e2117" />

5️⃣ Examine SPF, DKIM, and DMARC Results 🔐

SPF: Confirms if sender IP is valid.

✅ Pass → Authorized sender.

❌ Fail → Possible spoofing.

DKIM: Confirms message integrity.

✅ Pass → Content not altered.

❌ Fail → Content tampered.

DMARC: Combines SPF & DKIM.

✅ Pass → Authentication valid.

❌ Fail → Spoofing possible.

6️⃣ Analyze the ‘Message-ID’ 🆔

🔹Message ID is unique per each email.

🔹Domain must match sender’s domain .

🔹**Mismatches in any of these leads to Spoofing alert**

<img width="1811" height="734" alt="Screenshot 2025-09-01 142701" src="https://github.com/user-attachments/assets/723dddc7-a56e-451b-91db-4be7ff7d7de4" />

✅ Result

**This experiment demonstrates how to analyze an email header to trace sender details, verify authentication (SPF, DKIM, DMARC), and detect phishing or spoofing attempts. It ensures better email security by identifying suspicious servers, domains, or tampered content.**
