# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report
<img width="1598" height="839" alt="1" src="https://github.com/user-attachments/assets/2c52a39b-30eb-434d-8e5a-458e4f52aaae" />
<img width="1600" height="846" alt="2" src="https://github.com/user-attachments/assets/6723aab1-58b4-4094-8afc-0cb633c7ed78" />
<img width="1600" height="834" alt="3" src="https://github.com/user-attachments/assets/42c973b5-334c-454f-ac95-86bd0e820333" />
<img width="1600" height="843" alt="4" src="https://github.com/user-attachments/assets/faae1b0c-c148-4b21-8a9b-e9637463993c" />
<img width="1600" height="849" alt="5" src="https://github.com/user-attachments/assets/ad5bfaf4-a4c3-4a38-91ec-32749af75828" />
<img width="1600" height="734" alt="6" src="https://github.com/user-attachments/assets/350e01e6-c0e1-49cd-b16e-24a892ca2870" />
<img width="1600" height="687" alt="7" src="https://github.com/user-attachments/assets/84d70323-c21b-4e3d-8d99-f6980d6a47c3" />


## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

