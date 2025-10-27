# 🧪 Ex-6.No. — Sleuth Kit: Analyzing Digital Evidence Using Command-Line Tools  

## 🎯 Aim  
To learn and perform **digital evidence analysis using the Sleuth Kit (TSK)** by examining disk images, identifying partitions, recovering deleted data, and analyzing file system metadata through forensic investigation steps.

---

## 📖 Description  
**The Sleuth Kit (TSK)** is an open-source forensic toolkit that provides a set of command-line tools used for investigating and analyzing digital storage media.  
It helps investigators identify partitions, analyze file systems, recover deleted files, and extract metadata such as file timestamps and ownership details.  

TSK supports various file systems including **FAT, NTFS, EXT, HFS, and exFAT**.  
It can work as a standalone toolkit or as the backend engine for the **Autopsy** forensic platform.  

---

## 🛠️ Tools Required  
- **The Sleuth Kit (TSK)** installed on your system  
- A forensic image file (`.E01`, `.dd`, `.raw`)  
- A system terminal or command prompt  
- Text editor for report writing  
- (Optional) **FTK Imager** to create forensic images  
- Screenshots for each step  

---

## 📝 Procedure  

### 🧩 Part 1 — Preparing and Verifying the Evidence  
1. Open the forensic image file in The Sleuth Kit environment.  
2. Verify the hash value of the image (MD5 or SHA1) to ensure authenticity.  
3. Check the disk structure and identify all existing partitions and file systems.  
4. Record the partition offsets, sizes, and types for documentation.  

   ![Screenshot — Partition Table](https://github.com/user-attachments/assets/example_mmls_output.png)

---

### 🧩 Part 2 — File System Analysis  
1. Access the selected partition based on the recorded offset information.  
2. Examine the file structure to view directories and files stored in the partition.  
3. Review the file attributes such as size, type, creation time, and modification time.  
4. Analyze metadata information of critical or suspicious files for investigation.  

   ![Screenshot — File System Analysis](https://github.com/user-attachments/assets/example_fls_output.png)

---

### 🧩 Part 3 — Deleted File Recovery  
1. Search for and identify files that have been deleted but still exist in the file system.  
2. Recover selected deleted files to a secure folder for further examination.  
3. Validate the integrity of the recovered files by comparing their hash values.  
4. Document the recovered file names, locations, and evidence significance.  

   ![Screenshot — File Recovery](https://github.com/user-attachments/assets/example_recovery_output.png)

---

### 🧩 Part 4 — Timeline and Activity Analysis  
1. Collect all file system activity data such as creation, access, and modification times.  
2. Generate a timeline to visualize user actions and file events in chronological order.  
3. Review the timeline for unusual activity such as rapid deletions or file access patterns.  
4. Record findings and observations that are relevant to the case.  

   ![Screenshot — Timeline Report](https://github.com/user-attachments/assets/example_timeline_output.png)

---

### 🧩 Part 5 — Reporting and Documentation  
1. Compile all evidence findings including partition data, recovered files, and activity timelines.  
2. Summarize the forensic process and tools used during the analysis.  
3. Include screenshots, metadata summaries, and hash verification details.  
4. Prepare a final forensic report in a readable format such as PDF or HTML.  

---

## 📄 Notes  
- Always perform analysis on a **forensic copy**, not the original evidence.  
- Verify and record **hash values** before and after the investigation.  
- Maintain a complete **chain of custody** for all forensic actions.  
- The main tools used from Sleuth Kit include disk structure analysis, metadata extraction, file recovery, and timeline generation.  

---

## 📚 References  
- [The Sleuth Kit Official Documentation](https://sleuthkit.org/sleuthkit/docs.php)  
- Carrier, B. (2005). *File System Forensic Analysis*. Addison-Wesley.  
- [Autopsy & Sleuth Kit GitHub Repository](https://github.com/sleuthkit/sleuthkit)  

---

## 🧾 Result  
Successfully analyzed digital evidence using **The Sleuth Kit (TSK)**.  
Partitions were identified, file systems examined, deleted data recovered, and a forensic timeline was created.  
The experiment demonstrates the complete process of evidence analysis and reporting using Sleuth Kit.
