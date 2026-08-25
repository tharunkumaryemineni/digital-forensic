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

<img width="1553" height="817" alt="Screenshot 2026-08-24 235240" src="https://github.com/user-attachments/assets/e7900a30-1d06-4d65-8fa7-6b55d272a6cb" />
<img width="1560" height="317" alt="Screenshot 2026-08-24 234921" src="https://github.com/user-attachments/assets/097f3bec-57a5-4b79-b2bb-24d5a8712f35" />
<img width="922" height="193" alt="Screenshot 2026-08-24 234701" src="https://github.com/user-attachments/assets/8308e0f4-ed35-4e46-bd58-018ee0da497e" />
<img width="1902" height="905" alt="Screenshot 2026-08-24 234654" src="https://github.com/user-attachments/assets/6d5c19e9-ba7f-4e75-921b-d3e77a937e46" />
<img width="1910" height="912" alt="Screenshot 2026-08-24 234628" src="https://github.com/user-attachments/assets/457562c2-4d76-447e-aa6b-26e954e50842" />
<img width="1883" height="912" alt="Screenshot 2026-08-25 095359" src="https://github.com/user-attachments/assets/de323c93-67b6-4b9d-a55a-c18681f177b2" />
