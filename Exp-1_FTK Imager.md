# Evidence Acquisition Using AccessData FTK Imager  

## Objective
To acquire both volatile and non-volatile memory using **FTK Imager**, ensuring evidence integrity for forensic investigation.

---

## Description
Forensic Toolkit (FTK) Imager is a forensic acquisition tool from AccessData. It can acquire:  
- **Volatile memory (RAM)**  
- **Non-volatile memory (Hard disk / partitions)**  

It supports multiple formats such as **RAW (dd)**, **SMART**, **E01**, and **AFF**. FTK Imager can also be run in a portable mode (from USB) or installed directly on the investigator’s system with a write blocker.

---

## Experiment Steps with Screenshots

### 1. Opening FTK Imager
- Launch the FTK Imager tool.  
- The interface provides options for **memory capture** and **disk imaging**.  

![FTK Imager – Home Interface](https://github.com/user-attachments/assets/6a3fe4d5-7851-499d-8155-3728181ea9bd)

---

### 2. Acquiring Volatile Memory (RAM)
- Navigate to **Capture Memory**.  
- Options are available to include:  
  - **Pagefile.sys** (Windows swap file, may contain valuable data).  
  - **AD1 file** (FTK’s proprietary image format).  

![Capture Memory Option](https://github.com/user-attachments/assets/8dad9b0a-45cb-47d3-8fe3-4cac90b63779)  
![Selecting Memory Capture](https://github.com/user-attachments/assets/b1a03c7a-c550-45f8-9c04-5665f31f5f39)

---

### 3. Acquiring Non-Volatile Memory (Disk Imaging)
- Go to **Create Disk Image**.  
- Choose the source type:  
  - Physical Drive  
  - Logical Drive (partition)  
  - Image file  
  - Folder contents  
  - CD/DVD  

![Disk Image Option](https://github.com/user-attachments/assets/3b5b29c3-5a7a-4e95-b01a-1e74e9978b7e)

---

### 4. Selecting Physical Drive
- Select **Physical Drive** for complete acquisition.  
- The tool lists all available drives; choose the one to be imaged.  

![Select Physical Drive](https://github.com/user-attachments/assets/35ddfe4a-db63-434e-9047-f90166e8ba02)

---

### 5. Entering Case Details
- Provide **case number, examiner’s name, and description**.  
- This metadata is stored within the image file for traceability.  

![Case Details Entry](https://github.com/user-attachments/assets/3eb42dda-d44b-42bf-a9d0-8e1531147954)

---

### 6. Setting Image Destination
- Choose where the image will be saved.  
- Define:  
  - File name  
  - Image fragment size (set to `0` for a single file)  
  - Output format (RAW, SMART, E01, AFF)  

![Image Destination Setup](https://github.com/user-attachments/assets/253a9b5d-e573-450e-afa7-ca9fa3a0f1b7)

---

### 7. Verification Options
- Enable **Verify images after they are created** to confirm integrity.  
- This ensures acquired hash matches source hash.  

![Verification Setup](https://github.com/user-attachments/assets/598eab39-86a2-44f9-92b9-a1d0d6f74fb8)

---

### 8. Starting Acquisition
- Click **Start** to begin imaging.  
- FTK Imager displays progress until acquisition is complete.  

![Start Acquisition](https://github.com/user-attachments/assets/e175fcab-57eb-4cfc-8a54-d8a779425fbd)

---

### 9. Acquisition Results
- Once completed, FTK Imager generates:  
  - The acquired image file  
  - A text report containing acquisition details  
  - Hash values for verification  

![Acquisition Completed](https://github.com/user-attachments/assets/cf75bf5e-1205-487b-a65d-b1f4c4a67458)

---

## Result
Evidence was successfully acquired from both volatile and non-volatile memory using FTK Imager.  
The generated forensic image and verified hash values confirm the **integrity and reliability** of the acquired data.

---

## References
- AccessData FTK Imager User Guide  
- *Digital Forensics Lab – Ex. No. 1 Evidence Acquisition Using FTK Imager*:contentReference[oaicite:1]{index=1}
