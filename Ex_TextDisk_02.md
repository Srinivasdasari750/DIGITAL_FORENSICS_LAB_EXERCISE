#  Ex.No.2    TestDisk: Open-Source Data Recovery Tool

## 🎯 Aim
To use TestDisk step by step to recover a missing partition and repair a corrupted one.



## 📥 Installation
Linux (Debian/Ubuntu): sudo apt-get install testdisk

macOS (Homebrew): brew install testdisk

Windows: Download the executable from the official CGSecurity website.

## 🔎 Procedure

### 1. Create a Log File
- Launch TestDisk from your terminal or command prompt using sudo testdisk (or testdisk_win.exe on Windows).

- Select the [Create] option to generate a log file of the recovery session. This is helpful for future reference or troubleshooting.
<br>
<br>

<img src="https://github.com/user-attachments/assets/703ad113-9c61-4d39-ae2f-2d6d95c87bb2" />


</p>
<br>
<br>

### 2. Select the Drive to Analyze
- TestDisk will display a list of all detected storage devices.

- Use the Up/Down arrow keys to highlight the drive that contains your lost data.

<br>
<br>

<img src="https://github.com/user-attachments/assets/43561ed7-50fe-4c66-8de5-37533b1d9622" />

</p>
<br>
<br>

- Select [Proceed] to move to the next step.

### 3. Choose the Partition Table Type
- TestDisk will automatically suggest the most likely partition table type (e.g., Intel/PC, EFI GPT).

- The default value is usually correct. Confirm the selection by pressing Enter.
<br>
<br>
<img src="https://github.com/user-attachments/assets/96d88ed1-1314-4685-8a6e-6a70a105f6f6" />


</p>
<br>
<br>

### 4. Analyze Current Partition Structure
- From the main menu, choose [Analyse] and press Enter.
<br>
<br>
<img src="https://github.com/user-attachments/assets/1b98ebc3-1093-43f0-bd6b-132f7fba9d23" />


</p>
<br>
<br>

- This will display the current partition table and check for errors or missing partitions.

### 5. Perform a Quick Search
- After the analysis, you will be prompted to perform a [Quick Search].

<br>
<br>
<img src="https://github.com/user-attachments/assets/7149b460-ffc8-4c3a-a40e-398c12d70f60" />

</p>
<br>
<br>

- Select it and press Enter to scan the drive for lost partitions.

- Once a partition is found, you can press p to list its files. Deleted files and folders often appear in red.

- Press q to return to the search results.

  ### 6. Perform a Deeper Search
- If the Quick Search fails to find your lost partitions, select [Deeper Search].

-<br>
<br>
<img src="https://github.com/user-attachments/assets/4c411fdb-f895-4379-9223-29bddb0613e9" />

</p>
<br>
<br>

- This process can take a long time, as it scans the entire drive, block by block, to find remnants of partition structures.

- Again, use p to preview files and confirm if a found partition is the one you are looking for.

### 7. Modify Partition Status
- After finding the correct partitions, use the Left/Right arrow keys to set their status.

- Use **Left/Right arrow keys** to change status:  
  - **P**: Primary  
  - ***:** Bootable  
  - **L**: Logical  
  - **D**: Deleted

    <br>
<br>
<img src="https://github.com/user-attachments/assets/6f94b993-9391-4f01-b422-d784b746afaa" />


</p>
<br>
<br>

- Ensure that the partitions you want to recover are marked as Primary or Logical (and not deleted).

### 8. Write the Partition Table
- Once you are confident the partition structure is correct, select [Write] from the menu.

<br>
<br>
<img src="https://github.com/user-attachments/assets/936caea4-063d-4995-b362-e6c6ef258cc2" />

<br>
<br>

- Confirm the operation by pressing y (for yes). This will write the new partition table to your disk.

<br>
<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/d3f1429d-6531-4e08-9b1c-0334d0d1ee4e" />

</p>
<br>
<br>


- WARNING: This is a permanent change. Double-check your selections before writing.

### 9. Recover Files
- If you just need to recover a few files without fixing the partition table, you can do so from the file list (after pressing p).

- Navigate to the folder containing your desired files.

- Use the colon : key to select the files you want to recover.

- Press the uppercase C key to copy the selected file(s).

- Navigate to a safe destination on a different storage device and press uppercase C again to paste.

### 10. Exit and Restart
- Once your task is complete, select [Quit] to exit the program.

- If you wrote a new partition table to the drive, it is recommended to restart your computer to allow the operating system to recognize the changes.

## ✅ Result

Successfully learned how to install and run TestDisk detect, analyze, and recover lost/corrupted partitions Preview and recover files securely Repair and rewrite partition tables for data recovery.
