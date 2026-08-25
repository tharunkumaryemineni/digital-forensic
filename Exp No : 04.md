# 📧 Email Header Analysis and Email Spoofing Detection Using MHA

## 📌 Experiment No. 4

### 🎯 Aim

To analyze email headers and detect email spoofing using **MHA (Mail Header Analyzer)**.

---

## 📖 Description

Email header analysis is used to examine the metadata of an email and identify information about the sender, recipient, mail servers, IP addresses, authentication results, and possible spoofing.

---

## 🛠️ Procedure

### 1. Access the Email Header

#### Gmail

1. Open the email.
2. Click the **three dots (More)**.
3. Select **Show original**.

#### Outlook

1. Open the email.
2. Click **File**.
3. Select **Properties**.
4. Find **Internet headers**.

#### Yahoo

1. Open the email.
2. Click the **three dots (More)**.
3. Select **View raw message**.

### 2. Copy the Email Header

Copy the complete email header. It contains metadata about the journey of the email from the sender to the recipient.

### 3. Identify Key Header Fields

| Field | Description |
|---|---|
| `From` | Sender's email address |
| `To` | Recipient's email address |
| `Date` | Date and time the email was sent |
| `Subject` | Subject of the email |
| `Return-Path` | Return address if the email bounces |
| `Received` | Servers through which the email passed |
| `Message-ID` | Unique identifier of the email |
| `SPF` | Checks whether the sending IP is authorized |
| `DKIM` | Verifies email authentication and integrity |
| `DMARC` | Uses SPF and DKIM for authentication |

---

## 🔍 Analyze the `Received` Fields

The `Received` fields show the path taken by the email from the sender to the recipient.

Check:

- Sending server hostname/IP address
- Receiving server hostname/IP address
- Date and time
- Unexpected servers
- Suspicious IP addresses

---

## 🌐 Check IP Addresses and Hostnames

Use WHOIS or IP lookup services to investigate IP addresses found in the `Received` fields.

Check whether:

- The IP belongs to the expected mail server.
- The hostname matches the sending domain.
- The IP address appears suspicious.
- The location or ownership is unexpected.

---

## 🔐 SPF, DKIM and DMARC Analysis

### SPF

**Sender Policy Framework** checks whether the sending IP is authorized to send emails for the domain.

- ✅ **Pass** – IP is authorized.
- ❌ **Fail** – IP is not authorized and may indicate spoofing.

### DKIM

**DomainKeys Identified Mail** verifies email authentication and integrity.

- ✅ **Pass** – Authentication is successful.
- ❌ **Fail** – Email may have been altered or authentication failed.

### DMARC

**Domain-based Message Authentication, Reporting and Conformance** uses SPF and DKIM to authenticate emails.

- ✅ **Pass** – Authentication/alignment is successful.
- ❌ **Fail** – Possible spoofing or authentication problem.

---

## 🆔 Message-ID Analysis

The `Message-ID` is a unique identifier for an email.

Check whether the domain in the `Message-ID` matches the sender's domain.

A mismatch may indicate possible email spoofing.

---

## ⚠️ Detecting Anomalies

Check for:

1. **Email Domain Mismatch**
   - Compare `From`, `Return-Path`, and `Message-ID`.

2. **Suspicious IP Addresses**
   - Check whether the IP belongs to the expected mail server.

3. **Suspicious Timestamps**
   - Compare timestamps in the `Received` fields.

4. **Authentication Failures**
   - Check SPF, DKIM, and DMARC results.

---

## 🧪 Sample Email Header

```text
Received: from mail.example.com (mail.example.com [192.0.2.1])
 by mail.receiver.com with ESMTP id u29si8604336pjs.40.2023.08.10.07.00.16;
 Thu, 10 Aug 2023 07:00:16 -0700 (PDT)

Received: by mail.example.com with SMTP id a1mr1243772ywh.51;
 Thu, 10 Aug 2023 07:00:15 -0700 (PDT)

Message-ID: <CA+7eu=4pSeXgQ@mail.example.com><img width="1910" height="912" alt="Screenshot 2026-08-24 234628" src="https://github.com/user-attachments/assets/98e6b93e-f315-4332-b949-469974862df3" />
<img width="1883" height="912" alt="Screenshot 2026-08-25 095359" src="https://github.com/user-attachments/assets/5b2b4da4-b582-46e3-9e84-ae7524d770f0" />
<img width="1553" height="817" alt="Screenshot 2026-08-24 235240" src="https://github.com/user-attachments/assets/67f543bd-4443-43b3-b2e0-d5fd933679e4" />
<img width="1560" height="317" alt="Screenshot 2026-08-24 234921" src="https://github.com/user-attachments/assets/5d398af1-36dc-430f-b4d0-64802eb265a9" />
<img width="922" height="193" alt="Screenshot 2026-08-24 234701" src="https://github.com/user-attachments/assets/0a917e1d-7004-45f2-9398-bf6ee202fb77" />
<img width="1902" height="905" alt="Screenshot 2026-08-24 234654" src="https://github.com/user-attachments/assets/10c9bfb6-85df-4ddb-9004-8bfacdd34eb1" />
<img width="1910" height="912" alt="Screenshot 2026-08-24 234628" src="https://github.com/user-attachments/assets/9a89e2d8-0bee-46ba-b839-0289ce5b4986" />
