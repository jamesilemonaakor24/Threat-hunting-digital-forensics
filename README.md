# Threat Hunting & Digital Forensics Investigation

A hands-on digital forensics and threat hunting investigation focused on identifying, preserving, and analysing digital evidence from a Windows environment.

The investigation covers Windows event analysis, evidence acquisition and preservation, memory forensics, disk forensics, steganography, metadata analysis, file recovery, and chain of custody.

## Investigation Overview

This project was built around a practical investigation workflow rather than isolated tool demonstrations.

The investigation involved:

- Reviewing Windows security and system events for suspicious activity
- Identifying and preserving relevant digital evidence
- Acquiring forensic images for analysis
- Performing memory analysis to identify artefacts of interest
- Examining disk evidence and recovering relevant files
- Investigating hidden information using steganography techniques
- Extracting and analysing file metadata
- Documenting evidence handling through a chain of custody
- Correlating findings from different forensic sources
- Recording observations and conclusions throughout the investigation

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

## Key Skills Demonstrated

### Digital Forensics
- Evidence acquisition
- Evidence preservation
- Disk and file-system examination
- Memory forensics
- File recovery
- Metadata analysis
- Steganography analysis

### Threat Hunting
- Windows event analysis
- Identification of suspicious activity
- Examination of authentication and system events
- Evidence correlation
- Investigative reasoning

### Evidence Handling
- Chain of custody documentation
- Evidence identification and tracking
- Hash verification
- Maintaining evidence integrity
- Documenting investigative actions and findings

## Investigation Workflow

The investigation followed a structured process:

**Identify → Preserve → Acquire → Examine → Analyse → Correlate → Document → Conclude**

Each stage was documented with supporting evidence where appropriate.

## Evidence & Documentation

The repository contains supporting documentation and screenshots from the investigation, including:

- Investigation procedures
- Forensic analysis results
- Tool outputs
- Evidence-handling records
- Screenshots demonstrating investigative steps
- Chain of custody documentation
- Investigation conclusions

The purpose of the supporting evidence is to show not only the final result, but how the investigation was carried out.

## Investigation Outcome

The investigation demonstrated how multiple sources of digital evidence can be examined together to build a clearer understanding of activity on a Windows system.

Rather than relying on a single forensic artefact, the investigation used event data, memory, disk evidence, file information, metadata, and hidden-content analysis to support investigative conclusions.

This approach reflects the importance of preserving evidence, validating findings, and documenting the reasoning behind an investigation.

## Why This Project Matters

Digital forensics and threat hunting require more than knowing how to run security tools. An investigator needs to understand what evidence is relevant, preserve it correctly, interpret the results, and communicate findings clearly.

This project was built to demonstrate that process from evidence acquisition through analysis and final documentation.

## Repository Structure

```text
Threat-hunting-digital-forensics/
│
├── README.md
│
├── Documentation/
│   └── Investigation Guide
│
├── Evidence/
│   └── Investigation Evidence
│
├── Screenshots/
│   └── Investigation Screenshots
│
└── Chain-of-Custody/
    └── Chain of Custody Records
