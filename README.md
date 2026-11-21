# Networkwalks Cybersecurity Internship – Week 3

## Password Cracking with JTR & NetworkWalks Tools

**Name:** Sakina Aftab
**Batch:** B084
**Program:** Networkwalks Cybersecurity Internship
**Week:** 03
**Project:** Password Cracking (PM1 + PM2)

---

## Objective
Crack the password of a protected PDF file using two different methods:
1. John the Ripper (JTR) with the Johnny GUI
2. NetworkWalks' own Hash Calculator and Password Cracker web tools

This demonstrates how password hashes can be extracted from locked files and cracked using dictionary attacks, and reinforces why strong, unique passwords matter.

---

## PM1 — Password Cracking with JTR

**Tools Used:**
- John the Ripper (1.9.0 jumbo, Windows 64-bit)
- Johnny GUI (2.2, Windows)
- Online PDF Hash Extractor (onlinehashcrack.com)

**Target File:** `My Locked PDF1.pdf` (267 KB)

### Steps

**1. Downloaded target file and tools**
![Downloads](screenshots/q1.png)

**2. Configured Johnny with the John the Ripper executable**
![Johnny Settings](screenshots/q2.png)

**3. Extracted the PDF hash**
![Hash Extracted](screenshots/q3.png)

**4. Loaded the hash into Johnny**
![Hash Loaded](screenshots/q4.png)

**5. Ran the attack and cracked the password**
![Password Cracked](screenshots/q5.png)

**6. Verified by opening the PDF with the cracked password**
![PDF Unlocked](screenshots/q6.png)

### Cracked Password
`good-luck`

---

## PM2 — Password Cracking with NetworkWalks Tools

**Tools Used:**
- NetworkWalks Hash Calculator (networkwalks.com/hash-calculator)
- NetworkWalks Password Cracker (networkwalks.com/password-cracker)

**Target File:** `My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf` (66 KB)

### Steps

**7. Confirmed target file**
![Target File](screenshots/q7.png)

**8. Extracted the hash using Hash Calculator**
![Hash Extracted](screenshots/q8.png)

**9. Pasted the hash into Password Cracker**
![Hash Pasted](screenshots/q9.png)

**10. Ran the attack**
![Attack Running](screenshots/q10.png)

**11. Password cracked successfully**
![Password Cracked](screenshots/q11.png)

**12. Verified by opening the PDF with the cracked password**
![PDF Unlocked](screenshots/q12.png)

### Cracked Password
`good-luck`

---

## Conclusion
Both labs showed how password-protected PDFs can be cracked quickly once their hash is extracted, especially when the password is a common word or short phrase. JTR/Johnny represents the offline, installed-tool approach used by security professionals, while the NetworkWalks tools demonstrate the same concept entirely in-browser. Together they reinforce why strong, long, and unique passwords — not simple dictionary words — are essential for real-world file and account protection.
