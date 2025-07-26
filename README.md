# 🔐 Random Password Generator

A simple Python script to generate secure, random passwords based on user preferences. The user can choose the password length and whether to include letters, digits, and symbols.

---

## 📌 Features

- ✅ Choose your own password length
- 🔤 Include letters (A–Z, a–z)
- 🔢 Include digits (0–9)
- 🔣 Include symbols (!@#$%^&*, etc.)
- 🚫 Handles invalid input gracefully

---

### ✅ Prerequisites

- Python 3.x installed
- No external libraries needed

---
Run the script:

bash
Copy
Edit
python password_generator.py

## 🧠How It Works
Takes user input for password preferences

Assembles a character set from:

string.ascii_letters (A–Z, a–z)

string.digits (0–9)

string.punctuation (symbols)

Generates a random password of the specified length using random.choice()

Displays the generated password

## 🧪Example
🔐 Random Password Generator
Enter desired password length (e.g. 8, 12): 12
Include letters? (y/n): y
Include digits? (y/n): y
Include symbols? (y/n): n

Your generated password is: G2eKTqZf18yB



