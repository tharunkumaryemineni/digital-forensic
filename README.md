# Ex.No.1 - Evidence Acquisition Using FTK Imager

## Aim

To acquire digital forensic evidence using **AccessData FTK Imager** by capturing both **volatile memory (RAM)** and **non-volatile memory (Disk Image)** while maintaining evidence integrity.

---

## Objective

- Learn the basics of FTK Imager.
- Acquire volatile memory from a running system.
- Acquire non-volatile memory (disk image).
- Understand different forensic image formats.
- Verify evidence integrity using hash values.

---

## Software Required

- AccessData FTK Imager
- Windows Operating System
- Storage device (USB/HDD)
- Write Blocker (recommended for disk acquisition)

---

## About FTK Imager

FTK (Forensic Toolkit) Imager is a digital forensic tool developed by **AccessData**. It is used to create forensic images of storage devices and capture volatile memory for forensic investigations. The tool helps investigators preserve digital evidence without modifying the original data. :contentReference[oaicite:0]{index=0}

---

## Types of Evidence Acquisition

### 1. Volatile Memory Acquisition
Captures the contents of the system's RAM while the computer is running.

### 2. Non-Volatile Memory Acquisition
Creates a forensic image of storage devices such as hard disks, SSDs, USB drives, and partitions. :contentReference[oaicite:1]{index=1}

---

# Procedure

## Part A – Volatile Memory Acquisition

1. Open **FTK Imager**.
2. Click **Capture Memory**.
3. Select the destination folder.
4. (Optional) Include:
   - Pagefile
   - AD1 file
5. Click **Capture Memory**.
6. Wait for the acquisition process to complete.
7. The memory dump is saved with the `.mem` extension. :contentReference[oaicite:2]{index=2}

---

## Part B – Non-Volatile Memory Acquisition

1. Open **FTK Imager**.
2. Select **Create Disk Image**.
3. Choose the source type:
   - Physical Drive
   - Logical Drive
   - Image File
   - Folder Contents
   - CD/DVD
4. Select the drive to acquire.
5. Choose the image format.
6. Enter the case details.
7. Select the destination folder.
8. Specify image filename and fragment size.
9. Enable **Verify Images After Creation**.
10. Click **Start**.
11. Wait until acquisition completes.
12. Review the generated acquisition report. :contentReference[oaicite:3]{index=3}

---

# Supported Image Formats

| Format | Description |
|---------|-------------|
| RAW (dd) | Standard raw forensic image format used by most forensic tools. |
| SMART | Designed primarily for Linux forensic imaging. |
| E01 | EnCase proprietary compressed forensic image format with metadata and MD5 hash. |
| AFF | Open Advanced Forensic Format (AFF/AFF4). | :contentReference[oaicite:4]{index=4}

---

# Verification

After the acquisition process:

- FTK Imager generates an acquisition report.
- Hash values are calculated.
- Matching hash values confirm evidence integrity. :contentReference[oaicite:5]{index=5}

---

# Result

Successfully acquired:

- Volatile Memory (RAM)
- Non-Volatile Memory (Disk Image)

using **AccessData FTK Imager**, and verified the integrity of the acquired evidence using hash verification.

---

# Conclusion

FTK Imager is an effective forensic acquisition tool that enables investigators to securely capture volatile and non-volatile digital evidence while preserving data integrity through forensic imaging and hash verification.

---

## Author

**Name:** Tharun  
**Subject:** Digital Forensics Laboratory  
**Experiment:** Ex.No.1 – Evidence Acquisition Using FTK Imager

---

## License

This repository is created for educational and academic purposes.
<img width="500" height="472" alt="SS 1" src="https://github.com/user-attachments/assets/7117c2cf-a29f-4ba8-91f4-0c7bbd36bf4c" />
<img width="505" height="390" alt="SS 2" src="https://github.com/user-attachments/assets/1d75c2fb-23a1-4fcc-98b2-0e7e73c8da6e" />
<img width="1438" height="1094" alt="SS 3" src="https://github.com/user-attachments/assets/95b47f88-5282-4d4c-bda4-a22bde22a059" />
<img width="585" height="428" alt="SS 4" src="https://github.com/user-attachments/assets/c2b60342-140c-4a42-8e30-66020a625c6d" />
<img width="575" height="426" alt="SS 5" src="https://github.com/user-attachments/assets/65636937-10c0-456a-a6eb-f6fe993e0f29" />
<img width="395" height="347" alt="SS 6" src="https://github.com/user-attachments/assets/5eed39b3-c3ad-4219-9ab4-9565410916dc" />
<img width="465" height="355" alt="SS 7" src="https://github.com/user-attachments/assets/eb911822-778a-4cec-86d5-c3ac740cdc69" />
<img width="1172" height="1342" alt="SS 8" src="https://github.com/user-attachments/assets/a1615b16-fcd9-4dca-8124-98db6c021e26" />
<img width="470" height="355" alt="SS 9" src="https://github.com/user-attachments/assets/a3ffa82a-5503-4969-91e7-07fb81534df9" />
