### 🗳️ Secretum – Secure Polling Application

**Secretum** is a Python-based web application that enables secure and anonymous online voting.  
The system uses **RSA encryption** to protect votes and provides a simple, user-friendly web interface for managing polls and displaying results.

---

## 📌 Features

- 📝 Create and manage polls
- 👥 Handle participant voting
- 🔐 RSA-based encryption for secure votes
- 📊 View and analyze poll results
- 📁 CSV-based data storage
- 🌐 Web interface using HTML templates
- 🎨 Static assets (CSS, JavaScript)

---

## 🧠 Technology Stack

This project is built using the following technologies:

- **Python 3**
- **Flask** (web framework)
- **HTML / CSS / JavaScript**
- **RSA encryption** (custom implementation)
- **CSV files** for data persistence
- **Heroku** for deployment

---

## 🗂 Project Structure

```bash
Poll/
│
├── app.py # Main Flask application
├── RSA_crypt.py # RSA encryption logic
├── requirements.txt # Python dependencies
├── Procfile # Heroku start configuration
│
├── templates/ # HTML templates
│ ├── index.html
│ ├── poll.html
│ └── result.html
│
├── static/ # CSS, JavaScript, images
│
├── participants_vote_csv/ # Participant votes storage
├── users_polls_csv/ # User poll storage
│
└── README.md # Project documentation
 ```

---

## 🔐 Security – RSA Encryption

This project implements a custom RSA encryption module to secure voting data:

Key generation

Encryption and decryption

Secure storage of votes

The encryption logic is implemented in:
RSA_crypt.py

# RSA_crypt.py

⚠️ **Warning:** This implementation is strictly for **educational purposes** and should **not** be used in real-world or production cryptographic systems.


## Features

- RSA public and private key generation
- Encryption of an IP address using RSA
- Hexadecimal encoding of encrypted values
- Decryption back to the original IP address

## Requirements

- Python 3.x
- `sympy` library

Install dependencies using:

```bash
pip install sympy
```
## How the Code Works

1. Modular Inverse Calculation

The mod_inverse function calculates the modular inverse using the Extended Euclidean Algorithm, which is necessary for computing the RSA private key.

```python
def mod_inverse(e, phi):
```

2. RSA Key Pair Generation

The generate_key_pair function:

Generates two random 50-digit prime numbers (p and q)

Computes the modulus n = p * q

Calculates Euler’s totient value phi = (p - 1) * (q - 1)

Selects a public exponent e such that gcd(e, phi) = 1

Computes the private exponent d

```python
public_key, private_key = generate_key_pair()
```

3. IP Address Encryption

Each character of the IP address:

Is converted to its Unicode value using ord()

Is encrypted using modular exponentiation

Is stored in a list of encrypted integers

Example IP address:

```python
ip_addr = "192.168.0.1"
```

4. Hexadecimal Encoding

The encrypted integers are converted into a hexadecimal string format, which can be useful for storage or transmission.

```python
crypted_ip_hex += "{:02x}".format(y)
```

5. Decryption

For decryption:

Each encrypted integer is decrypted using the private key

Converted back to characters using chr()

Reassembled into the original IP address string

Final decrypted output:

```bash
192.168.0.1
```



---

## ⚠️ Disclaimer:
This RSA implementation is intended for educational and demonstration purposes and should not be used as a replacement for production-grade cryptographic libraries.

---

## 🧪 Data Storage

Polls and votes are stored in CSV files

Simple and transparent structure

Suitable for small-scale projects and educational use

---

## 🏁 Conclusion

The **Secretum Secure Polling Application** demonstrates how modern web technologies and basic cryptographic principles can be combined to build a functional and secure online voting system. By integrating a Flask-based backend with a custom RSA encryption mechanism, the project highlights the importance of data confidentiality and integrity in digital voting scenarios.

This application is particularly suitable for **educational purposes**, small-scale polling, and as a foundation for more advanced voting systems. While the current implementation uses CSV-based storage and a custom cryptographic module, the architecture can be extended with databases, user authentication, and industry-standard security libraries to support real-world use cases.

Overall, the project provides a solid starting point for understanding secure polling systems, web application development in Python, and the practical application of cryptography in software engineering.

