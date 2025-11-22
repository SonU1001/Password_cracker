# HashCracker CLI 🔐

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-yellow?style=for-the-badge)

**HashCracker CLI** is a lightweight, Python-based password cracking tool designed for educational purposes and security testing. It utilizes a dictionary attack method to recover passwords from **MD5** and **SHA1** hashes.

Featuring a retro ASCII art interface and color-coded output, this tool is designed for ease of use during Capture The Flag (CTF) competitions or basic penetration testing assessments.

---

## ⚠️ Legal Disclaimer

**FOR EDUCATIONAL USE ONLY.**

This tool is developed for educational purposes and to aid security researchers and penetration testers in understanding hashing algorithms and dictionary attacks.
* Do not use this tool on systems or data you do not have explicit permission to test.
* The developer assumes no liability and is not responsible for any misuse or damage caused by this program.

---

## ✨ Features

* **Multi-Algorithm Support:** Capable of cracking both MD5 and SHA1 hashes.
* **Dictionary Attack:** Uses a user-provided wordlist (`file.txt`) to compare hashes.
* **Interactive Interface:** Simple, menu-driven CLI.
* **Visual Feedback:** Uses `colorama` for colored output and status updates.

---

## 🚀 Getting Started

### Prerequisites

* Python 3.x installed on your system.
* A wordlist file (e.g., `rockyou.txt` or a custom list).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/HashCracker-CLI.git](https://github.com/yourusername/HashCracker-CLI.git)
    cd HashCracker-CLI
    ```

2.  **Install dependencies:**
    This tool requires the `colorama` library for terminal formatting.
    ```bash
    pip install colorama
    ```

3.  **Setup the Wordlist:**
    The script looks for a file named `file.txt` in the same directory to use as a password database.
    * Create a file named `file.txt`.
    * Paste your password candidates inside (one password per line).
    * *Alternatively, rename an existing wordlist (like rockyou.txt) to file.txt.*

---

## 💻 Usage

1.  **Run the script:**
    ```bash
    python cracker.py
    ```

2.  **Select the Hash Type:**
    When prompted, choose the algorithm corresponding to your target hash:
    ```text
    1. SHA1 Hash
    2. MD5 Hash
    3. Quit Script
    ```

3.  **Input the Hash:**
    Paste the target hash when prompted.

4.  **View Results:**
    The tool will iterate through `file.txt`.
    * **Success:** It will print `The password is [password]`.
    * **Failure:** It will notify you if the password was not found in the list.

---

🗺️ Roadmap & Future Improvements
[ ] Add support for SHA-256 and SHA-512.

[ ] Implement Salting support.

[ ] Add argument parsing (argparse) for direct CLI usage without the menu.

[ ] Add a progress bar for large wordlists.
