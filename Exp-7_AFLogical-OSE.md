
# Ex.No.7: Use AFLogical OSE to Extract Data from an Android Device

#  Aim  
To extract logical data such as contacts, SMS, and call logs from an Android device using *AFLogical OSE* and analyze the collected evidence for forensic purposes.

---

## STEP 1 — Extract All ZIP Files

*Files you should have already downloaded:*
- [Android Platform Tools (ADB)](https://developer.android.com/tools/releases/platform-tools)
- [AFLogical OSE ZIP (source or APK)](https://sourceforge.net/projects/santoku/)
- [Google USB Driver (for Windows)](https://developer.android.com/studio/run/win-usb)

 *Instructions:*
1. Create a main folder for your lab:
   
   C:\ForensicLab
   
2. Extract all the downloaded ZIP files into it:
   
   C:\ForensicLab\platform-tools\
   C:\ForensicLab\aflogical-ose\
   C:\ForensicLab\usb-driver\
   
3. If AFLogical OSE doesn’t include an APK file, use *Santoku Linux* (a digital forensics OS) to extract or build it from the source ZIP.  
    Santoku automatically includes AFLogical OSE tools.

---

##  STEP 2 — Add platform-tools to PATH

*Purpose:* So you can run adb commands from any directory.

 *Steps:*
1. Open:
   
   Control Panel → System → Advanced system settings → Environment Variables
   
2. Under *User Variables, select **Path → Edit → New*  
   Add:
   
   C:\ForensicLab\platform-tools
   
3. Click *OK* to save changes.
<img width="490" height="478" alt="Screenshot 2025-10-28 123650" src="https://github.com/user-attachments/assets/a1908157-0e0b-4c37-adf6-b4265438a371" />


 *Verify installation:*
bash
adb version

You should see something like:

Android Debug Bridge version 1.0.41

<img width="610" height="273" alt="Screenshot 2025-10-28 123734" src="https://github.com/user-attachments/assets/8670fa8f-101f-4842-a6d3-98f6436988c7" />


---

## STEP 3 — Install Google USB Driver (Windows)

 *Required for your PC to detect the Android device.*

 *Steps:*
1. Connect your Android phone via USB.
2. Open *Device Manager* → find your phone.
3. Right-click → *Update Driver* → *Browse my computer* →  
   Select:
   
   C:\ForensicLab\usb-driver
   
4. Click *Next* to install the driver.

 *Verify:* Run
bash
adb devices

If your phone appears in the list, the driver works.

<img width="662" height="295" alt="Screenshot 2025-10-28 123800" src="https://github.com/user-attachments/assets/cdfa49e5-9894-49e5-8040-a7547769ce78" />


---

##  STEP 4 — Enable Developer Options on the Phone

 *Steps:*
1. On your phone:
   
   Settings → About phone → Tap Build number 7 times
   
2. Go back:
   
   Settings → Developer options
   
3. Enable:
   - *USB Debugging*
   - *Install via USB* (if available)

---

## STEP 5 — Connect Phone and Check ADB Connection

 *Purpose:* Ensure communication between PC and phone.

 *Steps:*
1. Connect your phone using a *data cable*.
2. In CMD or PowerShell:
   bash
   adb devices
   
3. If prompted on your phone, tap *Allow USB debugging*.

 Expected output:

List of devices attached
ABCDEF123456    device


If it shows unauthorized, replug and allow access again.

---

##  STEP 6 — Install AFLogical on the Phone

 *Purpose:* Install the forensic extraction app (APK) onto the Android device.

 *Steps:*
1. Ensure you have the APK file ready:
   
   C:\ForensicLab\aflogical-ose\AFLogical-OSE.apk
   
   (If not present, extract/build from the AFLogical OSE ZIP using Santoku Linux.)

2. In CMD:
   bash
   adb install C:\ForensicLab\aflogical-ose\AFLogical-OSE.apk
   
3. Wait for:
   
   Success
   
  <img width="740" height="101" alt="Screenshot 2025-10-28 124027" src="https://github.com/user-attachments/assets/a1f975e7-78dd-4979-a304-4a73eb16e870" />


 *Verification:* Check your phone — the *AFLogical* app should now appear in your app list.

---

##  STEP 7 — Run AFLogical OSE on the Phone

 *Purpose:* Start the logical data extraction process.

 *Steps:*
1. Open the *AFLogical* app on the device.
2. Grant all requested permissions (Contacts, SMS, Storage).
3. Select which data to extract:
   -  Contacts  
   -  SMS  
   -  Call Logs  
   -  MMS  
   -  Calendar
4. Tap *Start Extraction* or *Create Extract*.
5. Wait until extraction finishes.

 *Default save location:*

/sdcard/aflogical/

or

/storage/emulated/0/aflogical/


 *Verify via ADB:*
bash
adb shell ls /sdcard/aflogical

You should see:

contacts.csv
sms.csv
calllog.csv


---

##  STEP 8 — Copy Extracted Data to Your Computer

 *Purpose:* Pull the extracted forensic data to your analysis workstation.

 *Command:*
bash
adb pull /sdcard/aflogical C:\ForensicLab\output

<img width="685" height="127" alt="Screenshot 2025-10-28 124516" src="https://github.com/user-attachments/assets/011e9f4d-00a5-47e5-b9b5-53e079d7865f" />



 This copies the folder from your phone to:

C:\ForensicLab\output\


Check using:
bash
dir C:\ForensicLab\output


You’ll find files like:

contacts.csv
sms.csv
calllog.csv
mms.csv
calendar.csv

<img width="600" height="280" alt="Screenshot 2025-10-28 124533" src="https://github.com/user-attachments/assets/a777d5b7-8507-47ee-8341-d0172f761d39" />


---

##  (Optional) STEP 9 — Verify Integrity (Hash Values)

To maintain forensic integrity, calculate file hashes.

*Windows (PowerShell):*
powershell
Get-FileHash "C:\Users\knsha\Downloads\ForensicLab\output\20251026.1721\Contacts Phones.csv" -Algorithm SHA256


*Linux/macOS:*
bash
sha256sum ~/ForensicLab/output/contacts.csv



Record the hash in your report.

---

## STEP 10 — Clean Up

*After extraction is complete:*

*Uninstall AFLogical :*
bash
adb uninstall com.viaforensics.android.aflogical


 *Safely disconnect your device.*

---
# Result  
- Successfully connected the *Android device* to the forensic workstation using *ADB*.  
- Installed and executed *AFLogical OSE* on the device for logical data extraction.  
- Extracted essential data — *contacts, **messages, **call logs, and **calendar entries* — and stored them as CSV files.  
- Verified the integrity of extracted data using *SHA-256 hash values*.  
- The experiment demonstrated how *AFLogical OSE* can perform effective logical data acquisition in mobile forensics.
