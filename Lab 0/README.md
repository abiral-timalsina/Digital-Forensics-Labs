# Lab 0: The Leaked Paper

| | |
|---|---|
| **Type** | Insider data leak |
| **Evidence** | Damaged USB drive, supplied as a raw disk image |
| **Level** | Sample, Easy to Medium |
| **Flags** | 1 |

## Story

A final-semester *Database Management System* paper at **Himalayan Model College** appeared in a student group the night before the exam, and the exam was cancelled.

A USB drive was found plugged into the PC in the exam section's photocopy room. When someone tried to open it, the computer asked to format it. Nobody claims the drive.

You are the examiner. Find out what happened and who is most likely responsible.

## Evidence

| | |
|---|---|
| **Download** | [`case01.zip`](https://github.com/abiral-timalsina/Digital-Forensics-Labs/releases/download/lab0-v1/case01.zip) (unzips to `case01.img`) |
| **Size** | 727 KB zipped, 512 MB unzipped |
| **SHA-256 of the zip** | `3d224703b088f40e9f555e7e5ae8918f2ecbe91d6caf553a842efc2b54176fa5` |
| **SHA-256 of the image** | `1fc14dfb1ddf5ca96f60103a28f94df3014a33a9e460abf98f9dc97da831dcae` |

Check both fingerprints before you start, and work on a copy of the image.

Windows (PowerShell):

```powershell
Get-FileHash case01.zip -Algorithm SHA256
```

Linux:

```bash
sha256sum case01.zip
unzip case01.zip
sha256sum case01.img
```

## Questions

1. What is the **label** of the drive's volume?
2. Which file on the drive is **not what its name says it is**, and what is it really?
3. Who **last saved** the exam paper, and who **created** it?
4. What **phone model** took the photos of the paper?
5. What was the **price per paper** (in Rs), and which payment number was used?
6. At about what **time** was the last change made to the drive's top-level folder? Give the time and the timezone you used.
7. Find the **flag**. Format: `FLAG{...}`
8. In 4 to 6 lines, say **who is most likely responsible**, give **at least two pieces of evidence**, and state **one thing you cannot prove** from this drive alone.

## Walkthrough

Try the lab on your own first. If you get stuck, the full walkthrough is here (**contains spoilers**): [walkthrough](walkthrough/README.md)

## Submission

See the main [README](../README.md#flag-format-and-submission).
