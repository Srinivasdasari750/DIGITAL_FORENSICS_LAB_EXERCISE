# Ex.No.4   MHA (Mail Header Analyzer)
## 🎯 Aim  
To use a **Mail Header Analyzer (MHA)** to trace the origin of an email and verify its authenticity by examining the header for signs of spoofing.

## 🛠️ Tools Required  
-  Email account (e.g., Gmail)  
-  Online Mail Header Analyzer (e.g., MXToolbox)  
-  Computer with internet access  


## 📝 Procedure  
### 1️⃣ Step 1: Get the Email Header  
- Open the email whose header needs to be analyzed.  
- In **Gmail**: Click on the **three dots (⋮)** → select **Show Original**.  
- Copy the **entire raw email header** text.  

<br>
<img  src="https://github.com/user-attachments/assets/97c7b348-5f67-4b02-8bb9-9d29de86a5f4" />

<br>
- Select all the text in the header and copy it.

<br>
<img width="1505" height="919" alt="Screenshot 2025-09-01 212318" src="https://github.com/user-attachments/assets/28e3b6d8-f667-444a-bb3d-c45f1911d4e5" />

<br>
<br>

### 2️⃣ Step 2: Use a Mail Header Analyzer  
- Navigate to an online tool such as **MXToolbox Email Header Analyzer**.  
- Paste the copied email header into the **analysis box**.  
- Click **Analyze** to generate a detailed, human-readable report.
 <br>
<br>

<img width="1919" height="901" alt="Screenshot 2025-09-01 212349" src="https://github.com/user-attachments/assets/672d3f77-1c2f-413e-964c-ea3b7ce45bb4" />

<br>
<br>

- Pasting email header in MHA tool  
- Analyzer’s parsed results  

<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>

<img width="1917" height="903" alt="Screenshot 2025-09-01 212430" src="https://github.com/user-attachments/assets/9c73b860-36ab-4c19-9440-4f855fc42056" />

### 3️⃣ Step 3: Analyze the Report  

#### ✅ Overall Delivery Summary  
- **DMARC Compliance:**  Passed → The email complies with DMARC policy.  
- **SPF Status:**  Passed → SPF Authenticated & Alignment successful; sending server authorized.  
- **DKIM Status:**  Alignment Passed but Authentication Failed → Indicates a problem with the email’s digital signature.  

<br>
<br>
<img width="1905" height="904" alt="Screenshot 2025-09-01 212502" src="https://github.com/user-attachments/assets/8c992527-f843-48a8-9e17-63e974b8e2d4" />


<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br>
<img width="1900" height="908" alt="Screenshot 2025-09-01 212545" src="https://github.com/user-attachments/assets/e11899c5-4b55-4487-9792-bec3be98f36c" />

<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="1872" height="555" alt="Screenshot 2025-09-01 212617" src="https://github.com/user-attachments/assets/8e78bfa0-1d0a-48b8-986f-92b42693a6ba" />

## ✅ Result  
The experiment successfully analyzed an email header using the **Mail Header Analyzer (MHA)** tool.  

- The **SPF check** passed because the sending server (`mailgun.net`) was authorized in the SPF record.  
- The **DMARC check** passed, confirming overall compliance with the sender’s domain policy.  
- The **DKIM check** partially failed: while alignment passed, authentication failed ❌, indicating a possible misconfiguration or an issue with the sender’s digital signature.  

🔎 This demonstrates how MHA helps in tracing the email’s origin, verifying authenticity, and detecting signs of spoofing or tampering.  
