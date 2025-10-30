
# 🧩 Digital Forensic Lab Experiments — README

A comprehensive, open-source collection of **10 hands-on digital forensics experiments** for students, instructors, and practitioners.  
Each experiment includes detailed **step-by-step procedures**, required tools, screenshots, and expected outputs so you can conduct realistic, forensically sound lab exercises.

---

## 📚 Table of Contents
- [Overview](#overview)
- [Experiments (1–10)](#experiments-1--10)
- [Tools & Skills](#tools--skills)
- [Getting Started](#getting-started)
- [Prerequisites & Lab Environment](#prerequisites--lab-environment)
- [How to Use This Repo](#how-to-use-this-repo)
- [Contributing](#contributing)
- [License](#license)

---

## 🧭 Overview
This repository organizes **10 modular lab exercises** that guide learners from **basic evidence acquisition** to **advanced malware reverse engineering**.  
Each module includes:
- Learning objectives  
- Required tools/configs  
- Step-by-step execution  
- Sample data and screenshots  
- Output and result interpretation  

These exercises align with the **Digital Forensics Laboratory Course (213CSE4307)** under the *School of Computing, Department of Computer Science & Engineering*.

---

## 🧪 Experiments (1–10)

### **Experiment 1 — Evidence Acquisition (FTK Imager)**
**Objective:** Create forensically sound disk images for legal evidence preservation.  
**Tools:** AccessData FTK Imager  
**Skills:** Disk imaging, hash verification, chain of custody  
**Output:** Forensic image (`.E01` / `.dd`) with verified integrity  

---

### **Experiment 2 — File Recovery (TestDisk & Foremost)**
**Objective:** Recover deleted or damaged files and partitions.  
**Tools:** TestDisk, Foremost  
**Skills:** Partition analysis, file system repair, file recovery  
**Output:** Recovered files and restored partition structures  

---

### **Experiment 3 — Network Traffic Analysis (Wireshark)**
**Objective:** Capture and analyze network communications for investigations.  
**Tools:** Wireshark  
**Skills:** Packet capture (`.pcap`), protocol filtering, traffic inspection  
**Output:** PCAP capture file and investigation report  

---

### **Experiment 4 — Email Header Forensics (MHA)**
**Objective:** Analyze email headers to detect spoofing and trace origin servers.  
**Tools:** Microsoft Message Header Analyzer (MHA) / online analyzer  
**Skills:** Header parsing, authentication verification (SPF, DKIM, DMARC)  
**Output:** Email authenticity/spoofing report  

---

### **Experiment 5 — Case Management & Evidence Analysis (Autopsy)**
**Objective:** Create forensic cases and import disk images or memory captures for analysis.  
**Tools:** Autopsy Digital Forensics Platform  
**Skills:** Case management, artifact extraction, timeline and keyword analysis  
**Output:** Forensic case file with analyzed evidence and exported reports  

---

### **Experiment 6 — File System Analysis (Sleuth Kit)**
**Objective:** Perform low-level file system forensics and create timelines.  
**Tools:** The Sleuth Kit (TSK)  
**Skills:** Deleted file recovery, metadata extraction, inode examination, timeline generation  
**Output:** File listings, recovered files, and activity timeline  

---

### **Experiment 7 — Mobile Forensics (LiME + ADB / AFLogical OSE)**
**Objective:** Extract logical and memory data from Android devices.  
**Tools:** LiME (Linux Memory Extractor), AFLogical OSE, ADB  
**Skills:** Logical extraction, volatile memory capture, artifact verification  
**Output:** Extracted data including SMS, contacts, calls, and memory dumps  

---

### **Experiment 8 — Steganography Detection (zsteg / StegSecret)**
**Objective:** Detect and extract hidden data from image and multimedia files.  
**Tools:** zsteg, StegSecret, StegSolve, steghide, exiftool, binwalk  
**Skills:** Steganalysis, metadata analysis, payload extraction  
**Output:** Extracted hidden payloads or proof of hidden data  

---

### **Experiment 9 — Process Analysis (Procmon / Process Explorer)**
**Objective:** Identify suspicious or malicious processes running on a Windows system.  
**Tools:** Procmon, Process Explorer (Sysinternals), VirusTotal  
**Skills:** Process inspection, DLL tracing, IOC collection, behavioral analysis  
**Output:** Detailed process analysis report and captured Indicators of Compromise (IOCs)  

---

### **Experiment 10 — Malware Reverse Engineering (REMnux / Ghidra)**
**Objective:** Perform static malware analysis and reverse engineer executable code.  
**Tools:** REMnux Linux Distro, Ghidra, binwalk, strings  
**Skills:** Disassembly, decompilation, static binary analysis, signature extraction  
**Output:** Decompiled code, IOC list, and malware behavior summary  

---

## 🧰 Tools & Skills Summary

| Category | Tools | Skills |
|-----------|--------|--------|
| **Disk Imaging & Recovery** | FTK Imager, TestDisk, Foremost | Disk cloning, integrity verification |
| **Network Forensics** | Wireshark | Packet capture, traffic analysis |
| **Email Forensics** | MHA, Email Analyzer | Header tracing, spoofing detection |
| **Case Management** | Autopsy, Sleuth Kit | Artifact extraction, timeline analysis |
| **Mobile Forensics** | LiME, AFLogical OSE, ADB | Logical/Memory extraction |
| **Steganography** | StegSolve, zsteg, StegSecret, exiftool | Hidden data detection |
| **Process & Malware Analysis** | Process Explorer, Procmon, Ghidra, REMnux | Static analysis, reverse engineering |

Completing all experiments builds end-to-end competency in **digital evidence handling**, **network and email forensics**, **mobile extraction**, **steganography**, and **malware analysis**.

---

## 🚀 Getting Started

Open any experiment folder (e.g.,  
`/Experiments/01_FTK_Imager/`)  
and follow its `README.md` for detailed instructions, screenshots, and expected results.

> ⚠️ **Always work on test data or virtual machines** — never use live systems or real evidence without authorization.

---

## 💻 Prerequisites & Lab Environment

| **Requirement** | **Recommended Setup** |
|-----------------|------------------------|
| **RAM** | 8 GB minimum (16 GB preferred) |
| **Disk Space** | 100 GB+ free |
| **Virtualization** | VMware / VirtualBox |
| **Operating Systems** | Windows 10/11, Ubuntu / REMnux |
| **Java Runtime** | Required for Ghidra |
| **Privileges** | Administrator / root access |
| **Ports** | USB (for devices), Ethernet/Wi-Fi (for packet capture) |

---

## 🧩 How to Use This Repo

Each experiment folder contains:
- `README.md` — Instructions for the experiment  
- `assets/` — Screenshots & output images  
- `samples/` — Test data used in the experiment  
- `report_template.docx` — Optional report format  

### 🔄 Recommended Progression

1. **Start with Experiments 1–3** → Fundamentals *(Acquisition, Recovery, Network)*  
2. **Continue with Experiments 4–6** → Core Analysis *(Case, File System, Artifacts)*  
3. **Finish with Experiments 7–10** → Advanced *(Mobile, Stego, Process, Malware)*  

---

## 🤝 Contributing

We welcome contributions from students and professionals!  

1. **Fork** the repository  
2. **Create a new branch** — e.g. `feature/update-lab8`  
3. **Add or improve** experiment documentation or automation scripts  
4. **Test** your changes thoroughly  
5. **Submit a Pull Request** with clear details  

> 💡 You can also suggest new tools, provide screenshots, or help automate data extraction and report generation.

---

## ⚖️ License

This project is licensed under the **MIT License**.  
It is intended solely for **educational and research use**.  
Ensure proper **authorization** before conducting forensic analysis on real devices, systems, or networks.



