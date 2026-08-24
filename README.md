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
<img width="1122" height="1001" alt="Screenshot 2026-08-23 122739" src="https://github.com/user-attachments/assets/170a619f-0e96-4704-8958-55f75f605f87" />
<img width="937" height="996" alt="Screenshot 2026-08-23 123447" src="https://github.com/user-attachments/assets/900ad0d7-8f0e-47e3-b894-f4687126be61" />
<img width="1143" height="1003" alt="Screenshot 2026-08-24 184045" src="https://github.com/user-attachments/assets/f9c5b01d-b2d8-4866-ab48-a05c83a19d96" />
<img width="1919" height="1012" alt="Screenshot 2026-08-24 184239" src="https://github.com/user-attachments/assets/799417e3-7eea-45d5-82de-4e2dcad3ab4c" />
<img width="1919" height="1016" alt="Screenshot 2026-08-24 184145" src="https://github.com/user-attachments/assets/959c8139-10ac-48d8-9a52-5ec7c16c084a" />
 /><img width="951" height="984" alt="Screenshot 2026-08-24 185140" src="https://github.com/user-attachments/assets/c640907e-bbf9-4d1a-9a07-7e83ca44966d" />
<img width="960" height="1052" alt="Screenshot 2026-08-24 185002" src="https://github.com/user-attachments/assets/16c0a6f3-9fed-40bb-9052-2f467180a3cb" />
<img width="1911" height="871" alt="Screenshot 2026-08-24 190732" src="https://github.com/user-attachments/assets/eed909ef-e852-4ba2-bec3-9084cb5204d4" />

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

