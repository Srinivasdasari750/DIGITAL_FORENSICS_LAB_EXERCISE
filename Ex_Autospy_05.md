# 🧪 Ex-5.No. — Autopsy: Creating a Forensic Case and Importing Evidence  

## 🎯 Aim  
To learn and perform the process of **creating a forensic case and importing evidence** using the **Autopsy Digital Forensics Tool**, and to understand how to analyze digital evidence through ingest modules and generate forensic reports.  

---

## 📖 Description  
**Autopsy** is an open-source digital forensic platform used for hard drive and smartphone investigations.  
It helps investigators analyze file systems, recover deleted files, and extract artifacts such as browser history, emails, and registry data.  
The tool supports evidence sources like disk images (`.E01`, `.dd`, `.raw`), local drives, and logical folders.  

This experiment demonstrates how to create a case, add evidence, perform analysis, and generate a report using Autopsy.  

---

## 🛠️ Tools Required  
- A computer with **Autopsy** installed  
- Sample **forensic image** (e.g., `.E01`, `.dd`, `.raw`)  
- External storage or folder to save reports  
- Screenshots captured during each step  
- (Optional) **FTK Imager** for creating the forensic image  

---

## 📝 Procedure  

### 🧩 Part 1 — Creating a New Case  

1. **Open Autopsy**  
   - Launch the **Autopsy** tool from the start menu or desktop shortcut.  

2. **Create a New Case**  
   - Click **Create New Case** on the welcome screen.  
   - Fill in:
     - Case Name: `Case_01`
     - Base Directory: Choose a folder for storing case data
     - Examiner Name: Your name
     - Case Number / Description: Brief details about the case  
   - Click **Finish** to create the case.  

   <img width="2704" height="1645" alt="Screenshot 2025-10-27 173323" src="https://github.com/user-attachments/assets/432986aa-58af-448c-b174-c5d100dc99eb" />


---

### 🧩 Part 2 — Adding a Data Source (Importing Evidence)  

1. Click **Add Data Source** after creating the case.  
2. Choose the evidence type:
   - **Disk Image or VM File** — `.E01`, `.dd`, `.raw`, `.vmdk`
   - **Local Disk** — connected drives
   - **Logical Files** — selected folders  
   > For full forensic analysis, select **Disk Image or VM File**.  

   <img width="2853" height="1761" alt="Screenshot 2025-10-27 191450" src="https://github.com/user-attachments/assets/7db1129f-257d-47cf-865d-b7b697755dae" />


3. **Browse to Image File**  
   - Locate and select your forensic image.  
   - Click **Next**.  

4. **Verify Hash Values**  
   - Autopsy automatically computes MD5/SHA1 hashes.  
   - Verify that they match the original hash values recorded during acquisition.  

5.  **Fit** for clarity and documentation.  

---

### 🧩 Part 3 — Selecting Ingest Modules  

1. When prompted, select the ingest modules to run:  
   - File Type Identification  
   - Recent Activity  
   - Web Artifacts (Browser Data)  
   - Keyword Search  
   - Deleted Files / File Carving  
   - Hash Lookup  
   - EXIF Metadata  
   - Registry Analysis  

2. Click **Next → Finish** to begin evidence ingestion.  

   <img width="2796" height="1738" alt="Screenshot 2025-10-27 192243" src="https://github.com/user-attachments/assets/f9b4251f-6772-4238-b032-dda9248c09db" />


3. Wait for the ingest process to complete. Progress is shown at the bottom panel.  

---

### 🧩 Part 4 — Analyzing the Evidence  

1. **Browse File System**  
   - Navigate through directories to inspect user data and files.  

2. **Timeline View**  
   - Click **Timeline** to visualize events (file creation, modification, deletion).  

3. **Artifact Analysis**  
   - Check **Extracted Content → Web History, Emails, Images**, etc.  

4. **Keyword Search**  
   - Use the **Keyword Search** tab to find terms, file names, or IP addresses.  

5. **Tag Important Files**  
   - Right-click any suspicious file → **Tag and Comment** for future reporting.  

---

### 🧩 Part 5 — Generating a Report  

1. After analysis, click **Generate Report**.  
2. Choose report format:
   - **HTML**
   - **PDF**
   - **Excel (CSV)**  
3. Select the data to include (tags, artifacts, keyword hits).  
4. Click **Finish** to generate and save the report in the case directory.  

   <img width="2858" height="1792" alt="Screenshot 2025-10-27 193957" src="https://github.com/user-attachments/assets/42652507-0042-4014-aa4c-7f6249f5acc4" />


---

## 📄 Notes  

- Always work on **forensic copies**, not the original evidence.  
- **Hash verification** ensures integrity and admissibility in court.  
- Maintain a **chain of custody** for every step.  
- Reports must include:
  - Examiner name  
  - Case details  
  - Timestamps  
  - Hash verification results  

---

## 📚 References  

- [Autopsy Official Website](https://www.autopsy.com)  
- [Autopsy User Documentation](https://sleuthkit.org/autopsy/docs/)  
- Carrier, B. (2005). *File System Forensic Analysis*. Addison-Wesley.  

---

## 🧾 Result  

Successfully created a new forensic case in **Autopsy**, imported digital evidence, executed ingest modules for artifact extraction, and generated a detailed forensic report — demonstrating a complete digital forensic workflow using Autopsy.  
