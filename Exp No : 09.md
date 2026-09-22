# Ex.No.9 – Use Process Explorer to Identify Suspicious Processes

## Aim

To use Process Explorer to identify and investigate suspicious processes running on a Windows system.

## Description

Process Explorer is a Windows tool that provides detailed information about running processes. It can be used to monitor processes, troubleshoot system issues, and detect potentially suspicious or harmful activities.

## Requirements

- Windows Computer/Laptop
- Process Explorer
- Internet Connection
- Antivirus/Malware Detection Tool

## Procedure

### Step 1: Download and Set Up Process Explorer

1. Download Process Explorer from the official Microsoft Sysinternals website.
2. Extract the downloaded ZIP file.
3. Open the extracted folder.
4. Run `procexp64.exe` for a 64-bit system or `procexp.exe` for a 32-bit system.
5. Run the program as Administrator.

### Step 2: Familiarize Yourself with the Interface

Process Explorer displays all running processes along with information such as:

- Process ID (PID)
- CPU Usage
- Memory Usage
- Process Hierarchy
- Description
- Company Name

The process tree shows parent and child processes.

### Process Colors

- Pink: Suspended processes
- Light Blue: Processes running under the current user
- Dark Blue: Services or processes running under system accounts
- Green: Newly created processes
- Red: Recently exited processes

### Step 3: Identify Suspicious Processes

#### 1. Look for Unfamiliar Processes

Check the list of running processes and identify process names that are unfamiliar or unusual.

Legitimate processes are generally associated with trusted companies such as Microsoft, Intel, or Adobe.

#### 2. Verify Digital Signatures

1. Right-click the suspicious process.
2. Select `Properties`.
3. Open the `Image` tab.
4. Check the Digital Signature.

An invalid or missing signature may require further investigation.

#### 3. Check the Process Path

1. Open the process `Properties`.
2. Go to the `Image` tab.
3. Check the process path.

Legitimate Windows system processes commonly run from:

    C:\Windows\System32

A process running from an unexpected temporary, user, or random directory may require investigation.

#### 4. Monitor CPU, Memory, and Disk Usage

Check the CPU, Memory, and Disk usage of the process.

A process using unusually high system resources without an obvious reason may be suspicious.

#### 5. Check Process Description and Company Name

Check the Description and Company Name columns.

Legitimate processes generally contain valid descriptions and recognizable company information.

#### 6. Check Network Activity

1. Right-click the suspicious process.
2. Select `Properties`.
3. Open the `TCP/IP` tab.
4. Check the network connections associated with the process.

Unexpected external connections may require further investigation.

### Step 4: Search for Information About Suspicious Processes

If an unfamiliar process is found:

1. Search the process name on Google.
2. Check trusted malware databases.
3. Use services such as VirusTotal or ProcessLibrary.
4. Compare the process information with known legitimate processes.

### Step 5: Kill or Suspend Suspicious Processes

If a process is confirmed to be malicious:

#### Kill the Process

Right-click the suspicious process and select:

    Kill Process

#### Suspend the Process

If further investigation is required, right-click the process and select:

    Suspend

#### Remove the Source File

1. Open the process Properties.
2. Check the file Path.
3. Locate the executable file.
4. Delete it only after confirming that it is malware.

### Step 6: Scan the System

After dealing with a suspicious process:

1. Run a full antivirus scan.
2. Use Windows Defender or another trusted antivirus.
3. Use a malware removal tool such as Malwarebytes.
4. Review the system again for suspicious processes.

## Example

Suppose a process named:

    randomname123.exe

is using unusually high CPU resources.

The investigation can be performed as follows:

1. Open Process Explorer.
2. Locate `randomname123.exe`.
3. Check its CPU and memory usage.
4. Open Properties.
5. Check its digital signature.
6. Check its file path.
7. Check the TCP/IP connections.
8. Search the process name online.
9. Verify whether it is associated with malware.
10. If confirmed as malicious, terminate the process and remove the malicious executable.
11. Perform a full antivirus scan.

## Important Commands/Actions

    Run Process Explorer as Administrator

    Right-click → Properties

    Image → Check Digital Signature

    Image → Check Process Path

    TCP/IP → Check Network Activity

    Right-click → Kill Process

    Right-click → Suspend

## Result

The Process Explorer tool was successfully used to examine running processes and identify potentially suspicious processes based on process name, digital signature, file path, resource usage, company information, and network activity.

## Conclusion

Process Explorer is useful for investigating running Windows processes and detecting potentially suspicious activities. By examining process properties, digital signatures, file paths, resource usage, and network connections, suspicious processes can be identified and investigated.

<img width="592" height="441" alt="9 aa" src="https://github.com/user-attachments/assets/30f570ff-f882-4d82-8491-368266308a48" />
<img width="1920" height="1080" alt="9 bb" src="https://github.com/user-attachments/assets/52377222-05f3-4633-a8a9-196f37f69686" />
<img width="714" height="900" alt="9 cc" src="https://github.com/user-attachments/assets/945163df-f087-4576-88a1-370278d3a04a" />
<img width="694" height="858" alt="9 dd" src="https://github.com/user-attachments/assets/09bfb263-7242-484f-affc-c1d13cb8f989" />
<img width="703" height="914" alt="9 gg" src="https://github.com/user-attachments/assets/c4b4988a-6e63-49f4-a8a9-bedab4d949c0" />
<img width="565" height="469" alt="9 ee" src="https://github.com/user-attachments/assets/ad80db80-7ebd-443b-b037-dd399e171168" />
<img width="1169" height="889" alt="9 ff" src="https://github.com/user-attachments/assets/8f134a95-38e6-411b-b8f8-32a0eb6f90ff" />
<img width="533" height="326" alt="image" src="https://github.com/user-attachments/assets/e0114a5b-ce87-4d2b-ba90-468cb6389fdc" />

