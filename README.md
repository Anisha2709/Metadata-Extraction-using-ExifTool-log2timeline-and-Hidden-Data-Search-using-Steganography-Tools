# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools
## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps
# A. Using ExifTool – for file metadata

 Install:
```
sudo apt update
sudo apt install exiftool -y
```
 Extract metadata from a file:
```
exiftool image.jpg
```
 Batch process a folder:
```
exiftool -r /path/to/folder
```
Useful flags:

-G: Show metadata group

-time:all: Show only timestamps

-GPSLatitude -GPSLongitude: Extract GPS data

![image](https://github.com/user-attachments/assets/75dc64ee-7af7-4765-9ecf-0ee8eafec4af)

# install log2timeline
```
sudo apt install plaso -y
```
```
sudo apt install steghide -y
```
# Embed data
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
![image](https://github.com/user-attachments/assets/47166c87-4abe-4226-9529-141f1f602ec9)

Extract hidden data:
```
steghide extract -sf hidden.jpg
```
![image](https://github.com/user-attachments/assets/f7d8e853-d26b-4226-93f2-ccd5d73b9de3)

# Using binwalk – for file analysis

```
sudo apt install binwalk -y
binwalk suspicious.jpg
```
![image](https://github.com/user-attachments/assets/7fcc7fe9-bf17-47e5-9405-3800b294a7ea)

## OUTPUT:
Extracted Metadata, Timeline Events, and Hidden Data Detection Results
![image](https://github.com/user-attachments/assets/3273ce33-c3bf-4929-9fc4-b2056c1cf075)

## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

