# Investigation Evidence & Findings

## Case Overview

**Case Number:** LAB-001  
**Examiner:** James Ilemona Akor  
**Primary System:** WKSTN11  
**Operating System:** Windows 11  
**Investigation Type:** Digital Forensics and Threat Hunting

## Investigation Objective

The objective was to examine a Windows workstation for indicators of suspicious activity and demonstrate a complete forensic workflow from evidence identification and preservation through acquisition, examination, analysis, correlation, and documentation.

The investigation used multiple sources of digital evidence rather than relying on a single artefact.

## Evidence Examined

The investigation included:

- Windows security and system events
- Volatile memory
- Forensic disk image
- File-system and deleted-file artefacts
- Recent document and user activity artefacts
- Browser-related artefacts
- USB device artefacts
- File metadata
- Hidden-content and steganography artefacts
- Recovered files

## Evidence Acquisition

### Volatile Memory

A RAM capture was acquired from the Windows workstation and transferred to the host system for preservation and analysis.

**Filename:** `WKSTN11_RAMcapture_1AUG2026.raw`  
**Capture date:** 1 August 2026  
**Transfer time:** 7:55 PM

**SHA-256:**

`51b111a9447b13d69d42b10d2d06e03324cff07cc63e4938c7f9dd8eda9305b7`

The same SHA-256 value was recorded for the VM RAM capture and the copy transferred to the host, supporting the integrity of the transferred memory evidence.

### Disk Evidence

A forensic disk image was acquired using FTK Imager.

**Filename:** `WKSTN11_DiskImage_1AUG2026.E01`  
**Acquisition date:** 1 August 2026  
**Acquisition time:** 9:35 PM

The image was subsequently verified in FTK Imager. The computed hash matched the stored verification hash and the verification result was reported as **Match**. FTK Imager also reported that no bad blocks were found in the image.

The verified E01 image was loaded into Autopsy at approximately 9:45 PM for forensic examination.

## Forensic Examination

Autopsy was used to examine the acquired disk image and identify relevant Windows artefacts.

The examination included:

- Operating system information
- Recent documents
- Installed programs
- Run-program artefacts
- Shell Bags
- USB device history
- Web history
- Web downloads
- Browser artefacts
- Deleted files
- File-system information
- File-extension inconsistencies
- User and account artefacts

The Autopsy examination identified a number of artefacts requiring further examination, including **337 extension-mismatch results**.

These results were treated as investigative leads rather than automatically classified as malicious activity. File-extension mismatches can have legitimate explanations, so they require contextual examination before drawing a conclusion.

## File Recovery

Deleted and recoverable files were examined as part of the investigation.

A recovered document of interest was identified during the examination and used to demonstrate how deleted or previously removed user files can remain recoverable from forensic disk evidence.

The recovery process demonstrated the importance of examining deleted-file artefacts rather than relying only on currently visible files on a live workstation.

## Memory Forensics

The acquired RAM image was preserved and examined as a separate evidence source.

Memory analysis was used to demonstrate the value of volatile evidence when investigating activity that may not be completely represented on disk.

The memory evidence was retained with its SHA-256 value so that the working copy could be compared against the recorded acquisition value.

## Metadata Analysis

File metadata was examined to identify information associated with files beyond their visible contents.

Metadata can provide useful investigative context such as timestamps, file characteristics, and other attributes that may help establish relationships between artefacts.

Metadata findings were considered together with file-system and other forensic evidence rather than treated as standalone proof.

## Steganography Analysis

Files were examined for indications that information could be concealed within apparently ordinary media.

Steganography analysis demonstrated that a file's visible appearance does not necessarily represent all of the information contained within it.

The analysis was therefore incorporated into the wider investigation rather than treated as an isolated tool exercise.

## Evidence Correlation

The investigation followed a correlation-based approach:

**Event Evidence → Memory Evidence → Disk Evidence → File Artefacts → Metadata → Hidden Content**

The purpose was to determine whether individual observations were supported by other evidence sources.

This approach reduced reliance on isolated artefacts and provided a more defensible basis for investigative conclusions.

## Key Observations

1. The Windows disk image was successfully acquired and subsequently verified.
2. The FTK Imager verification process reported a hash **Match** and no bad blocks.
3. The RAM evidence retained the recorded SHA-256 value after transfer to the host.
4. Autopsy successfully loaded and examined the verified E01 image.
5. Multiple Windows artefact categories were available for examination, including recent documents, browser activity, USB history, run-program information, and deleted files.
6. Autopsy identified 337 extension-mismatch results requiring contextual examination.
7. File recovery demonstrated that deleted user data can remain available within forensic evidence.
8. Metadata and hidden-content analysis provided additional investigative context.
9. Findings were considered across multiple evidence sources rather than relying on a single artefact.

## Investigative Conclusion

The investigation demonstrated a complete practical forensic workflow beginning with evidence identification and preservation and continuing through acquisition, integrity verification, examination, analysis, correlation, and documentation.

The strongest aspect of the investigation was the use of multiple evidence sources to support investigative reasoning. Disk evidence, memory evidence, Windows artefacts, recovered files, metadata, and hidden-content analysis were examined as complementary sources.

The investigation also demonstrated an important forensic principle: **an artefact that appears suspicious is an investigative lead, not automatically a finding of malicious activity.** Context and corroboration are required before assigning significance to an artefact.

The evidence-handling process, including acquisition verification and preservation of recorded hashes, provided an auditable basis for the subsequent examination.

## Professional Takeaway

This investigation was designed to demonstrate practical investigative judgement rather than simply the ability to operate forensic tools.

The work required identifying relevant evidence, preserving its integrity, examining different artefact sources, distinguishing observations from conclusions, and documenting the reasoning behind the findings.

That workflow reflects how digital forensic investigations are approached when the objective is not merely to find an artefact, but to determine what the evidence actually supports.
