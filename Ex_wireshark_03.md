#   Ex.No.3   Wireshark – Network Packet Capture and Analysis Tool

## 🎯 Aim  
To capture and analyze network traffic using **Wireshark**, and to demonstrate how plaintext credentials transmitted over the HTTP protocol can be intercepted.  

## 🛠️ Tools Required  
-  **Wireshark** (Network packet capture and analysis tool)  
-  **Web browser** (e.g., Chrome/Firefox/Edge)  
-  **Test website with HTTP login form** 
-  **Computer with internet access**  


## 📝 Procedure Capturing Plaintext Passwords

### Step 1: Start Capturing Packets
- First, open Wireshark. You will see a list of all available network interfaces (e.g., "Wi-Fi," "Ethernet").


- Select the interface your computer is using to connect to the internet (in this case, Wi-Fi).

  <br>
   <br>
<img width="957" height="794" alt="Screenshot 2025-09-01 212943" src="https://github.com/user-attachments/assets/cd566815-7602-4413-9cd3-343700470c29" />


  </p>
  <br>
  <br>

- Click the blue shark fin icon 🦈 in the top-left corner to start the capture. Wireshark will immediately begin capturing all traffic passing through that interface.
 <br>
   <br>
<img width="1919" height="1029" alt="Screenshot 2025-09-01 213050" src="https://github.com/user-attachments/assets/006d12a4-a202-499a-bc41-5edb36d566a9" />

 </p>
  <br>
  <br>

  ### Step 2: Generate Login Traffic
  - Open a web browser and navigate to http://testphp.vulnweb.com/login.php.

- Enter any dummy credentials. For this example, we'll use:

   Username: golddude

   Password: trinity07

- Click the login button. The login will fail, but the data has already been sent across the network.

 <br>
   <br>
<img width="1919" height="935" alt="Screenshot 2025-09-01 214539" src="https://github.com/user-attachments/assets/82fa19f2-fadd-4f43-9719-0f2907714236" />

 </p>
  
  
### step 3: Stop Capture and Filter Traffic

- Return to Wireshark and click the Stop button (the red square).

- In the display filter bar, you need to find the packet containing the login data. Since the form data was sent to the server, we will look for an HTTP POST request.

- Apply the following filter to find the exact packet and press Enter:

 <br>
   <br>
<img width="1919" height="1028" alt="Screenshot 2025-09-01 215119" src="https://github.com/user-attachments/assets/8cef796f-6851-4e8a-a3a7-6e9272e3833a" />

 </p>
  <br>
  <br>

### step 4: Inspect the Packet to Find Credentials 

- In the filtered packet list, you should see a packet with information like "POST /userinfo.php". Select this packet.

- In the Packet Details pane below the list, expand the following sections:

Hypertext Transfer Protocol

HTML Form URL Encoded

- Inside the "HTML Form URL Encoded" section, you will see the credentials you entered in plaintext.

 <br>
   <br>
<img width="954" height="257" alt="Screenshot 2025-09-01 215157" src="https://github.com/user-attachments/assets/efeb4fbc-936e-44d5-b5e2-2451c0aaef63" />

 </p>
  <br>
  <br>

---

## ✅ Result
The experiment successfully intercepts the login credentials in a human-readable format. The analysis of the captured POST packet reveals the plaintext data that was transmitted over the network:

This result confirms the inherent security flaw of the HTTP protocol. Any sensitive data sent over HTTP is transmitted openly, making it trivial to intercept.
