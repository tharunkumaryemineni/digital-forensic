# Ex.No.8 – StegExpose: Detect Hidden Data in Images

## Aim

To use StegExpose to detect hidden data embedded in images using steganography analysis.

## Description

StegExpose is a tool used to detect hidden data in images. It analyzes the statistical properties of an image and calculates a suspect score to estimate whether steganography is present.

## Requirements

- Java Runtime Environment (JRE)
- StegExpose `.jar` file
- Windows / Linux / macOS
- Image files such as PNG, JPG, BMP

## Installation

### 1. Install Java

Check whether Java is installed:

    java -version

### 2. Download StegExpose

Download the StegExpose `.jar` file from its official GitHub repository.

Place `StegExpose.jar` in your working folder.

## Procedure

### Step 1 – Prepare StegExpose

Keep the `StegExpose.jar` file in the same folder where your image files are available.

### Step 2 – Select an Image

Choose an image that you want to analyze for hidden data.

Example:

    test_image.png

### Step 3 – Open Command Prompt

Open Command Prompt or Terminal and navigate to the folder containing `StegExpose.jar`.

Example:

    cd path/to/your/folder

### Step 4 – Analyze a Single Image

Run the following command:

    java -jar StegExpose.jar test_image.png

Replace `test_image.png` with the actual image filename.

### Step 5 – Analyze the Result

StegExpose generates a suspect score between 0 and 1.

| Score | Interpretation |
|---|---|
| Less than 0.2 | Image is clean |
| 0.2 – 0.3 | Possibly contains hidden data |
| Above 0.3 | Steganography is likely present |

### Step 6 – Batch Analysis

To analyze multiple images in a folder:

    java -jar StegExpose.jar <folder_path>

Example:

    java -jar StegExpose.jar images

### Step 7 – View Help

To view the available options:

    java -jar StegExpose.jar --help

## Example

Command:

    java -jar StegExpose.jar suspect_image.png

Example output:

    Analyzing suspect_image.png...
    Result: 0.4
    Steganography likely present

A score of `0.4` indicates that hidden data is likely present in the image.

## Result

The image was successfully analyzed using StegExpose, and the suspect score was used to determine the likelihood of hidden steganographic data.

## Conclusion

StegExpose can be used as a digital forensics tool to analyze images and identify images that may contain hidden data using steganography detection techniques.

## Commands Used

    java -version

    cd path/to/your/folder

    java -jar StegExpose.jar test_image.png

    java -jar StegExpose.jar <folder_path>

    java -jar StegExpose.jar --help

<img width="950" height="539" alt="Screenshot 2026-09-22 224640" src="https://github.com/user-attachments/assets/965b48a5-df45-4bc5-843a-c8cd9915aba3" />
<img width="866" height="599" alt="8 b" src="https://github.com/user-attachments/assets/815e22e9-6c68-47e7-8737-06ea43949483" />
<img width="478" height="239" alt="8 c" src="https://github.com/user-attachments/assets/82a2a080-20dd-49d2-b474-7f6aece1d292" />
<img width="331" height="165" alt="8 d" src="https://github.com/user-attachments/assets/c1ddef0a-d7fc-412b-bd7b-c3f62958cae2" />
<img width="959" height="349" alt="8 e" src="https://github.com/user-attachments/assets/2b742911-5390-4a45-abc6-438d7874ea26" />
<img width="959" height="349" alt="8 e - Copy" src="https://github.com/user-attachments/assets/44ad8a88-d6e9-415f-b201-7adff1a4552c" />
