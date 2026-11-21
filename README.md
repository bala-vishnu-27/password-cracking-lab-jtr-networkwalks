# 🔐 Password Cracking Lab: JTR, Johnny & Networkwalks Tools

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![Purpose](https://img.shields.io/badge/purpose-educational-blue)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey)

Hands-on lab from the **Networkwalks Cybersecurity & Ethical Hacking** course (Week 3). I recovered the password of a protected PDF using two different approaches and captured the lab flag.

> ⚠️ **Disclaimer:** This was done on a lab file provided by the course, in an authorized training environment, for educational purposes only. Do not use these techniques on files or systems you don't own or have permission to test.

---

## 🎯 Objective

Understand how password cracking works end to end and show why weak, common passwords are dangerous.

## 🧰 Tools Used

| Module | Tools |
|--------|-------|
| Module 1 | John the Ripper 1.9.0-jumbo-1, Johnny GUI 2.2, PDF hash extractor |
| Module 2 | Networkwalks Hash Calculator, Networkwalks Password Cracker (dictionary attack) |

## 🧠 Background

- **Hashing** is a one-way function: plain text goes in, a scrambled digest comes out.
- **Encryption** is two-way: it can be decrypted with the right key.
- A locked PDF stores its password as a hash (`$pdf$...`). If we extract that hash, we can test guesses against it offline.

## 🔁 Methodology

### Module 1: John the Ripper + Johnny
1. Downloaded John the Ripper (jumbo) and Johnny GUI.
2. Pointed Johnny to `john.exe` in Settings.
3. Extracted the PDF hash (`$pdf$...`) and saved it as `hash1.txt`.
4. Opened `hash1.txt` in Johnny and started a new attack.
5. Johnny cracked the hash (100%, 1/1 cracked).
6. Opened the PDF with the recovered password.

### Module 2: Networkwalks Tools
1. Uploaded the PDF to the **Hash Calculator** to extract the hash (Revision R4, Version V4, 128-bit key).
2. Pasted the hash into the **Password Cracker**.
3. Ran a dictionary attack with the built-in 100-word list.
4. Match found after 91 attempts.
5. Opened the PDF and captured the flag. 🚩

## 📸 Screenshots

### Module 1
| Johnny setup | Hash extraction |
|---|---|
| ![](module1-jtr-johnny/screenshots/01-johnny-settings-john-exe.png) | ![](module1-jtr-johnny/screenshots/02-hash-extracted.png) |

| Cracked in Johnny | Flag captured |
|---|---|
| ![](module1-jtr-johnny/screenshots/03-password-cracked.png) | ![](module1-jtr-johnny/screenshots/04-flag-captured.png) |

### Module 2
| Hash extracted | Attack in progress |
|---|---|
| ![](module2-networkwalks-tools/screenshots/01-pdf-hash-extracted.png) | ![](module2-networkwalks-tools/screenshots/02-cracker-in-progress.png) |

| Password cracked | Flag captured |
|---|---|
| ![](module2-networkwalks-tools/screenshots/03-password-cracked.png) | ![](module2-networkwalks-tools/screenshots/04-flag-captured.png) |

## 📊 Results

| Item | Result |
|------|--------|
| Hash type | PDF (`$pdf$4*4*128*...`), R4/V4, 128-bit |
| Attack type | Dictionary attack |
| Attempts needed | 91 of 100 words |
| Outcome | ✅ Password recovered, PDF unlocked, flag captured |

## 💡 Key Learnings

1. **Weak passwords fall in seconds.** A common password was found within 91 guesses.
2. **Length and uniqueness matter.** Long passphrases make dictionary and brute-force attacks impractical.
3. **Encryption is only as strong as the password** protecting the key, even with 128-bit encryption.
4. **Defensive takeaways:** use a password manager, enable MFA, never reuse passwords, avoid patterns like `word + number`.
5. GUI tools like Johnny make it easy to learn, but the real work is done by John the Ripper underneath.

## 🔮 Next Steps

- [ ] Try wordlist + rules attacks in John
- [ ] Compare dictionary vs brute-force speed
- [ ] Next lab: [add your Week 4 topic]

## 🙏 Acknowledgements

Thanks to [Networkwalks Academy](https://www.networkwalks.com) and my instructors for the lab material.

## 👤 Author

**[Your Name]**
[LinkedIn](your-linkedin-url) | [GitHub](your-github-url)
