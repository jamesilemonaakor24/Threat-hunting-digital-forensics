# Chain of Custody Record

## Case Information

| Field | Details |
|---|---|
| Case Number | Lab-001 |
| Examiner | James Ilemona Akor |
| Examination Type | Digital Forensics Investigation |
| Primary System | WKSTN11 |
| Operating System | Windows 11 |
| Evidence No. | 001 |

## Evidence Description

| Field | Details |
|---|---|
| Evidence Type | Forensic Disk Image |
| Filename | WKSTN11_DiskImage_1AUG2026.E01 |
| Acquisition Date | 1 August 2026 |
| Acquisition Time | 9:35 PM |
| Acquisition Tool | FTK Imager 4.7.1.2 |
| Verification | Acquisition hash matched verification hash |
| Verification Result | MATCH |
| Bad Blocks | None detected |

## Memory Evidence

| Field | Details |
|---|---|
| Evidence Type | RAM Capture |
| Filename | WKSTN11_RAMcapture_1AUG2026.raw |
| Capture Date | 1 August 2026 |
| Transfer to Host | 1 August 2026, 7:55 PM |
| SHA-256 | `51b111a9447b13d69d42b10d2d06e03324cff07cc63e4938c7f9dd8eda9305b7` |

## Evidence Handling Log

| Date | Time | Action | From | To | Purpose |
|---|---|---|---|---|---|
| 1 Aug 2026 | 7:52 PM | RAM acquisition initiated | WKSTN11 | Examiner | Volatile evidence collection |
| 1 Aug 2026 | 7:55 PM | RAM capture transferred | WKSTN11 | Host system | Preservation and analysis |
| 1 Aug 2026 | 9:35 PM | Disk image acquired | WKSTN11 | Host storage | Forensic acquisition |
| 1 Aug 2026 | 9:35 PM | Disk image verified | Host storage | Examiner | Integrity verification |
| 1 Aug 2026 | 9:45 PM | E01 loaded into Autopsy | Host storage | Autopsy | Forensic examination |

## Integrity Verification

The forensic disk image was verified using FTK Imager. The computed acquisition hash matched the stored verification hash, and the verification result was reported as **Match**. FTK Imager also reported that no bad blocks were found in the image.

The RAM capture was independently recorded using the SHA-256 value shown above.

## Examination Record

The verified E01 image was loaded into Autopsy for examination. Analysis included Windows artefacts, recent documents, browser artefacts, operating system information, deleted files, file-system information, USB device artefacts, and other relevant forensic artefacts.

## Examiner Declaration

I certify that the evidence handling and examination activities recorded above represent the procedures performed during this investigation and that the integrity verification results were recorded from the forensic tools used during acquisition and examination.

**Examiner:** James Ilemona Akor  
**Case:** Lab-001
