# 🗳️ Secretum – Secure Polling Application

**Secretum** is a Python-based web application that enables secure and anonymous online voting.  
The system uses **RSA encryption** to protect votes and provides a simple, user-friendly web interface for managing polls and displaying results.

🔗 **Live demo:**  
https://secretum-polling-app.herokuapp.com/

🔗 **GitHub repository:**  
https://github.com/tamascsiba/Poll

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

---

## 🔐 Security – RSA Encryption

This project implements a custom RSA encryption module to secure voting data:

Key generation

Encryption and decryption

Secure storage of votes

The encryption logic is implemented in:
RSA_crypt.py

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

