#  Ex.No.2    TestDisk: Open-Source Data Recovery Tool

## Aim :
To use TestDisk step by step to recover a missing partition and repair a corrupted one
  

### 1. Log Creation & Disk Detection  
When TestDisk starts, it creates a log file.  
All connected hard drives are detected and listed with their correct size.  
 Use the arrow keys to select the drive with the lost partition.  

<p align="center">
<img width="1920" height="950" alt="Screenshot 2025-08-31 214747" src="https://github.com/user-attachments/assets/ef6d048a-6a4b-450c-82e5-95d3afe03716" />
</p>  

---

### 2. Partition Table Type Selection  
TestDisk auto-detects the *partition table type*.  
- Usually, the default value is correct.  
- Press *Enter* to proceed.  

<p align="center">
<img width="1859" height="1000" alt="Screenshot 2025-08-31 214908" src="https://github.com/user-attachments/assets/c130be5d-1ce9-4b0a-8863-412b804798e9" />
</p>  

---

### 3. Analyse Current Partition Structure  
Choose *Analyse* → TestDisk displays the current partition structure.  
- The first partition is listed twice → indicates corruption.  
- “Invalid NTFS boot” → faulty NTFS boot sector.  
- One logical partition is missing.  

Press *Quick Search* to continue.  

<p align="center">
<img width="1920" height="1080" alt="Screenshot 2025-08-31 214948" src="https://github.com/user-attachments/assets/54bd041c-3d05-421e-9c3e-6cfd2949869f" />
</p>  

---

### 4. Quick Search for Partitions  
Quick Search begins and TestDisk lists results in real-time.  
- Missing logical partition (Partition 3) is detected.  
- Press *p* to list files inside the partition.  
- Files in *red* are deleted entries.  

<p align="center">
<img width="1920" height="1080" alt="Screenshot 2025-08-31 215009" src="https://github.com/user-attachments/assets/0a604987-ae1f-4889-a02e-6ef1d9fcb051" />
</p>  

---

### 5. Deeper Search (If Needed)  
If a partition is still missing → run *Deeper Search*.  
- TestDisk scans cylinder by cylinder.  
- It can detect FAT32, NTFS, ext2/ext3 backup boot sectors.  
- Some partitions may appear as *D (Deleted)* and overlap.  
- Use *p* to preview files in each partition to decide which is correct.  

<p align="center">
<img width="1920" height="1080" alt="Screenshot 2025-08-31 215026" src="https://github.com/user-attachments/assets/a7540d80-701a-4eda-9bb9-a8079983b8f3" />
</p>  

 If files are visible → mark the correct partition as *L (Logical)* or *P (Primary)*.  

---

### 6. Partition Table Recovery  
Once the correct partitions are identified:  
- Go to *Write* → Save the partition table.  
- Confirm with *Enter → Y → OK*.  
- TestDisk updates the partition structure.  

<p align="center">
<img width="1920" height="1080" alt="Screenshot 2025-08-31 215117" src="https://github.com/user-attachments/assets/43c90dce-b179-4f19-8397-2b5594e4b8f5" />
</p>  

---

### 7. NTFS Boot Sector Recovery  
If the NTFS boot sector is damaged but the backup is valid:  
- Choose *Backup BS* → copy backup boot sector over the corrupted one.  
- Now both boot sector and backup are identical → filesystem recovered.  

<p align="center">
<img width="1730" height="961" alt="Screenshot 2025-08-31 215130" src="https://github.com/user-attachments/assets/b7c9acf0-c622-4eff-824d-29b67f5369a9" />
</p>  

## Result :

The experiment successfully demonstrated the recovery of deleted or damaged files using TestDisk.
Lost partitions were detected and restored.
Corrupted NTFS boot sector was repaired using the backup.
File system was made accessible again after partition table recovery.
Hence, recovery of lost data from a storage device was achieved.
