# 🧪 Ex.No.8:# Steg-Expose: Detecting Hidden Data in Images

---

## 🎯 Aim
Use **Steg-Expose** to scan a folder of images for signs of steganography (hidden data), generate a report, and perform follow-up checks on suspicious files.

---

## 📖 Description :
**StegExpose** is a specialized tool used for **steganography analysis**. It works by evaluating the **statistical properties** of an image to estimate the probability of hidden data being embedded within it. This process helps forensic investigators detect steganography techniques like Least Significant Bit (LSB) embedding.

---

## 🛠️ Tools & Requirements
- Java Runtime Environment (JRE) — `java` on PATH  
- Steg-Expose JAR (download from the project release page)  
- A folder of images to test (e.g. `images/`)  
- Utilities for follow-up analysis (recommended):
  - `strings`, `binwalk`, `exiftool`
  - `zsteg` (for PNG), `steghide` (for JPEG/GIF), `foremost`/`scalpel` (file carving)
  - `xxd` / `hexdump` for low-level inspection
    
---

## 🧠 **Procedure :

### 🧩 1. Download and Set Up StegExpose

1.  **Download the tool:** Obtain the `StegExpose.jar` file from the GitHub repository.
2.  **Install Java:** Ensure JRE is installed on your machine.
3.  **Prepare environment:** Place the `StegExpose.jar` file in a dedicated working folder.

<img width="2348" height="1529" alt="Screenshot 2025-10-27 233550" src="https://github.com/user-attachments/assets/916f95bf-7189-4acb-b0e4-7e648823329b" />

---

### 🧩 2. Select Images for Analysis

* Collect the images you suspect might contain hidden data.
* StegExpose supports common image formats such as **.png**, **.jpg**, and **.bmp**.

<img width="1892" height="985" alt="8 6" src="https://github.com/user-attachments/assets/f028bdbf-8701-434f-93c7-8b02639bc062" />

---

### 🧩 3. Open Command Line or Terminal

* Navigate to the folder where the `StegExpose.jar` file is located using your Command Prompt (Windows) or Terminal (Linux/macOS).

<img width="2568" height="1562" alt="Screenshot 2025-10-27 234255" src="https://github.com/user-attachments/assets/7317333c-3ff9-481b-b201-4c6f21ccef26" />


---


### 🧩 4. Run StegExpose on an Image

* Use the following command structure to analyze a single image for hidden data:

    **Command Structure:**
    ```bash
    java -jar StegExpose.jar <image_file_path>
    ```

    **Example:**
    ```bash
    java -jar StegExpose.jar test_image.png
    ```

---

### 🧩 5. Analyze the Output

* StegExpose calculates a **"suspect" score** ranging from 0 to 1. **The higher the score, the more likely steganography is present.**

| Score Range | Interpretation (Suggested Thresholds) |
| :---: | :--- |
| **Less than 0.2** | Image is considered **clean** (no hidden data detected). |
| **0.2 - 0.3** | **Possibly** some hidden data is present. |
| **Above 0.3** | **Likely** that steganography is present. |

* **Example Output Analysis:**
    ```bash
    java -jar StegExpose.jar suspect_image.png
    ```
    ```makefile
    Analyzing suspect_image.png...
    Result: 0.4
    Steganography likely present
    ```
  
<img width="2568" height="1562" alt="Screenshot 2025-10-27 234255" src="https://github.com/user-attachments/assets/d599b3c9-ad28-468c-9a2c-fac64115a3bb" />

<img width="2735" height="1696" alt="Screenshot 2025-10-27 234859" src="https://github.com/user-attachments/assets/a0890a0a-1c3d-4dc8-bff2-c3aac0b32ab1" />

---

### 🧩 6. Batch Analysis (Multiple Images)

* To check multiple images at once, specify the folder path containing the images:

    **Command Structure:**
    ```bash
    java -jar StegExpose.jar <folder_path>
    ```
---

### 🧩 7. Advanced Options (Optional)

* To view additional parameters, such as options for adjusting detection sensitivity or output verbosity, use the `--help` flag:

    **Command:**
    ```bash
    java -jar StegExpose.jar --help
    ```
---

###  🧾 Results

* Review the scores generated for each image and use the threshold values to determine which images require further forensic investigation to extract the suspected hidden data.

---

### 🧠 Conclusion

The experiment successfully demonstrated logical forensic extraction from an Android device using AFLogical OSE.
All artifacts were securely acquired, hashed for integrity verification, and properly documented following forensic standards.

---

### ⚠️ Notes & Limitations

AFLogical OSE performs logical acquisition only (not physical).
Data extraction depends on Android permissions and user consent.
It cannot bypass encryption or recover deleted data.
Always maintain hash integrity and chain of custody documentation.

---

### 📚 References

AFLogical OSE on GitHub
ADB Command-Line Reference
NIST SP 800-101 Rev.1 — Guidelines on Mobile Device 

---

### ✅ Final Outcome

AFLogical OSE successfully extracted logical data (contacts, SMS, call logs) from the Android device via ADB in a forensically sound manner.
All extracted files were hashed and documented to preserve evidence integrity.

📁 Evidence Path: D:\Case_07_AFLogical\forensics\
🔐 Hash Verification: Completed (SHA256)
🧾 Report: Case_07_AFLogical_Report.pdf
