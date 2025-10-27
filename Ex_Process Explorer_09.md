# 🧪 Ex.No:9 – Using Process Explorer to Identify Suspicious Processes

---

## 🎯 Aim :
To use Microsoft Sysinternals **Process Explorer** to monitor system activities and identify any **suspicious or malicious processes** running on a Windows computer.

---

## 📖 Overview
**Steg-Expose** is a Java-based detector that applies multiple steganalysis techniques and produces a per-file "suspicion score" (commonly 0.0–1.0).  
A higher score means a stronger indication that the image may contain hidden data. This tool is a *detector* — it does not extract hidden payloads itself. Detected candidates should be analyzed further with extraction/forensic tools.

---

## 🛠️ Requirements :
- Windows operating system  
- Internet connection  
- **Process Explorer** (from Microsoft Sysinternals)  
- Optional: Antivirus software (e.g., Windows Defender, Malwarebytes)

---

## 📖 Description :
Process Explorer is a part of the **Microsoft Sysinternals Suite**. It is a powerful tool used to view detailed information about system processes.  
It helps investigators and administrators analyze active processes, detect suspicious behavior, monitor CPU and memory usage, and verify process authenticity using digital signatures.

---

## 🧠 Procedure :

### 🧩 1. Download and Setup Process Explorer
1. Go to the official Microsoft Sysinternals website:  
   🔗 [https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer)
2. Click **Download Process Explorer**.
3. Extract the downloaded ZIP file to a folder.
4. Right-click `procexp64.exe` (for 64-bit) or `procexp.exe` (for 32-bit) → select **Run as Administrator**.

---

### 🧩 2. Understand the Interface
1. The main window displays all running processes in a **hierarchical tree view**.
2. Each process shows details such as **PID**, **CPU usage**, **memory usage**, and **company name**.
3. Color codes represent process states:
   - 🟩 **Green** — Newly started processes  
   - 🟥 **Red** — Terminated processes  
   - 🟦 **Light Blue** — Processes running under the current user  
   - 🟪 **Pink** — Suspended processes
<img width="2158" height="1737" alt="Screenshot 2025-10-28 001616" src="https://github.com/user-attachments/assets/900dda2e-cf4c-49e4-922c-0fc5d94c3aff" />


---

### 🧩 3. Identify Suspicious Processes
1. Look for **unfamiliar or oddly named processes** (e.g., `xkdjeo.exe`, `randomname123.exe`).
2. Check the **Company Name** and **Description**:
   - Legitimate software usually shows known publishers like *Microsoft*, *Intel*, or *Adobe*.
3. Right-click the process → **Properties** → go to the **Image** tab.
4. Verify the **Path** of the executable file:
   - ✅ Safe: `C:\Windows\System32\`
   - ⚠️ Suspicious: `C:\Users\<User>\AppData\Temp\` or `Downloads\`
5. Check for **Digital Signature**:
   - Valid signature = trusted developer  
   - No signature or invalid = possibly malicious
<img width="2158" height="1737" alt="Screenshot 2025-10-28 001616" src="https://github.com/user-attachments/assets/49fa868f-93d2-4e66-a919-beb205d177b1" />

---

### 🧩 4. Analyze Process Behavior
1. Observe **CPU**, **Memory**, and **I/O usage** columns.
2. If a small or unknown process consumes **excessive CPU or memory**, it may be malicious.
3. Right-click the process → **Properties** → go to the **TCP/IP tab**.
   - Check if it communicates with **unknown external IP addresses**.
4. Examine **Handles** and **DLLs** tabs for suspicious loaded files or libraries.

<img width="2462" height="1790" alt="Screenshot 2025-10-28 002548" src="https://github.com/user-attachments/assets/744a2791-678b-4c69-8be7-b62b52dfbb51" />

---

### 🧩 5. Verify Process Legitimacy
1. Search the process name on Google.  
   Example: `svchost.exe` vs `svhost.exe` (one letter missing — suspicious).
2. Visit 🔗 [https://www.virustotal.com](https://www.virustotal.com)
   - Upload the process file or search its name to verify if it’s reported as malware.
3. Cross-check with **ProcessLibrary.com** or official vendor websites for authenticity.
 
<img width="2800" height="1474" alt="Screenshot 2025-10-28 002805" src="https://github.com/user-attachments/assets/d8143515-8092-426d-9183-b3102437ba3e" />


---

### 🧩 6. Take Appropriate Action
1. **If the process is confirmed malicious:**
   - Right-click the process → **Kill Process** to stop it.
   - Delete the corresponding executable file from its path.
2. **If unsure:**
   - Right-click → **Suspend Process** to stop it temporarily for investigation.
3. **After removal:**
   - Run a **Full System Scan** using Windows Defender or Malwarebytes to ensure no remnants remain.

<img width="2302" height="984" alt="Screenshot 2025-10-28 003041" src="https://github.com/user-attachments/assets/9c3ad238-d8d6-4e42-b1d4-b5d7125674ff" />


---

### 🧩 7. Example Observation
You find `faangpath_simple_template.pdf` consuming 70% CPU.  
- **Path:** `C:\Users\Admin\AppData\Temp\faangpath_simple_template.pdf`  
- **Digital Signature:** None  
- **Company Name:** Unknown  
- **Network Activity:** Shows connections to unknown IPs in the TCP/IP tab  
- **Online Check:** VirusTotal confirms it as a **known trojan**  
- **Action Taken:** Suspended → Killed → Deleted file → Performed full antivirus scan  

<img width="2879" height="1781" alt="Screenshot 2025-10-28 003234" src="https://github.com/user-attachments/assets/03c984f8-2dcf-4532-854f-6648c5742b53" />



---


## 🧾 **Result**
Using Process Explorer, suspicious processes were successfully identified by examining their **CPU usage**, **path**, **digital signature**, and **network activity**.  
Confirmed malicious processes were terminated and removed to maintain system integrity.

---

## ✅ **Conclusion**
Process Explorer is an essential forensic tool that provides in-depth visibility into running processes.  
It enables forensic investigators and system administrators to **detect, analyze, and remove suspicious or malicious programs** efficiently.

---

## ⚠️ Notes

Always cross-check results with VirusTotal and other analysis tools.
Do not terminate system-critical processes without full verification.
Keep Process Explorer updated to ensure accurate VirusTotal integration.
Always run investigations in a controlled forensic environment.

---

## 📚 References

Microsoft Sysinternals: Process Explorer Official Page
NIST SP 800-83: Guide to Malware Incident Prevention and Handling
SANS DFIR Process Analysis Guide
VirusTotal Documentation

---

## ✅ Final Outcome

A suspicious process was detected and analyzed using Process Explorer.
The process exhibited anomalous behavior and failed digital signature verification.
After documentation and hash verification, the process was safely terminated — confirming the successful use of Process Explorer for forensic process analysis.

📁 Evidence Folder: D:\Case_08_ProcessExplorer\
🔐 Hash Verification: Completed
🧾 Report: Case_08_ProcessExplorer_Report.pdf

---
