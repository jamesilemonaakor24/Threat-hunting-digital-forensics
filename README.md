# Threat Hunting & Digital Forensics Investigation

A practical digital forensics and threat hunting investigation conducted in a controlled Windows lab environment.

The investigation focused on identifying, preserving, acquiring, examining, and correlating digital evidence to understand suspicious activity on a Windows workstation.

> **📄 Investigation Report & Visual Evidence**
>
> The **complete investigation report contains the supporting screenshots, tool outputs, forensic evidence, analysis, and documented findings** from the investigation.
>
> **[Download / Open the Complete Investigation Report (PDF)](James_Ilemona_Akor_DFIR_Investigation.pdf)**
>
> If GitHub does not display the PDF correctly in the browser or shows an **"Unable to render code block"** message, please **download the PDF and open it locally**. The report itself is intact, and the complete visual evidence is contained within the PDF.

## Table of Contents

- [Investigation Overview](#investigation-overview)
- [Investigation Workflow](#investigation-workflow)
- [Case Information](#case-information)
- [Evidence Acquisition](#evidence-acquisition)
- [Forensic Examination](#forensic-examination)
- [Memory Forensics](#memory-forensics)
- [Steganography & Hidden Content Analysis](#steganography--hidden-content-analysis)
- [Metadata Analysis](#metadata-analysis)
- [Evidence Integrity & Chain of Custody](#evidence-integrity--chain-of-custody)
- [Investigation Documentation](#investigation-documentation)
- [Investigation Report](#investigation-report)
- [Tools Used](#tools-used)
- [Skills Demonstrated](#skills-demonstrated)
- [Key Investigative Principle](#key-investigative-principle)
- [Repository Structure](#repository-structure)

## Investigation Overview

This investigation followed a structured forensic workflow rather than isolated tool demonstrations.

The main objectives were to:

- Analyse Windows security and system events
- Acquire and preserve digital evidence
- Verify the integrity of acquired forensic evidence
- Perform memory forensics
- Examine a forensic disk image
- Recover and analyse relevant files and artefacts
- Investigate hidden information using steganography analysis
- Examine file metadata
- Correlate findings from multiple evidence sources
- Document evidence handling and investigative decisions

The investigation was designed to demonstrate how an analyst can move from individual artefacts to a broader understanding of activity by correlating evidence from different sources.

## Investigation Workflow

The investigation followed this workflow:

**Identify → Preserve → Acquire → Verify → Examine → Analyse → Correlate → Document → Conclude**

Each stage was supported by investigative notes, tool output, screenshots, and evidence records where applicable.

## Case Information

| Field | Details |
|---|---|
| Case Number | LAB-001 |
| Evidence Number | 001 |
| Examiner | James Ilemona Akor |
| Investigation Date | 1 August 2026 |
| Primary System | Windows 11 Workstation |
| Forensic Image | `WKSTN11_DiskImage_1AUG2026.E01` |
| Autopsy Case | `WKSTN11 DiskImage` |

## Evidence Acquisition

### Memory Acquisition

A RAM capture was acquired from the Windows workstation and transferred to the host system for analysis.

**RAM capture:**

`WKSTN11_RAMcapture_1AUG2026.raw`

**Acquisition date:** 1 August 2026  
**Transfer time:** 7:55 PM

**SHA-256:**

`51b111a9447b13d69d42b10d2d06e03324cff07cc63e4938c7f9dd8eda9305b7`

The same SHA-256 value was recorded for the VM RAM capture and the transferred host copy, supporting integrity verification of the transferred evidence.

### Disk Image Acquisition

A forensic disk image of the Windows workstation was acquired using FTK Imager.

**Image filename:**

`WKSTN11_DiskImage_1AUG2026.E01`

**Acquisition time:** 9:35 PM, 1 August 2026

The acquired image was verified immediately after acquisition using FTK Imager.

The verification result showed:

**Verify result: Match**

The verification screen also reported that no bad blocks were found in the image.

The verification evidence is retained in the investigation report.

## Forensic Examination

The forensic disk image was loaded into Autopsy for examination.

**Autopsy case:** `WKSTN11 DiskImage`

**Image loaded:** 9:45 PM, 1 August 2026

The examination included review of:

- Operating system information
- User accounts
- Recent documents
- Run programs
- Browser artefacts
- USB device history
- Web history and downloads
- File metadata
- Deleted files
- File-system artefacts
- Extension mismatches
- Other relevant forensic artefacts

The objective was not simply to identify individual artefacts, but to determine what those artefacts could establish when considered together.

## Memory Forensics

Memory analysis was performed against the acquired RAM image to identify artefacts that may not be available from disk evidence alone.

The analysis formed part of the wider investigation and was correlated with findings from the disk image and Windows system activity.

Memory analysis included examination of running processes and network-related artefacts, providing additional context for the state of the workstation at the time of acquisition.

The detailed analysis and supporting screenshots are included in the investigation report.

## Steganography & Hidden Content Analysis

Hidden-content analysis was performed using steganography tools to determine whether information had been concealed within files.

QuickStego and related examination techniques were used as part of this analysis.

The exercise demonstrated the importance of considering whether apparently ordinary files may contain information that is not immediately visible during normal examination.

Supporting evidence is included in the investigation report.

## Metadata Analysis

File metadata was examined to identify information that could provide additional investigative context, including file properties and timestamps where available.

ExifTool was used to support metadata examination.

The analysis demonstrated how image metadata can expose information such as:

- File characteristics
- Creation or modification information
- Camera-related information
- Author or software information
- Potential location-related metadata where present

From a security perspective, metadata can become a source of unintended information disclosure when files are published publicly.

The supporting ExifTool command output and screenshots are included in the investigation report.

## Evidence Integrity & Chain of Custody

Evidence handling was documented throughout the investigation.

The chain-of-custody record identifies:

- Case and evidence numbers
- Evidence descriptions
- Acquisition and transfer activities
- Evidence handling times
- Examiner information
- Integrity verification details

The completed chain-of-custody documentation is available in:

[`Chain-of-Custody/`](Chain-of-Custody/)

## Investigation Documentation

Detailed investigative notes, evidence observations, analysis results, and conclusions are documented in:

[`Evidence/Investigation-Documentation.md`](Evidence/Investigation-Documentation.md)

## Investigation Report

The complete investigation report is the primary visual evidence package for this repository.

It contains:

- Investigation methodology
- Evidence acquisition records
- Hash verification evidence
- FTK Imager verification screenshots
- Autopsy examination evidence
- Memory-forensics evidence
- Volatility analysis
- File-system examination
- File recovery evidence
- Steganography examination
- ExifTool metadata analysis
- Supporting screenshots and command output
- Investigative findings
- Evidence correlation
- Conclusions and recommendations

### 📄 Complete Report

**[Download / Open James Ilemona Akor — DFIR Investigation Report](James_Ilemona_Akor_DFIR_Investigation.pdf)**

> **Note:** GitHub's browser-based PDF viewer may occasionally fail to render this document and display an **"Unable to render code block"** message. This does **not** mean that the investigation report is corrupted.
>
> If the report does not open or render in GitHub, **download the PDF and open it locally using a PDF reader such as Microsoft Edge, Adobe Acrobat Reader, or another PDF viewer**.
>
> **All supporting visual evidence from the investigation is contained within the PDF.**

## Tools Used

- Windows 11
- Kali Linux
- FTK Imager
- Autopsy
- Volatility
- QuickStego
- ExifTool
- Windows Event Viewer
- Command Prompt
- Oracle VirtualBox

## Skills Demonstrated

### Digital Forensics

- Evidence acquisition
- Evidence preservation
- Hash verification
- Disk and file-system examination
- Memory forensics
- File recovery
- Metadata analysis
- Steganography analysis

### Threat Hunting

- Windows event analysis
- Authentication and system-event examination
- Identification of suspicious activity
- Evidence correlation
- Investigative reasoning

### Evidence Handling

- Chain-of-custody documentation
- Evidence identification and tracking
- Integrity verification
- Documentation of investigative actions
- Maintaining evidence integrity

## Key Investigative Principle

The investigation did not rely on a single artefact.

Findings were considered across multiple evidence sources, including Windows event information, memory, disk evidence, file information, metadata, and hidden-content analysis.

This approach helped establish a more complete picture of activity on the investigated Windows workstation.

A key lesson from the investigation is that individual artefacts often provide only partial context. Stronger conclusions can be developed by correlating independent evidence sources and considering whether the available evidence supports or contradicts a particular hypothesis.

## Repository Structure

```text
Threat-hunting-digital-forensics/
│
├── README.md
│
├── Chain-of-Custody/
│   ├── Chain-of-Custody-Record.md
│   └── James_Ilemona_Akor_Chain_of_Custody_...
│
├── Evidence/
│   └── Investigation-Documentation.md
│
└── James_Ilemona_Akor_DFIR_Investigation.pdf
