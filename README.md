### Batch Folder Sorter

Batch Folder Sorter is a desktop application designed to automatically generate a correct folder structure for ingest workflows based on a CSV metadata file. The tool was created to work in combination with systems such as Instroomtool, where a consistent and validated folder structure is required before upload.

### How It Works

The application takes a single folder containing files and a CSV file as input. The CSV acts as the authoritative source for the structure: the column `Mapnaam` defines which folders need to be created.

Users do not create folders manually. During processing, the application:

1. You select a **ROOT folder**  
   → this is the folder that contains the files you want to sort  

2. You select a **CSV metadata file**  
   → the CSV must contain a column named **`Mapnaam`**, which defines the target folder names  

3. Click **RUN**  
   → the application automatically creates folders and moves files according to the CSV  

No coding, no terminal, no configuration files required.


- Reads the CSV file  
- Automatically creates the required folders  
- Matches files to those folders based on their filenames  

Files are grouped under folders named after the values in the `Mapnaam` column.

Within each folder, the application automatically creates subfolders per file format (for example `jpg`, `tiff`, `png`, --> whole white list Instroomtool). This allows different representations of the same item to be kept together in a clear and predictable structure. Multiple formats per item are supported, and formats are detected automatically.

### File Validation

Only supported file formats are processed.

Files that:
- Do not match the CSV  
- Use unsupported formats  

are collected in a separate `_EXTRA_FILES` folder. This makes it easy to review unexpected files without breaking the main structure.

Empty folders are removed automatically, ensuring that the final output is clean and consistent.

### Output

The resulting folder structure is ready for direct use in ingest workflows such as Instroomtool. No additional restructuring or manual intervention is required after processing.

All actions happen locally on the user’s machine. No data is uploaded or shared. The application does not require Python or any additional software to be installed by the end user.

### Availability

Batch Folder Sorter is provided as a ready-to-use desktop application for:

- macOS  
- Windows (ARM and x64 variants)  

Users simply download the version matching their operating system, launch the application, select their files and CSV, and run the process.

---

## Downloads & Installation --> https://github.com/9elmaz9/folderify/releases/tag/v1.0


### Windows 
- Download: `BatchFolderSorter-win-x64.exe` ( of download - `BatchFolderSorter_Windows_ARM.exe` for windows RAM) 
- Double-click to run  
- If Windows shows a security warning, choose **More info → Run anyway**

### macOS
- Download: `BatchFolderSorter.app.zip`
- Unzip the file
- Move **Batch Folder Sorter.app** to the **Applications** folder
- On first launch: right-click → **Open** (macOS security requirement)

---

## ⚠️ Important Notes

- This is the **first stable release (v1.0)**  
- On macOS and Windows, security warnings may appear because the app is not signed  
- The application does **not upload or share any data** — all processing happens locall
- Works completely offline  
- No Python installation required  
- No additional software required  
- All processing happens locally  
- No data is uploaded anywhere  
- No external services are used  

---

## Future improvements (planned)

- Visual theme improvements
- Better progress indicators
- Extended CSV validation
- Alternative front-end (web-based UI)




<div align="center">

<h3>For Windows</h3>
<img src="https://github.com/user-attachments/assets/f0d4adc5-a723-4f8e-ab30-d5231bb86ff9" width="800">
<br><br>

<h3>For macOS</h3>
<img src="https://github.com/user-attachments/assets/816d7269-cbd2-4005-9f68-a59ca9d7899a" width="800">
<img src="https://github.com/user-attachments/assets/67326f62-f20e-4cb8-9e43-b7ac6c54591c" width="800">
<br><br>



<!--
<div align="center">
  <img src="https://github.com/user-attachments/assets/116e39c3-f580-40c8-819c-379a02a2c978" height="400">
    <span style="font-size:40px; margin: 0 20px;">→</span>
  <img src="https://github.com/user-attachments/assets/08668f81-44a5-4e65-9177-ef2a42f93a67" height="400">
  <img src="https://github.com/user-attachments/assets/e160bb1d-be0f-4730-bb60-bcd089d350f2" height="400">
</div>
-->
<br>



<div align="center">
  <img src="https://github.com/user-attachments/assets/116e39c3-f580-40c8-819c-379a02a2c978" height="400">
  &nbsp;&nbsp; ➜ &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/08668f81-44a5-4e65-9177-ef2a42f93a67" height="400">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/e160bb1d-be0f-4730-bb60-bcd089d350f2" height="400">
</div>

