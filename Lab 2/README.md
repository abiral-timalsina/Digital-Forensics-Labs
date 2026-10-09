# Lab 2: The Lost Bid

**Level:** Medium  
**Evidence:** a pendrive image (`case03.img`)  
**Main tool:** Autopsy (other tools work too)  
**Flags:** 1

> All people, companies and amounts in this lab are **fictional**.

---

## The case

Himalaya Build and Everest Infra were both bidding for the Bagmati Bridge tender. Each company handed in a **sealed bid**, to be opened together on Friday.

On Thursday night, someone at Himalaya Build is suspected of passing the final bid figure to the rival. The next morning, Everest Infra's offer turned out to be just a little lower than Himalaya Build's.

A **pendrive** was found in the printer room of Himalaya Build, and the police cyber cell made a copy of it. The pendrive belongs to the bidding team. Nobody has admitted owning it.

Your job is to **examine the copy** and tell the investigating officer what the drive shows, and what it does **not** show.

---

## Evidence

| Item | Value |
|---|---|
| File | `case03.zip` (about 400 KB, unzips to a 256 MiB disk image) |
| Image inside | `case03.img` |
| Download | See the **Releases** page of this repository (release `lab2-v1`) |

### Check the fingerprint first

| File | SHA-256 |
|---|---|
| `case03.zip` | `780d25be8fb473d3a847c1b90333d5db4475f2c89ad7b040026f120d7ed79afa` |
| `case03.img` | `fa1c9664f2eb01b1e39a50ef67da7edecb20e8d4993c03e90a23020a894d6910` |

Windows (PowerShell):

```
certutil -hashfile case03.img SHA256
```

Linux or Kali:

```
sha256sum case03.img
```

If the fingerprint is different, download the file again.

---

## Questions

Answer all nine. Write your answers in your own notes.

1. What are the **volume label** and the **volume ID** of the pendrive?
2. One file is **not what its name says**. Which file is it, and what does it really contain?
3. A file that was **deleted** holds a final figure for a bid. Which file is it, and what is the total?
4. Who is recorded as the **author** of that file?
5. There is a **photo** on the drive. What **phone** took it, what is written in its **artist** tag, and what **public place** do its GPS numbers point to?
6. Some notes were deleted too. Which **company name** in them links the bidding team to the rival?
7. What is the **latest modified time** of any file on the drive? Write it with a **time zone**.
8. Find the **flag**. It looks like `FLAG{some_text_here}`.
9. Write a **short conclusion** (5 to 8 sentences) for the investigating officer. Say what the drive **proves**, what it is **consistent with**, and what is **unknown**.

---

## Hints

- Not every piece of data on a drive has a **file name**.
- A deleted file is not always gone.
- A file's **name** and a file's **content** can disagree.
- Dates inside Office files and dates kept by the file system are **not stored the same way**. Be careful with time zones.
- The case happened in **Nepal**. In Autopsy, choose the time zone **Asia/Kathmandu** when you add the image.

---

## Tools

Any of these will work:

- [Autopsy](https://www.autopsy.com/) 4.x (this lab was tested with 4.23.1 on Windows)
- The Sleuth Kit (`mmls`, `fls`, `icat`, `istat`)
- [TestDisk](https://www.cgsecurity.org/wiki/TestDisk) and PhotoRec
- [ExifTool](https://exiftool.org/)
- A hex editor such as HxD
- Standard tools: `file`, `strings`, `unzip`, `grep`

---

## Rules

1. Check the fingerprint before you start.
2. Never work on the only copy. Keep the original and work on a copy.
3. Everything you need is **inside the evidence file**.
4. Say what you can **prove**. Do not guess who the leaker is.

---

## Submitting your flag

See the **Flag format and submission** section of the [main README](../README.md).

---

## Walkthrough

A full walkthrough with screenshots is in [Walkthrough.md](Walkthrough.md). **It contains spoilers.** Try the lab on your own first.

---

## License and credit

© 2026 Abiral Timalsina. Licensed under [CC BY-NC-SA 4.0](../LICENSE). If you share, translate or write about this lab, please credit **Abiral Timalsina** and link to this repository.
