# Ex.No.7 – Use AFLogical OSE to Extract Data from an Android Device

## Aim

To use AFLogical OSE (Open Source Edition) to extract data from an Android device.

## Description

AFLogical OSE is an open-source Android forensic tool used for logical extraction of data from Android devices. It can extract data such as contacts, SMS, MMS, and call logs.

## Requirements

- Android Device
- Computer/Laptop
- USB Cable
- Java
- Android Debug Bridge (ADB)
- AFLogical OSE
- USB Debugging enabled on Android device

## Procedure

### Step 1: Prepare the Environment

1. Download AFLogical OSE.
2. Install Java on the computer.
3. Install Android Debug Bridge (ADB).
4. Add ADB to the system PATH.
5. Enable Developer Options on the Android device.
6. Enable USB Debugging.

### Step 2: Connect the Android Device

Connect the Android device to the computer using a USB cable.

Open Command Prompt or Terminal and run:

    adb devices

If the Android device appears in the list, the ADB connection is successful.

### Step 3: Install AFLogical OSE

Navigate to the directory containing the AFLogical APK and run:

    adb install aflogical.apk

After installation, open the AFLogical application on the Android device.

Select the required data types:

- Contacts
- SMS
- MMS
- Call Logs

Start the extraction process.

The extracted data will be stored in CSV files in the `aflogical` directory.

### Step 4: Transfer Extracted Data

Use ADB to copy the extracted data from the Android device to the computer:

    adb pull /sdcard/aflogical /path/to/destination

Replace `/path/to/destination` with the destination folder on your computer.

### Step 5: Analyze the Extracted Data

Open the extracted CSV files using:

- Microsoft Excel
- Google Sheets
- Text Editor

Analyze the extracted:

- Contacts
- SMS
- MMS
- Call Logs

Document the findings for further forensic analysis.

### Step 6: Clean Up

After completing the extraction, uninstall AFLogical OSE using:

    adb uninstall com.viaforensics.android.aflogical

Finally, safely disconnect the Android device from the computer.

## Commands Used

    adb devices

    adb install aflogical.apk

    adb pull /sdcard/aflogical /path/to/destination

    adb uninstall com.viaforensics.android.aflogical

## Result

The logical data from the Android device was successfully extracted using AFLogical OSE and stored in CSV files for further forensic analysis.

## Conclusion

AFLogical OSE was successfully used to perform logical extraction of Android data such as contacts, messages, MMS, and call logs.

<img width="1233" height="695" alt="1" src="https://github.com/user-attachments/assets/df8e5dce-0aa5-4e41-98f3-e7a501fb5967" />
<img width="1600" height="533" alt="2" src="https://github.com/user-attachments/assets/9e55064e-b7f7-46b4-9ceb-7ef2eded4f59" />
<img width="1192" height="362" alt="3" src="https://github.com/user-attachments/assets/89aea77a-e644-4670-a48c-9c03d7d2f0be" />
<img width="1076" height="235" alt="4" src="https://github.com/user-attachments/assets/d36fa651-a563-43b8-be5c-44796a4b0f92" />
<img width="1190" height="207" alt="5" src="https://github.com/user-attachments/assets/efab2221-cfd5-42ec-b154-c809076bd19f" />
<img width="1600" height="533" alt="6" src="https://github.com/user-attachments/assets/1d654a32-bdc0-4b96-9ecb-1399fa565941" />
<img width="1747" height="132" alt="7" src="https://github.com/user-attachments/assets/c594f981-01d8-4dd7-a53e-42525138c8cf" />
<img width="1907" height="985" alt="8" src="https://github.com/user-attachments/assets/9493ea1f-5ef8-4143-946c-640252da1650" />
