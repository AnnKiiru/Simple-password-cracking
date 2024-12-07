# Password Cracking Project: Cracking Password Hash Using John the Ripper

## Description  
This project demonstrates the process of cracking password hashes using **John the Ripper**, a powerful password cracking tool. The goal is to showcase how to crack a password protected by various hash types, utilizing **wordlist-based** attacks with the famous **rockyou.txt** wordlist.

## Key Features  
- **Hash Cracking**: Cracks password hashes using John the Ripper with a pre-defined wordlist.  
- **Wordlist Attack**: Utilizes the popular **rockyou.txt** wordlist to attempt password guesses.  
- **Hash File Analysis**: Explains the process of extracting password hashes from a file and analyzing them.  
- **Format Detection**: Handles different hash formats such as LM, NTLM, MD5, etc., ensuring compatibility with the cracking tool.  
- **File Integrity Check**: Demonstrates how to verify file integrity using hashes and compare them with known signatures.

## Tools Used  
- **John the Ripper**: A password cracking tool that supports multiple hash algorithms.  
- **rockyou.txt**: A widely used wordlist containing common passwords, often used in brute force attacks.  
- **HashMyFiles**: A tool used to generate file hashes to check for integrity.  
- **Cmder**: A command-line interface for executing the cracking process and handling files.

## How It Works  
1. **Prepare the Hash File**: Extract the password hashes from a file that is protected by a password (e.g., `.txt` file containing the hash).
2. **Configure John the Ripper**: Run John the Ripper with the appropriate format and wordlist to begin the cracking process.
3. **Run Wordlist-Based Attack**: Use the rockyou.txt wordlist to attempt to match the password hash with possible guesses.
4. **Monitor Cracking Progress**: Check the status of the cracking process and review any discovered passwords.
5. **Analyze Cracked Password**: Once cracked, analyze the password for strength and potential security vulnerabilities.

## Benefits  
- **Password Cracking Knowledge**: Provides hands-on experience with password cracking techniques and tools.  
- **Real-World Application**: Demonstrates how attackers might try to gain unauthorized access to systems using weak passwords.  
- **Security Awareness**: Highlights the importance of using strong and unique passwords to enhance security.  
- **Tool Familiarity**: Offers experience with John the Ripper, a popular password cracking tool used in penetration testing and cybersecurity.

## Prerequisites  
- **John the Ripper**: Install John the Ripper by following the official [John the Ripper GitHub repository](https://github.com/magnumripper/JohnTheRipper).  
- **rockyou.txt Wordlist**: Obtain the **rockyou.txt** wordlist, often pre-installed on Linux systems or available online.  
- **Basic Understanding of Hashes and Password Security**: Familiarity with password hashing algorithms and password security best practices.

## Installation  
1. **Install John the Ripper**:  
   - Clone the John the Ripper repository:  
   ```bash
   git clone https://github.com/magnumripper/JohnTheRipper.git
   cd JohnTheRipper/src
2. **Download rockyou.txt**
   -wget https://github.com/praetorian-inc/Hob0Rules/raw/master/wordlists/rockyou.txt.gz
gunzip rockyou.txt.gz
3. ****Prepare hashfile**
   -user:$lm$1000$1A2B3C4D5E6F7A8B9C0D1E2F3A4B5C6D7E8F9G0H1I2J3K4L5M6N7O8P9Q0:1000:1000:::
4. **Run John The Ripper**
   -john --wordlist=/path/to/rockyou.txt.gz /path/to/hash.txt
