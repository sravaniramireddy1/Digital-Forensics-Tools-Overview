
# **Experiment No. 9 — Using Process Explorer to Identify Suspicious Processes**

**💻 Course:** Digital Forensics Lab
**🧰 Tool Used:** Process Explorer (Microsoft Sysinternals)
**🪟 Platform:** Windows

---

## 🎯 **Aim**

To use the **Process Explorer** tool to observe all running system processes and identify any **suspicious or malicious activities** in the Windows environment.

---

## 🧾 **Requirements**

* 🖥️ Windows operating system
* 🌐 Internet connection
* ⚙️ Process Explorer software
* 🛡️ Antivirus software (optional)

---

## 📘 **Description**

Process Explorer is a system monitoring tool developed by Microsoft Sysinternals.
It provides detailed information about each running process such as process ID, CPU usage, memory usage, file path, and digital signature.
It helps in detecting **unknown, harmful, or hidden processes** that may compromise system security.

---

## 🪜 **Procedure**

### 🔹 Step 1: Download and Launch Process Explorer

1. Open the official Microsoft Sysinternals website.
2. Download and extract the **Process Explorer** ZIP file.
3. Run **procexp64.exe** with **Administrator privileges**.

---

### 🔹 Step 2: Observe the Interface

* The window displays all running processes in a **tree structure**.
* Each process shows information like **PID**, **CPU**, **Memory**, and **Company Name**.
* Color codes indicate the process status:
  🟩 Green – newly started process
  🟥 Red – terminated process
  🟦 Blue – user process
  🟪 Pink – suspended process
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/91dbbaa6-32ba-422c-8e8d-80729a1e1889" />

---

### 🔹 Step 3: Identify Suspicious Processes

* Check for **unfamiliar or random process names** (e.g., `abc123.exe`).
* Observe if the **Company Name** or **Description** field is blank.
* Right-click the process → **Properties → Image tab**.
* Verify the **file path**:

  * ✅ Safe: `C:\Windows\System32\`
  * ⚠️ Suspicious: `Downloads`, `Temp`, or `AppData` folders
* Check for a **digital signature** to ensure authenticity.
<img width="1033" height="708" alt="image" src="https://github.com/user-attachments/assets/ba71fe0f-0ce5-423a-bfad-02491c1d47a7" />

---

### 🔹 Step 4: Analyze Process Behavior

* Monitor **CPU**, **Memory**, and **I/O usage** of each process.
* Suspicious processes often use high resources continuously.
* Open the **TCP/IP tab** to check for unknown network connections.
* Examine the **Handles** and **DLLs** tabs for unusual files or libraries.
<img width="1033" height="708" alt="image" src="https://github.com/user-attachments/assets/109ffe8a-d819-49c0-bc54-eb2207afbeaf" />

---

### 🔹 Step 5: Verify Process Legitimacy

* Search the process name online to confirm its origin.
* Use 🔗 [VirusTotal.com](https://www.virustotal.com) to check if the file is reported as malware.
* Refer to **ProcessLibrary.com** or official vendor websites for more details.

---

### 🔹 Step 6: Take Appropriate Action

* 🚫 For malicious processes:

  * Right-click → **Kill Process** to terminate.
  * Delete the related executable file.
* ⏸️ For unknown processes:

  * Use **Suspend Process** to pause for analysis.
* 🧹 After completion:

  * Run a **full antivirus scan** to clean any remaining threats.
  <img width="728" height="607" alt="image" src="https://github.com/user-attachments/assets/cb4e8739-259c-41cf-9eee-3631e21ae148" />

---

### 🔹 Step 7: Example Observation

A process named `updatefile.exe` was found using 70% CPU.

* Path: `C:\Users\Admin\AppData\Temp\updatefile.exe`
* No digital signature and unknown publisher
* VirusTotal result: Detected as malware

✅ The process was suspended, terminated, deleted, and a full system scan was performed.
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/7bff7d02-c324-47bd-a125-568974b9f174" />

---

## ✅ **Result**

Process Explorer was successfully used to detect, analyze, and remove suspicious processes.
By checking CPU usage, process paths, and digital signatures, malicious activities were identified and eliminated.
System security was effectively maintained through continuous process monitoring.

---

## 📝 **Notes**

* Always run Process Explorer as **Administrator** for full access.
* Some legitimate processes may look suspicious; always verify before deleting.
* Regular process monitoring improves system safety.
* Keep antivirus and Windows updates regularly installed.
* Avoid terminating essential system processes.

---

## 💡 **Conclusion**

Process Explorer is an effective forensic tool for identifying and analyzing hidden or suspicious system processes.
It provides valuable insights into resource usage, file paths, and network activity, helping to maintain system stability and security.
