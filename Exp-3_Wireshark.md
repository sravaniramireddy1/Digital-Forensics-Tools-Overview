#  Ex.No.3   Wireshark – Network Packet Capture and Analysis Tool

**So, here we will see how we can capture the password using the Wireshark network capture analyzer. and see the outputs of the following steps.**

**Step 1:**

**First of all, open your Wireshark tool in  Windows  and start capturing the network. suppose I am capturing my wireless fidelity.**

<br>
   <br>
  <p align="center">
 <img width="1724" height="746" alt="Screenshot 2025-08-29 213014" src="https://github.com/user-attachments/assets/cd0dc575-d400-4b46-8dea-ecace31e1e48" />
 </p>
  <br>
  <br>



<br>
   <br>
  <p align="center">
<img width="1886" height="894" alt="Screenshot 2025-08-29 213112" src="https://github.com/user-attachments/assets/3e63f8b2-fe98-4cd2-8e74-ff23137d75d4" />
 </p>
  <br>
  <br>


**Step 2:**

**After starting the packet capturing we will go to the website and login the credential on that website as you can see in the image.**

<br>
   <br>
  <p align="center">
<img width="1886" height="894" alt="Screenshot 2025-08-29 213112" src="https://github.com/user-attachments/assets/3e63f8b2-fe98-4cd2-8e74-ff23137d75d4" />
 </p>
  <br>
  <br>


<img width="1067" height="646" alt="Screenshot 2025-08-29 213247" src="https://github.com/user-attachments/assets/98712208-bc1f-4c89-b5be-654ac894420b" />

**Step 3:**

**Now after completing the login credential we will go and capture the password in Wireshark. for that we have to use some filter that helps to find the login credential through the packet capturing.**         

<img width="1903" height="389" alt="Screenshot 2025-08-29 213420" src="https://github.com/user-attachments/assets/bb8cf59d-6a43-4d41-adc8-f40dfc99915b" />

**Step 4:** 

**Wireshark has captured some packets but we specifically looking for HTTP packets. so in the display filter bar we use some command to find all the captured HTTP packets. as you can see in the below image the green bar where we apply the filter.
http**

<img width="1524" height="806" alt="Screenshot 2025-08-29 213605" src="https://github.com/user-attachments/assets/0bf565d7-8349-4a7c-b94c-1150788d9b95" />


<img width="1524" height="806" alt="Screenshot 2025-08-29 213605" src="https://github.com/user-attachments/assets/19c9da89-3c8f-40ef-bc65-de2a997990a2" />

