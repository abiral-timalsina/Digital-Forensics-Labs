# Digital Forensics Labs

CTF-styled digital forensics labs built around **police cyber cell case files**. Each lab gives you a short story and a piece of evidence (a disk image, and later memory dumps and phone images). Your job is to investigate it the way a real examiner would and find out what happened.

> All people, organisations, phone numbers and payments in these labs are **fictional**.

---

## Table of contents

1. [About](#about)
2. [Structure of the repository](#structure-of-the-repository)
3. [Tools](#tools)
4. [Rules of the lab](#rules-of-the-lab)
5. [Flag format and submission](#flag-format-and-submission)
6. [Roadmap](#roadmap)
7. [Credits](#credits)
8. [License](#license)
9. [Author](#author)

---

## About

Most free forensics practice is either memory-only or very abstract. These labs wrap real forensic skills (damaged drives, deleted files, hidden data, metadata, timelines) in realistic case stories, and push you to **write a conclusion**, not just collect flags.

You can solve them on **Windows, Ubuntu or Kali Linux**. The evidence is a normal disk image, so no physical USB drive is needed.

## Structure of the repository

| Directory | Case | Evidence | Level |
|---|---|---|---|
| [Lab 0](Lab%200) | The Leaked Paper | Damaged USB drive (disk image) | Sample, Easy to Medium |
| [Lab 1](Lab%201) | The Fake Wallet Link | Network capture (PCAP) | Easy to Medium |
| [Lab 2](Lab%202) | The Lost Bid | Pendrive image (disk image) | Medium |
| Lab 3 | Coming soon | | |
Lab 0 is the **sample lab**. Its full walkthrough will be published so you can see how an investigation is approached. Later labs will not include solutions in this repository.

## Tools

You do not need anything exotic. Any of these will do the job:

- `sha256sum` (or `Get-FileHash` on Windows) to verify evidence
- `xxd` or a hex editor such as HxD
- [TestDisk](https://www.cgsecurity.org/wiki/TestDisk) and PhotoRec
- [The Sleuth Kit](https://www.sleuthkit.org/) (`mmls`, `fls`, `icat`, `istat`) and Autopsy
- [ExifTool](https://exiftool.org/)
- FTK Imager
- Standard command-line tools: `file`, `strings`, `unzip`, `grep`

## Rules of the lab

1. **Verify the evidence first.** Each lab publishes a SHA-256 fingerprint. Check it before you start.
2. **Never work on the original.** Make a copy and work on the copy.
3. **Evidence only.** Everything you need is inside the evidence file. You never need to attack or access any real system.
4. **Say what you can prove.** Good answers separate *proven*, *consistent with* and *unknown*.

## Flag format and submission

Flags look like this: `FLAG{some_text_here}`

If a lab has more than one flag, join them in order, separated by spaces.

Submission details will be added here (email or form). Each lab README says how many flags it has.

## Roadmap

- Disk and USB images (Lab 0 and more)
- Windows memory forensics (Volatility)
- Android phone images
- macOS images
- A website to download the evidence files

## Credits

The layout of this repository is inspired by [MemLabs](https://github.com/stuxnet999/MemLabs) by P. Abhiram Kumar (Team bi0s), a great set of memory forensics CTF labs. The cases, evidence and text here are original.

## License

© 2026 Abiral Timalsina. The labs, case stories and write-ups are licensed under [CC BY-NC-SA 4.0](LICENSE). You may share and adapt them for non-commercial use, as long as you give credit and share your changes under the same license.

## Author

**Abiral Timalsina**, BCA student, aspiring SOC analyst and DFIR practitioner.

- GitHub: [abiral-timalsina](https://github.com/abiral-timalsina)
- LinkedIn: [abiral-timalsina](https://linkedin.com/in/abiral-timalsina)

Feedback and suggestions are welcome. Open an issue or message me.
