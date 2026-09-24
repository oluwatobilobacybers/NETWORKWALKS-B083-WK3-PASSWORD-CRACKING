# NETWORKWALKS-B083-WK3-PASSWORD-CRACKING

## Week 3 Project – Password Cracking with John the Ripper & NetworkWalks Tools

This repository documents the completion of my Week 3 project at **NetworkWalks Academy**, focusing on practical password-recovery techniques using two different tools and platforms.

> **Security & Privacy Note:** Recovered passwords, complete password hashes, and other sensitive credential information are intentionally excluded from this public repository.

### Project Goal

Perform authorized password-recovery exercises on protected PDF files using:

- **John the Ripper on Kali Linux**
- **NetworkWalks Hash Calculator and Password Cracker on Windows**

The objective was to understand how password-protected PDF files can be assessed through hash extraction and dictionary-based password recovery, while reinforcing the importance of strong and unique passwords.

---

## Modules Completed

| Module | Description | Platform | Status |
|--------|-------------|----------|--------|
| **W3-PM1** | Password Cracking with John the Ripper | Kali Linux | Completed |
| **W3-PM2** | Password Cracking with NetworkWalks Hash Calculator & Password Cracker | Windows | Completed |

---

## Tools Used

### W3-PM1 – Kali Linux

- `pdf2john` – Extracts password hashes from password-protected PDF files
- **John the Ripper** – Performs offline password-recovery attacks against supported password hashes

### W3-PM2 – Windows

- **NetworkWalks Hash Calculator** – Extracts the password hash from the protected PDF
- **NetworkWalks Password Cracker** – Performs dictionary-based password recovery against the extracted hash

---

## Results Summary

Two different password-protected PDF files were used for the two modules.

| Module | Target | Tool | Result |
|--------|--------|------|--------|
| **W3-PM1** | Locked PDF 1 | John the Ripper | Password successfully recovered |
| **W3-PM2** | Locked PDF 2 | NetworkWalks Password Cracker | Password successfully recovered |

---

# W3-PM1 – Password Cracking with John the Ripper

## Procedure

1. Used `pdf2john` to extract the password hash from the protected PDF.
2. Saved the extracted hash to a text file.
3. Used John the Ripper to process the extracted PDF hash.
4. Performed a dictionary-based password-recovery attempt.
5. Verified the successful recovery using John's `--show` option.

### Hash Extraction

The PDF hash was extracted using `pdf2john`:

```bash
pdf2john "My Locked PDF1.pdf" > hash1.txt
```

The extracted hash was then processed with John the Ripper.

### Verification

The recovery result was verified using:

```bash
john --show hash1.txt
```

### Result

The password was successfully recovered.

Evidence from the John the Ripper session confirmed:

```text
1 password hash cracked, 0 left
```

### Evidence

#### 1. Hash Extraction using pdf2john (Kali Linux)

![pdf2john Hash Extraction](screenshots/01-pdf2john-hash-extraction.png)

#### 2. John the Ripper – Successful Password Crack

![John the Ripper Success](screenshots/02-john-the-ripper-success.png)

#### 3. Flag Capture – PDF1 Cracked with John the Ripper

![Flag Capture - PDF1](screenshots/03-flag-capture-pdf1-jtr.png)

---

# W3-PM2 – NetworkWalks Hash Calculator & Password Cracker

## Procedure

1. Used a separate authorized password-protected PDF supplied for the NetworkWalks exercise.
2. Uploaded the PDF to the NetworkWalks Hash Calculator.
3. Extracted the PDF password hash.
4. Copied the extracted hash into the NetworkWalks Password Cracker.
5. Performed the password-recovery exercise.
6. Successfully recovered the password.

### Result

The password was successfully recovered using the NetworkWalks tools.

The recovered credential is intentionally excluded from this public documentation.

### Evidence

Screenshots documenting the practical exercises are included below.

#### 4. NetworkWalks Hash Calculator

![NetworkWalks Hash Calculator](screenshots/04-networkwalks-hash-calculator.png)

#### 5. NetworkWalks Password Cracker – Successful Result

![NetworkWalks Password Cracker Success](screenshots/05-networkwalks-password-cracker-success.png)

#### 6. Flag Capture – PDF2 Cracked with Windows-Based NetworkWalks Tools

![Flag Capture - PDF2](screenshots/06-flag-capture-pdf2-networkwalks.png)

> **Important:** Ensure screenshots uploaded to this public repository do not expose recovered passwords, complete hashes, usernames, session tokens, or other sensitive credentials.

---

## Troubleshooting & Analysis

One important lesson from this week's exercises was that successful password recovery depends not only on running a cracking tool, but also on understanding the workflow between the protected file, extracted hash, wordlist, and cracking tool.

I also compared two different approaches:

- A command-line workflow using Kali Linux, `pdf2john`, and John the Ripper
- A Windows-based workflow using the NetworkWalks Hash Calculator and Password Cracker

Using different tools and platforms helped me understand the common principle behind both workflows while also seeing how the implementation differs between environments.

---

## Lessons Learned

- Password-protected files can be assessed through their extracted password hashes.
- Hash extraction is an important step in the password-recovery workflow.
- Dictionary attacks can successfully recover weak or commonly used passwords.
- The effectiveness of a dictionary attack depends heavily on the available wordlist and password characteristics.
- Strong, unique passwords significantly increase resistance to dictionary-based attacks.
- Password-cracking tools should only be used against systems and files for which testing is explicitly authorized.
- Sensitive credentials and password hashes should not be unnecessarily exposed in public documentation.
- Different operating systems and tools can implement the same underlying password-recovery workflow in different ways.

---

## Full Report

📄 **[Password Cracking Report (DOCX)](./reports/w3-password_cracking_report.docx)**

> Add the DOCX file to the `reports/` directory before relying on this link.

---

## Authorization & Ethical Use

All activities were performed using educational files and tools provided for the **NetworkWalks cybersecurity training program**.

The exercises were conducted for educational and authorized security-testing purposes only.

No unauthorized systems, accounts, or third-party files were targeted.

Sensitive credentials, password hashes, and other confidential information have been excluded or redacted from the public documentation.

> **Liability Disclaimer:** The techniques documented in this project are intended for authorized educational and security-testing purposes only. Password-recovery and password-cracking techniques must not be used against systems, accounts, or files without explicit permission. Unauthorized access or password cracking may be illegal. The author and training provider are not responsible for misuse of the information contained in this repository.

---

## Author

**Banjo Oluwatobiloba Adekunle**

Aspiring Cybersecurity Analyst | Network Security Enthusiast  
ISC² Certified in Cybersecurity (CC)  
CompTIA Security+  
CEH Candidate

🔗 **LinkedIn:** https://www.linkedin.com/in/oluwatobiloba-banjo-b2368819b/

💻 **GitHub:** https://github.com/oluwatobilobacybers

---

### Project Information

- **Batch:** B083 – NetworkWalks Cybersecurity Internship
- **Project:** Week 3 – Password Cracking
- **Modules:** W3-PM1 & W3-PM2
- **Platforms:** Kali Linux & Windows
