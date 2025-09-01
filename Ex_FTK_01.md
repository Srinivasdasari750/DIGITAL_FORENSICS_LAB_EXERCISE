
🎯 Aim:  
To learn and perform forensic acquisition of digital evidence using **FTK Imager Toolkit**, and to understand how to create, verify, and analyze forensic images step by step.  

📖 Description  
FTK Imager is a forensic imaging tool that allows investigators to create exact copies of digital storage devices or files without altering the original evidence.It helps in capturing forensic
images, verifying their integrity through hash values, and previewing file systems. The tool is widely used in digital forensics for evidence acquisition and preliminary analysis.  

🛠️ Tools Required:  
-  A computer with **FTK Imager** installed  
-  Sample storage media / disk image for testing  
-  External storage device (to save the acquired image)  
- 🖼 Screenshots captured during each step of the process  

📝 Procedure:

🔹 Step 1: Launching FTK Imager  
- Open the FTK Imager application from the system.  
- The main interface will display options for creating forensic images, capturing memory, and adding evidence items.  

  [Step 1 Screenshot](C:\Users\SRINIVAS\Pictures\Screenshots\Screenshot 2025-09-01 221146.png)  


🔹 Step 2: Creating a Forensic Image  
- Go to **File → Create Disk Image**.  
- Choose the source type (Physical Drive, Logical Drive, Image File, or Contents of a Folder).  
- Select the appropriate source media that you want to acquire.  

  [Step 2 Screenshot](C:\Users\SRINIVAS\Pictures\Screenshots\Screenshot 2025-09-01 222739.png)  

🔹 Step 3: Selecting Image Destination  
- Choose the image type (E01, RAW, SMART, or AFF).  
- Provide a destination folder and filename to store the image.  
- Enter case details such as Case Number, Evidence Number, Examiner Name, and Description for documentation.  

  [Step 3 Screenshot](C:\Users\SRINIVAS\Pictures\Screenshots\Screenshot 2025-09-01 222839.png)  

🔹 Step 4: Configuring Image Options  
- Set the compression level and segment size (if required).  
- Enable **MD5** and **SHA1** hashing options to generate hash values for integrity verification.  

  [Step 4 Screenshot](C:\Users\SRINIVAS\Pictures\Screenshots\Screenshot 2025-09-01 222810.png)  

🔹 Step 5: Starting the Imaging Process  
- Click on **Start** to begin the acquisition.  
- The tool will copy the selected data into a forensic image file while generating hash values.  

  [Step 5 Screenshot](C:\Users\SRINIVAS\Pictures\Screenshots\Screenshot 2025-09-01 222825.png)  

🔹 Step 6: Verification of Image Integrity  
- After completion, FTK Imager verifies the generated hash values with the original source.  
- If both values match, it confirms that the acquired image is an exact replica of the original.  

  [Step 6 Screenshot](C:\Users\SRINIVAS\Pictures\Screenshots\Screenshot 2025-09-01 222839.png)  

🔹 Step 7: Previewing the Image  
- Load the created forensic image into FTK Imager using **File → Add Evidence Item**.  
- Browse through file structures, deleted files, and system metadata for preliminary analysis.  

  [Step 7 Screenshot](images/step7.png)  

✅ Result:
Successfully created a forensic image using FTK Imager, verified its integrity through hashing, and previewed the acquired evidence without altering the original data. This demonstrates the correct
procedure for forensic acquisition using FTK Imager Toolkit.  
