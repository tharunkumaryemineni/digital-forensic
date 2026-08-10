# 🔍 Evidence Acquisition Using AccessData FTK Imager

![Tool](https://img.shields.io/badge/Tool-FTK%20Imager-blue)
![Category](https://img.shields.io/badge/Category-Digital%20Forensics-critical)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6)

**Ex. No. 1 — Digital Forensics Lab**

---

## 📑 Table of Contents

- [Description](#-description)
- [Ways to Use FTK Imager](#-ways-to-use-ftk-imager)
- [Acquiring Volatile Memory (RAM)](#-acquiring-volatile-memory-ram)
- [Acquiring Non-Volatile Memory (Disk Image)](#-acquiring-non-volatile-memory-disk-image)
  - [Collecting Physical Drives](#collecting-physical-drives)
  - [Disk Image Formats](#disk-image-formats)
  - [Case Details & Image Destination](#case-details--image-destination)
  - [Verifying and Starting Acquisition](#verifying-and-starting-acquisition)
  - [Results](#results)

---

## 📖 Description

**Forensic Toolkit (FTK)** is a computer forensics software product made by **AccessData**, distributed as a Windows-based commercial tool. The same development team also maintains **FTK Imager** — a free version with fewer features, purpose-built for forensic investigations. FTK Imager is capable of both **acquiring** and **analyzing** computer forensic evidence.

The evidence FTK Imager can acquire splits into two main categories:

- Acquiring **volatile memory**
- Acquiring **non-volatile memory** (hard disk)

## 🖥️ Ways to Use FTK Imager

| Method | Description |
|---|---|
| **Portable version** | Run directly from a USB pen drive or HDD on the evidence machine. Most frequently used for **live data acquisition**, where the evidence PC/laptop is already switched on. |
| **Installed version** | Installed on the investigator's laptop. The source disk is mounted via a **write blocker**, which prevents any writes to the evidence disk while allowing read-only access — preserving the integrity of the source. |

---

## 🧠 Acquiring Volatile Memory (RAM)

FTK Imager can collect the complete volatile memory (RAM) of a live computer.

1. Open FTK Imager and navigate to the volatile memory icon (**Capture Memory**), then set a destination path and filename.

   ![Capture Memory icon and Memory Capture dialog](images/01-capture-memory-icon.jpg)

   > **Note:** FTK Imager provides options to include the **pagefile** and create an **AD1** file when acquiring volatile memory.
   >
   > - **Pagefile** (`pagefile.sys`) — used by Windows as an extension of physical RAM once available memory is exceeded. It sits on the `C:` partition and often holds valuable data, so it's recommended to capture it alongside the RAM.
   > - **AD1 file** — FTK Imager's own image file format, optional, for later use by the investigator.

2. Click **Capture Memory** to start acquiring the volatile memory.

   ![Memory capture in progress](images/02-memory-progress.jpg)

   > **Note:** Once acquisition completes, the destination folder will contain the acquired memory with a **`.mem`** file extension.

---

## 💾 Acquiring Non-Volatile Memory (Disk Image)

The same tool can also be used to collect a full disk image.

1. Open FTK Imager and navigate to **Create Disk Image**.

   ![Create Disk Image icon](images/03-create-disk-image-icon.jpg)

2. Select the source you need to acquire.

   ![Select Source dialog](images/04-select-source.jpg)

   > **Note:** FTK Imager can acquire **physical drives**, **logical drives** (partitions), **image files**, the **contents of a folder**, or **CDs/DVDs**. External HDDs should be connected through a write blocker and acquired using the **Logical Drive** option, selecting the mounted HDD as a partition.

### Collecting Physical Drives

1. Select the **Physical Drive** option.
2. Select the drive you need to acquire and click **Finish**.

   ![Select Drive dialog](images/05-select-physical-drive.jpg)

### Disk Image Formats

| Format | Notes |
|---|---|
| **Raw (dd)** | The image format most commonly used by modern analysis tools. Contains no headers, metadata, or magic values. Skipped or unreadable memory ranges are padded, which helps maintain spatial integrity (relative offsets among data). |
| **SMART** | Designed for Linux file systems. Keeps disk images as pure bitstreams with optional compression. Starts with a standard 13-byte header followed by sections, each with a type string, a 64-bit offset to the next section, a 64-bit size, padding, and a CRC. |
| **E01** | A proprietary format developed by Guidance Software's **EnCase**. Compresses the image file. Header and footer store case information — including an MD5 hash of the entire bitstream, acquisition date/time, examiner's name, notes, and an optional password. |
| **AFF** (Advanced Forensic Format) | Developed by Simson Garfinkel and Basis Technology; latest implementation is **AFF4**. Designed to avoid locking investigators into a proprietary format that could prevent proper analysis later. |

### Case Details & Image Destination

1. Enter the case details.

   ![Evidence Item Information dialog](images/06-evidence-item-information.jpg)

2. Add an image destination (where the image file will be saved), an image filename, and a fragment size.

   ![Select Image Destination dialog](images/07-select-image-destination.jpg)

   > **Image Fragment Size (MB):** Splits the image file into multiple fragments saved to the same destination. Set this to **`0`** if you want a single, unfragmented image file instead.

### Verifying and Starting Acquisition

1. Select **Verify images after they are created**. This verifies the hash values once the image has been created — recommended to ensure integrity, though it increases acquisition time, especially for large disk images.

   ![Verify images after they are created option](images/08-verify-images-option.jpg)

2. Click **Start** to begin acquiring.

   ![Creating image progress](images/09-creating-image-progress.jpg)

### Results

Once acquisition is complete, FTK Imager generates a text file containing all the information it has acquired, and confirms the hash verification.

![Image created successfully](images/10-image-created-successfully.png)

![Image summary showing computed and verified hash values](images/11-image-summary-hash.png)

✅ **Hash values are matched.**

---

<sub>Digital Forensics Lab · Ex. No. 1</sub>
<img width="500" height="472" alt="SS 1" src="https://github.com/user-attachments/assets/7117c2cf-a29f-4ba8-91f4-0c7bbd36bf4c" />
<img width="505" height="390" alt="SS 2" src="https://github.com/user-attachments/assets/1d75c2fb-23a1-4fcc-98b2-0e7e73c8da6e" />
<img width="1438" height="1094" alt="SS 3" src="https://github.com/user-attachments/assets/95b47f88-5282-4d4c-bda4-a22bde22a059" />
<img width="585" height="428" alt="SS 4" src="https://github.com/user-attachments/assets/c2b60342-140c-4a42-8e30-66020a625c6d" />
<img width="575" height="426" alt="SS 5" src="https://github.com/user-attachments/assets/65636937-10c0-456a-a6eb-f6fe993e0f29" />
<img width="395" height="347" alt="SS 6" src="https://github.com/user-attachments/assets/5eed39b3-c3ad-4219-9ab4-9565410916dc" />
<img width="465" height="355" alt="SS 7" src="https://github.com/user-attachments/assets/eb911822-778a-4cec-86d5-c3ac740cdc69" />
<img width="1172" height="1342" alt="SS 8" src="https://github.com/user-attachments/assets/a1615b16-fcd9-4dca-8124-98db6c021e26" />
<img width="470" height="355" alt="SS 9" src="https://github.com/user-attachments/assets/a3ffa82a-5503-4969-91e7-07fb81534df9" />
