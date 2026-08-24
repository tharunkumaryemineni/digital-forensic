# Wireshark – Password Capturing

## 📌 Aim

To capture and analyze HTTP network packets using **Wireshark** and identify form data submitted through a login page.

---

## 📖 Introduction

Wireshark is a network packet capture and analysis tool. It can capture information transmitted over a network, including usernames, email addresses, personal information, and passwords when the traffic is transmitted in an observable form.

Protocols such as **HTTP, FTP, and Telnet** may transmit information that can be inspected from captured packets. This can be useful for network troubleshooting and security testing, but it can also be misused to obtain sensitive information without authorization.

> ⚠️ **Note:** Perform packet capture and credential analysis only on systems and networks that you own or have explicit permission to test.

---

## 🛠️ Requirements

- Wireshark
- Windows or Linux
- Wi-Fi/Network connection
- Web browser
- Authorized vulnerable test website

---

## 🔬 Procedure

### Step 1: Start Wireshark

Open Wireshark and select the required network interface, such as **Wi-Fi**, and start capturing packets.

### Step 2: Open the Test Website

While Wireshark is capturing packets, open the authorized test website in a browser and enter the login credentials into the login form.

### Step 3: Filter HTTP Packets

After submitting the login form, return to Wireshark and apply the following display filter:

```text
http
<img width="1724" height="912" alt="ss 5" src="https://github.com/user-attachments/assets/c593bc15-8e5c-48f9-bf7d-a34164912a53" />
<img width="1917" height="1018" alt="ss 4" src="https://github.com/user-attachments/assets/1ab85403-67cc-44d6-848b-18764ffbd0d2" />
<img width="1917" height="1011" alt="ss 3" src="https://github.com/user-attachments/assets/3886c048-c49a-4d02-80f1-db5faece9a05" />
<img width="1742" height="903" alt="ss2" src="https://github.com/user-attachments/assets/6b32a368-139b-4007-b015-2417efe71edd" />
<img width="1917" height="1020" alt="ss 1" src="https://github.com/user-attachments/assets/be7d61b0-e920-4117-a420-5e0417f17636" />
