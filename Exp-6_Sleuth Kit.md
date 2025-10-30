## **Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit** ##

**Overview**

The **Sleuth Kit (TSK)**  is a versatile suite of command-line tools used in **digital forensics**.  
It enables investigators to analyze disk images , uncover deleted files , and extract critical digital evidence  from storage devices.  
This document walks through the complete process of using Sleuth Kit on a **Windows** system to perform forensic analysis.

---

##  **Step 1: Installing Sleuth Kit**

1. **Download the Tool:**  
   - Head over to the official Sleuth Kit page or use this link:  
     👉 [Download Sleuth Kit](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v)  
   - Choose the latest stable **Windows-compatible** version.

2. **Installation Process:**  
   - Run the installer and follow the setup wizard .  
   - Once done, TSK will be ready to use on your system!

---

 **Step 2: Acquire the Disk Image**

Before analysis, a **forensic disk image** (a perfect bit-by-bit copy) of the device is needed.

1. **Create Disk Image:**  
   - Use tools like **FTK Imager**  or **`dd`** to create an exact copy.  
   - Save it in a TSK-supported format: `.dd`, `.raw`, `.img`, or `.E01`.

2. **Sample Evidence Files:**  
   - For this lab, download the following from the provided link:  
      `4Dell Latitude CPi.E01`  
      `4Dell Latitude CPi.E02`

---

##  **Step 3: Mounting the Disk Image (Optional)**

Mounting lets you access the disk image as if it were a normal drive.

- Use **OSFMount**  to mount the image in **read-only mode**.  
-  *Note: This is optional but helps when browsing the file system.*

---

##  **Step 4: File System Analysis with TSK**

Now let’s dive into Sleuth Kit tools  to inspect the file system.

###  Navigate to the TSK Directory

```bash
cd C:\Program Files (x86)\sleuthkit-4.14.0-win32\sleuthkit-4.14.0-win32\bin
```
 <img width="1110" height="626" alt="Screenshot 2025-10-27 192700" src="https://github.com/user-attachments/assets/f418dc0b-8624-4b00-99d6-83b81e539760" />



---

###  Identify File System Type

```bash
.\fsstat.exe -o 63 "C:\Users\madhi\Downloads\4Dell Latitude CPi.E01"
```

 *Displays key details about the file system type and structure.*
 

---

###  View Partition Layout

```bash
.\mmls.exe "C:\Users\madhi\Downloads\4Dell Latitude CPi.E01"

```


<img width="1365" height="767" alt="Screenshot 2025-10-27 192904" src="https://github.com/user-attachments/assets/7e2d5202-8f77-4476-959e-cc09371a50b4" />

 *Lists all partitions and their respective start/end addresses.*

---

###  List Files and Directories

```bash
.\fls.exe -o 63 "C:\Users\madhi\Downloads\4Dell Latitude CPi.E01"

```
 
<img width="1344" height="642" alt="Screenshot 2025-10-27 193012" src="https://github.com/user-attachments/assets/d0f4cc04-ebfa-4103-9366-d28bc90125cb" />



 *Recursively lists files and folders with their inode details.*
 
<img width="1365" height="719" alt="Screenshot 2025-10-27 193057" src="https://github.com/user-attachments/assets/d15705ef-7d22-484f-8898-1d15ad1331aa" />

---

###  Recover Deleted Files

```bash
.\icat.exe -o 63 "C:\Users\madhi\Downloads\4Dell Latitude CPi.E01" 119 > "C:\Users\madhi\Downloads\BOOTLOG_recovered.TXT"
```
  
<img width="1365" height="731" alt="Screenshot 2025-10-27 193241" src="https://github.com/user-attachments/assets/ec7fdaf7-45dc-4bdd-b483-de11db3387ac" />


 *Recovers a deleted or existing file by its inode number.*

---

## **Step 5: Metadata Analysis**

To uncover file history and access details, view the file’s metadata.

```bash
.\istat.exe -o 63 "C:\Users\madhi\Downloads\4Dell Latitude CPi.E01" 119 > "C:\Users\madhi\Downloads\BOOTLOG_metadata.txt" 
```

 *Displays file attributes such as MAC times (Modified, Accessed, Changed), size, and allocation info.*

---


##  **Step 6: Report Generation**

After completing your analysis:

1. **Compile All Outputs:**  
   Collect files like `filesystem_info.txt`, `partitions.txt`, `file_list.txt`, and `timeline.txt`.

2. **Interpret and Document:**  
   Write a clear summary  explaining your findings, methods used, and any key recovered evidence.

<img width="1355" height="671" alt="Screenshot 2025-10-27 193229" src="https://github.com/user-attachments/assets/5eb5bd9c-9247-42d5-8581-cc7891fb15a7" />

--- 

##  **Step 7: Evidence Preservation**

Ensuring the integrity of evidence is the final and most important step.

1. **Archive Evidence Securely:**  
   Use encryption  and hashing  to store your disk image and findings.

2. **Maintain Chain of Custody:**  
   Keep the evidence in a secure location following proper forensic protocols .

---

##  **Conclusion**

Using the **Sleuth Kit (TSK)**, investigators can efficiently extract, analyze, and preserve digital evidence .  
It remains one of the most reliable and open-source forensic toolkits for digital investigation .
