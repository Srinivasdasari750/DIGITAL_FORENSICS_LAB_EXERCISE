# Ex.No.1    FTK Imager: A Forensic Imaging Tool Overview
## 🎯 Aim  
To learn and perform forensic acquisition of digital evidence using **FTK Imager Toolkit**, and to understand how to create, verify, and analyze forensic images step by step.  

## 📖 Description  
FTK Imager is a forensic imaging tool that allows investigators to create exact copies of digital storage devices or files without altering the original evidence. It helps in capturing forensic images, verifying their integrity through hash values, and previewing file systems. The tool is widely used in digital forensics for evidence acquisition and preliminary analysis.  

## 🛠️ Tools Required  
-  A computer with **FTK Imager** installed  
-  Sample storage media / disk image for testing  
-  External storage device (to save the acquired image)  
-  Screenshots captured during each step of the process  

## 📝 Procedure

 Acquiring Volatile Memory (RAM) Using FTK Imager
<br>


### Steps to Capture RAM Using FTK Imager
<br>

### 1. Run as Administrator
- Open **FTK Imager** with administrative privileges.  
- Right-click the FTK Imager icon and select **Run as administrator**.
<br>
<br>

![WhatsApp Image 2025-09-01 at 23 09 37_276754fb](https://github.com/user-attachments/assets/461b61d9-d59d-4bc1-a6e0-dc04d7eb33d8)

<br>
<br>

### 2. Initiate Memory Capture
- In the top menu bar, click **File → Capture Memory...** from the dropdown list.
  <br>
<br>

<img width="1919" height="1079" alt="1" src="<img width="2349" height="1509" alt="Screenshot 2025-09-01 231317" src="https://github.com/user-attachments/assets/767aee87-2f29-4905-aaf1-7fb1af40004b" />


<br>
<br>

### 3. Configure Destination
A dialog box will appear where you configure where and how the memory will be saved.

- **Destination Path:**  
  Click **Browse** to select a folder on an **external drive** (not the system drive).  

- **Destination Filename:**  
  You can keep the default `memdump.mem` or assign a more descriptive name.

- **Optional: Include pagefile.sys**  
  Check this box to capture `pagefile.sys`, which is virtual memory stored on the disk.  
  > Note: This may increase capture size and duration, but can contain valuable artifacts.

- **Optional: Create AD1 file**  
  Saves the memory dump in an AccessData-specific container file.  
  > Generally not necessary if using tools like **Volatility** for analysis.



<br>
<br>

<img width="1919" height="1079" alt="2" src=<img width="2382" height="1558" alt="Screenshot 2025-09-01 231901" src="https://github.com/user-attachments/assets/0eaceeec-1fe6-45ea-a423-9d6febfb3bff" />
 
 
<br>
<br>

### 4. Start Capture
- Click the **Capture Memory** button to begin acquisition.
<br>
<br>


<img width="1919" height="1079" alt="3" src="<img width="2234" height="1525" alt="Screenshot 2025-09-01 223335" src="https://github.com/user-attachments/assets/1eab66d3-f79f-4875-a5d6-6dd14f6a1d26" />

<br>
<br>

### 5. Wait for Completion
- A progress bar will indicate the capture status.  
- Capture time depends on the system’s RAM size.  
- Once finished, the memory dump file will be available in the destination folder.
---
<br>
<br>

## Acquiring Non-Volatile Memory (Disk Image) Using FTK Imager


### 1. Start the Process
- In FTK Imager, go to the top menu bar: **File → Create Disk Image...**.

<br>
<br>
<img width="1919" height="1016"src="https://github.com/user-attachments/assets/df90df51-2328-4ac7-b6db-870e4860793e" />


<br>
<br>

### 2. Select Source Evidence Type
A window will appear asking you to choose the source type:

- **Physical Drive:** Images the entire disk, including all partitions, unallocated space, and the Master Boot Record (MBR).  
- **Logical Drive:** Images a specific partition (e.g., C: drive).  
- **Image File:** Converts or copies an existing image file.  
- **Contents of a Folder:** Creates an image of a specific folder only.  

> **Tip:** For full forensic imaging, select **Physical Drive**.
<br>
<br>
<p align="center">

<img width="1089" height="735" alt="image" src=<img width="2376" height="1565" alt="Screenshot 2025-09-01 222758" src="https://github.com/user-attachments/assets/f633bd04-032a-479d-a448-35f22b039c64" />

</p>
<br>
<br>

### 3. Select the Source Drive
- From the dropdown, choose the physical drive to image (connected via **write-blocker**).  
- Click **Finish**.
 <br>
<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/45090b51-f21e-4861-8a5e-98b7fdbbd41a" />


</p>
<br>
<br>

### 4. Configure the Image Destination
- Click **Add...** in the "Create Image" window to define the image **format** and **destination**.
  <br>
<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/c85f6645-1ac5-4d91-a9a5-4b888508130b" />


<br>

#### Options:

- **Image Type:**  
  - **E01 (EnCase Format):** Recommended; includes compression, metadata, and error-checking.  
  - **Raw (DD):** Bit-for-bit copy with no extra features.
<br>
<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/a751093f-8ba3-4e16-9e3a-a1f1ecb7e940" />


</p>
<br>
<br>

- **Fill in Evidence Item Information:**  
  - Enter case details, examiner name, and description.  
  - This information is stored in the image metadata (important for documentation).
 <p align="center">
<img width="1919" height="1079" alt="6" src="https://github.com/user-attachments/assets/b54228ea-2d2f-4fad-a6e2-308031b09c27" />

</p>
<br>
<br>

- **Choose Destination Folder:**  
  - Must be a different drive from the source.  
  - Name the image file (e.g., `Case001_SuspectHDD`).  

- **Image Fragment Size:**  
  - Set a value to split the image into multiple parts.  
  - Set to `0` for a single image file.
  <br>
  <br>
  
<p align="center">
<img width="1919" height="1079" alt="7" src="https://github.com/user-attachments/assets/1e70219b-98ae-48d8-a922-05835baad8e9" />
</p>
<br>
<br>


### 5. Start the Imaging Process
- Click **Finish** to return to the "Create Image" screen.  
- **Check "Verify images after they are created"** to calculate hash values and ensure integrity.  
- Click **Start**.
  <br>
  <br>
  <p align="center">
<img width="1919" height="1079" alt="8" src="https://github.com/user-attachments/assets/3228c063-a78c-45cd-8789-6cc1e7608b6f" />

<img width="1919" height="1079" alt="9" src="https://github.com/user-attachments/assets/9538bd4f-c6ea-48b3-b46f-21d2eacd7979" />

</p>
<br>
<br>

### 6. Completion and Hash Verification
- The imaging process may take time depending on the drive size.  
- After completion, FTK Imager verifies the hashes automatically.  
- A final window shows **MD5** and **SHA1** hashes for both the source drive and image.  
- Matching hashes confirm the forensic image’s integrity.

---
## Notes

- Always use a **write-blocker** to prevent modifications to the evidence.  
- **Hash verification** is critical to maintain a chain of custody and admissibility in court.  
- **Image Fragmentation** is useful for large drives or storage limitations.
---

## References

- [FTK Imager Official Website](https://accessdata.com/product-download/ftk-imager-version-4-5)  
- FTK Imager Documentation

## Result  
Successfully created a forensic image using FTK Imager, verified its integrity through hashing, and previewed the acquired evidence without altering the original data. This demonstrates the correct procedure for forensic acquisition using FTK Imager Toolkit.  
