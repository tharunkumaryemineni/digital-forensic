
# Experiment - 02: Recover Deleted or Damaged Files Using TestDisk

## AIM
To recover a deleted or missing partition and restore access to the files using TestDisk.

## SOFTWARE USED
- TestDisk 7.3-WIP
- Windows Operating System
- USB Pendrive
- NTFS File System

---

## INTRODUCTION

TestDisk is a free and open-source data recovery utility used to recover lost partitions, repair damaged partition structures, and restore access to files from storage devices.

In this experiment, a 4 GB partition named `Testing` was created on a USB pendrive. The partition was deleted to simulate data loss. TestDisk was then used to analyse the USB pendrive, locate the deleted partition, verify the files stored in it, and restore the partition structure.

---

## PROCEDURE

### Step 1: Open TestDisk

1. Open `testdisk_win.exe` with administrator privileges.
2. TestDisk displays information about the data recovery utility and provides options for creating or appending a log file.
3. Select `Create` and press **Enter** to create a new log file.

**Observation:** TestDisk was successfully started, and the option to create a new log file was selected.

---

### Step 2: Select the USB Pendrive

TestDisk displays all detected physical storage devices.

The USB pendrive was identified as:

- **Physical Drive:** PhysicalDrive1
- **Capacity:** 125 GB / 117 GiB
- **Device:** USB DISK 2.0

Select the USB pendrive and choose `Proceed`.

**Observation:** The 117 GB USB pendrive was correctly identified and selected for the recovery process.

---

### Step 3: Analyse the Disk

After selecting the USB pendrive, TestDisk displays the main menu.

The available options include:

- Analyse
- Advanced
- Geometry
- Options
- MBR Code
- Delete
- Quit

Select `Analyse` to analyse the current partition structure and search for lost partitions.

**Observation:** The Analyse option was selected to search for the deleted partition.

---

### Step 4: Perform Quick Search

1. TestDisk displays the current partition structure of the USB pendrive.
2. The existing `SARATH'S` partition is displayed.
3. Select `Quick Search` and press **Enter**.

**Observation:** TestDisk started searching for lost or deleted partitions.

---

### Step 5: Verify the Deleted Partition

1. TestDisk detects the deleted `Testing` partition.
2. Select the `Testing` partition.
3. Press `P` to list the files stored in the selected partition.

**Observation:** TestDisk successfully displayed the files from the deleted `Testing` partition. The displayed files included images and screenshots that were previously stored in the partition.

#### Examples of Detected Files

- `1.jpg`
- `2345.jpg`
- `Screenshot 2026-09-07 203856.png`
- `WIN_20250914_21_21_06_Pro.jpg`
- `WIN_20251207_20_53_37_Pro.jpg`
- `WIN_20251208_13_29_03_Pro.jpg`

This confirms that the deleted partition and its file system data were successfully detected.

Press `q` to return to the partition list.

---

### Step 6: Confirm the Recovered Partition

After returning to the partition list, TestDisk displays both the deleted `Testing` partition and the existing `SARATH'S` partition.

The detected partition structure is:

- `Testing` – approximately 4 GB
- `SARATH'S` – approximately 113 GB

The screen displays:

`Structure: Ok.`

**Observation:** The deleted `Testing` partition was successfully detected, and the partition structure was reported as OK.

Press **Enter** to continue.

---

### Step 7: Write the Recovered Partition Structure

TestDisk provides the `Write` option to save the detected partition structure to the USB pendrive.

1. Select `Write`.
2. Press **Enter**.
3. Confirm the operation when TestDisk asks for confirmation.

**Observation:** The recovered partition structure was selected to be written back to the USB pendrive.

---

## RESULT

The deleted 4 GB `Testing` partition was successfully detected using TestDisk. The files stored in the deleted partition were successfully displayed using the `P` option, confirming that the partition data was recoverable.

---

## RUBRICS

| S.No. | Criteria | Marks Allotted | Marks Awarded |
|---|---|---|---|
| 1 | GitHub Activity & Submission Regularity | 3 | |
| 2 | Application of Forensic Tools & Practical Execution | 3 | |
| 3 | Documentation & Reporting | 2 | |
| 4 | Engagement, Problem-Solving & Team Collaboration | 2 | |
| | **Total** | **10** | |

<img width="1538" height="1022" alt="ChatGPT Image Sep 29, 2026, 10_10_18 AM" src="https://github.com/user-attachments/assets/a27a9e68-fb9a-47b8-9c7a-81de8bec76f0" />
<img width="1573" height="1000" alt="ChatGPT Image Sep 29, 2026, 10_09_14 AM" src="https://github.com/user-attachments/assets/b4eb1f27-2c2a-41e7-81b9-5336dc6e0377" />
<img width="1572" height="1001" alt="ChatGPT Image Sep 29, 2026, 10_08_23 AM" src="https://github.com/user-attachments/assets/651d0ca3-ccdf-4e67-a474-97d0ede7e89b" />
<img width="1554" height="1012" alt="ChatGPT Image Sep 29, 2026, 10_06_54 AM" src="https://github.com/user-attachments/assets/e5bfbed1-0170-4808-a3de-f86847097a0a" />
<img width="1557" height="1010" alt="ChatGPT Image Sep 29, 2026, 09_51_39 AM" src="https://github.com/user-attachments/assets/d46734c3-4ff5-4395-9bef-3a6a916fe71c" />
<img width="1566" height="1005" alt="ChatGPT Image Sep 29, 2026, 09_50_31 AM" src="https://github.com/user-attachments/assets/10b62a31-bfdb-483e-8b66-dba4e6fcb7e6" />
<img width="1570" height="1002" alt="ChatGPT Image Sep 29, 2026, 09_46_42 AM" src="https://github.com/user-attachments/assets/19ea3f9d-5ff9-46ba-8523-c9ccba0afe2b" />
