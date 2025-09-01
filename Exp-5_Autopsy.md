# 🔍 Digital Forensics Lab – Experiment 5  
**Use Autopsy to Create a Case and Import Evidence**

---

## 📌 Objective
To understand how to use **Autopsy**, an open-source digital forensics tool, for creating a case, importing evidence, and analyzing forensic artifacts.

---

## 📝 Description
Autopsy is an open-source digital forensics platform used for analyzing and extracting data from digital devices.  
In this experiment, we performed the following steps:

1. **Installation** of Autopsy.  
2. **Creating a New Case** with examiner details.  
3. **Adding a Data Source** (evidence image file).  
4. **Configuring Ingest Modules** for automated analysis.  
5. **Performing Analysis** (keyword search, file system, hash lookup, timeline).  
6. **Generating a Report** of findings.  
7. **Closing and Archiving** the case.  

---

## 📂 Steps with Screenshots

### 1️⃣ Opening Autopsy and Creating a Case
- Launch Autopsy → Select **New Case**.  
- Provide case name, location, and examiner details.

![Step 1 – Create Case](https://github.com/user-attachments/assets/b89fa7a1-b593-4be5-a596-5f22a524d953)

---

### 2️⃣ Adding a Data Source
- Choose the type of evidence (disk image, logical files, or local drive).  
- Browse and select the image file (e.g., `.E01` format).

![Step 2 – Add Data Source](https://github.com/user-attachments/assets/aad384dc-5f5f-4553-b652-219baf2dc09c)

---

### 3️⃣ Configuring Ingest Modules
- Enable modules like **File Type Identification, Keyword Search, Hash Lookup, Web Artifacts**.  
- These modules automatically extract forensic artifacts.

![Step 3 – Configure Ingest](https://github.com/user-attachments/assets/e5e58d82-ece7-4cae-a2b5-7899c22a75be)

---

### 4️⃣ Viewing Ingest Progress
- Autopsy begins processing the evidence.  
- Progress is shown in the lower-left corner.  

![Step 4 – Ingest Progress](https://github.com/user-attachments/assets/4a49779c-fef9-4bc9-80e2-0ee74387554d)

---

### 5️⃣ Exploring File System and Artifacts
- Left pane shows a **tree structure**: File System, Web History, Email, etc.  
- Navigate folders, view file details, extract metadata.  

![Step 5 – File System](https://github.com/user-attachments/assets/b05e5536-c1ea-4d3c-a940-123575d430c1)

---

### 6️⃣ Keyword Search
- Use the **Keyword Search** module to search for specific terms.  
- Helps in identifying relevant user activities.  

![Step 6 – Keyword Search](https://github.com/user-attachments/assets/368bf9a6-afae-467a-84bd-206d75ef34e6)

---

### 7️⃣ Timeline Analysis
- Visualize events based on timestamps.  
- Useful to reconstruct user actions in chronological order.  

![Step 7 – Timeline Analysis](https://github.com/user-attachments/assets/7c9eb450-bca8-4966-8eca-5a00c2701783)

---

### 8️⃣ File Hash Analysis
- Autopsy compares file hashes with databases of **known good/bad files**.  
- Helps identify malware or unauthorized files.  

![Step 8 – Hash Analysis](https://github.com/user-attachments/assets/58a3de8d-7747-4b4e-9fc2-21000a0bcd04)

![Step 8 (contd.) – Hash Lookup](https://github.com/user-attachments/assets/0f777a06-e23b-49aa-9fa0-671579ae7362)

---

### 9️⃣ Report Generation
- After analysis, generate reports in **HTML, CSV, or Excel** formats.  
- Export artifacts and findings for documentation.  

![Step 9 – Generate Report](https://github.com/user-attachments/assets/132d31f9-9972-4a2a-80ac-af1ffa60e414)

---

### 🔟 Case Closure
- After completing the investigation:  
  - Close the case in Autopsy.  
  - Archive all reports and evidence safely.  

![Step 10 – Case Closure](https://github.com/user-attachments/assets/7d40290f-c6a3-48ae-961b-62d764783fb0)

---

## ✅ Final Review
This lab demonstrates how Autopsy can be used to:  
- Import and analyze evidence.  
- Perform keyword, timeline, and hash analysis.  
- Generate detailed forensic reports.  

![Final Overview](https://github.com/user-attachments/assets/989efcab-9ac7-43f9-ada2-3c3a14920bab)


## Result

The experiment successfully demonstrated the use of Autopsy for creating a case, importing evidence, analyzing digital artifacts, and generating reports, thereby validating its effectiveness as a digital forensic investigation tool.
  
