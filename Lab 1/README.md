# Lab 1: The Fake Wallet Link

| | |
|---|---|
| **Type** | Phishing / account takeover |
| **Evidence** | Network capture (PCAP) from a home router |
| **Level** | Easy to Medium |
| **Flags** | 1 |
| **Tools** | Wireshark (or tshark, NetworkMiner) |

## Story

**Sita Rai** from Kathmandu received an SMS saying her mobile wallet account would be blocked unless she verified it. She tapped the link in the message and followed the steps on the page. A short while later, **Rs 45,000** left her account.

Her home router recorded the network traffic of that evening. The police cyber cell has the capture.

You are the examiner. Find out what happened, and what the capture can and cannot prove.

> All people, brands, domains, phone numbers and payments in this lab are **fictional**. The domains end in `.example`, which can never point to a real site.

## Evidence

| | |
|---|---|
| **Download** | [`case02.zip`](https://github.com/abiral-timalsina/Digital-Forensics-Labs/releases/download/lab1-v1/case02.zip) (unzips to `case02.pcap`) |
| **Size** | 3.5 KB zipped, 11 KB unzipped |
| **SHA-256 of the zip** | `ffda788f802d3a7a4a35a432a43bed2f6f47f7bdb7320f2f7dcaaca040245f11` |
| **SHA-256 of the capture** | `bd3a6f0b8f11f637fba64953a4ebfd0c8ea56d7d124495b9e9726d31535351b5` |

Check both fingerprints before you start, and work on a copy of the capture.

Windows (CMD):

```
certutil -hashfile case02.zip SHA256
```

Linux:

```bash
sha256sum case02.zip
unzip case02.zip
sha256sum case02.pcap
```

## Questions

1. What is the **IP address of the victim's device**?
2. Two domain names in the capture look almost identical. Which one is the **lookalike**, and how do you know?
3. What is the **IP address of the server** that hosts the lookalike?
4. What details were **submitted**, and in what **order**?
5. What **phone model** and **browser** did the victim use?
6. At what **time** was the OTP submitted? Give the time and the **time zone** you used.
7. Find the **flag**. Format: `FLAG{...}`
8. In 4 to 6 lines, say **what happened**, give **at least three pieces of evidence**, and state **one thing you cannot prove** from this capture alone.

## Walkthrough

Try the lab on your own first. If you get stuck, the full walkthrough is here (**contains spoilers**): [walkthrough](walkthrough/README.md)

The walkthrough shows you where the flag is hidden, but it does not decode it for you.

## Submission

See the main [README](../README.md#flag-format-and-submission).
