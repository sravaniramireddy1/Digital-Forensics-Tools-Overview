#  Ex.No.3   Wireshark – Network Packet Capture and Analysis Tools

## Step 1: Begin Packet Capture

- Launch Wireshark on your system. A list of network interfaces (like Wi-Fi or Ethernet) will appear.

- Choose the interface currently connected to the internet (for example, Wi-Fi) to start capturing packets.

<br>
   <br>
  <p align="center">
 <img width="1724" height="746" alt="Screenshot 2025-08-29 213014" src="https://github.com/user-attachments/assets/cd0dc575-d400-4b46-8dea-ecace31e1e48" />
 </p>
  <br>
  <br>


- Press the blue shark fin button 🦈 at the top-left corner to initiate packet capture. Once clicked, Wireshark starts recording all the network traffic flowing through the chosen interface.

<br>
   <br>
  <p align="center">
<img width="1886" height="894" alt="Screenshot 2025-08-29 213112" src="https://github.com/user-attachments/assets/3e63f8b2-fe98-4cd2-8e74-ff23137d75d4" />
</p>
  <br>
  <br>

### Step 2: Create Login Traffic

- Open any web browser and visit http://testphp.vulnweb.com/login.php

- Enter some sample credentials, for example:

      - Username: Sravani

      - Password: Sravani@123

- Hit the Login button. Even though the login attempt will fail, the entered data will still be transmitted over the network.

<br>
   <br>
  <p align="center">
<img width="1067" height="646" alt="Screenshot 2025-08-29 213247" src="https://github.com/user-attachments/assets/98712208-bc1f-4c89-b5be-654ac894420b" />
</p>
  <br>
  <br>
        
### Step 3: Stop Capture and Apply Filter

- Go back to Wireshark and press the red square (Stop button) to end the capture.

- To locate the login details, focus on the packets carrying form data, which are usually sent via an HTTP POST request.

- In the filter bar, type the HTTP filter and hit Enter to narrow down the results and spot the required packet.

<br>
   <br>
  <p align="center">
<img width="1903" height="389" alt="Screenshot 2025-08-29 213420" src="https://github.com/user-attachments/assets/bb8cf59d-6a43-4d41-adc8-f40dfc99915b" />
  </p>
  <br>
  <br>
  
### Step 4: Inspect Packets for Credentials

- From the filtered results, locate a packet showing something like “POST /userinfo.php” and click on it.

- In the Packet Details section, expand:

- Hypertext Transfer Protocol (HTTP)

- HTML Form URL Encoded

- Within the HTML Form URL Encoded part, you’ll find the username and password you entered, displayed in plaintext.

<br>
   <br>
  <p align="center">
<img width="1524" height="806" alt="Screenshot 2025-08-29 213605" src="https://github.com/user-attachments/assets/0bf565d7-8349-4a7c-b94c-1150788d9b95" />
</p>
  <br>
  <br>


<br>
   <br>
  <p align="center">
<img width="1524" height="806" alt="Screenshot 2025-08-29 213605" src="https://github.com/user-attachments/assets/19c9da89-3c8f-40ef-bc65-de2a997990a2" />
</p>
  <br>
  <br>
  
### Result: 

The experiment was able to capture and view login credentials in plain text. By analyzing the POST packet, the transmitted data could be clearly seen.
This proves the weakness of the HTTP protocol, as it sends sensitive information without encryption, making it easy for attackers to intercept.
