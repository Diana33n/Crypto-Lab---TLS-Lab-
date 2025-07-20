TLS Lab - ENCS5322

This repository contains the implementation and documentation of a Transport Layer Security (TLS) Lab as part of the **ENCS5322** course at the **Faculty of Engineering & Technology, Electrical & Computer Engineering Department**.

Overview

This lab explores the fundamentals of **TLS** and its role in securing communication over networks. It guides students through implementing:

* ✅ A **TLS Client** to understand the handshake process, certificate validation, and secure data exchange.
* ✅ A **TLS Server** with custom certificates and Subject Alternative Names (SANs).
* ✅ A **Simple HTTPS Proxy** to demonstrate vulnerabilities such as Man-In-The-Middle (MITM) attacks.

Through these hands-on exercises, students gain practical experience in **TLS**, **PKI**, and **HTTPS**, preparing them to secure real-world applications.

---

## 📂 Contents

* `handshake.py`: Implements a TLS client performing a handshake and data retrieval.
* `server.py`: Implements a basic TLS server serving HTML content over HTTPS.
* `client-certs/`: Directory for custom CA certificates used by the client.
* `server-certs/`: Directory for server certificates and private keys.
* `san_config.cnf`: OpenSSL configuration for generating certificates with SANs.
* `README.md`: This file.

---

## 🚀 How to Run

### Prerequisites

* Python 3.x
* OpenSSL
* Docker (optional for containerized environment)
* Wireshark (for network traffic analysis)

### 1️⃣ Run the TLS Client

```bash
cd client
python3 handshake.py www.google.com
```

This will:

* Establish a TLS handshake
* Validate server certificates
* Send and receive data securely

### 2️⃣ Run the TLS Server

```bash
cd server
python3 server.py
```

Ensure the server certificates (`server.crt` and `server.key`) exist in the `server-certs/` directory.

### 3️⃣ Simulate HTTPS Proxy (MITM)

Follow the instructions in the lab document to set up hosts redirection and run the MITM proxy.

---

## 🔒 Key Features

* 🔑 TLS handshake with real-world servers (Google, Example.com)
* 🗂 Custom CA directory for certificate validation
* 📜 Certificate generation with SAN support
* 🛡 MITM attack demonstration using HTTPS proxy

---

## 📚 References

* [RFC 5246 - The Transport Layer Security (TLS) Protocol Version 1.2](https://datatracker.ietf.org/doc/html/rfc5246)
* [Wireshark Documentation](https://www.wireshark.org/docs/)
* [Python ssl module](https://docs.python.org/3/library/ssl.html)
* [OpenSSL](https://www.openssl.org/docs/)

---

## 👨‍🎓 Author

* **Diana Naseer**
* Student ID: 1210363
* Instructor: Dr. Ahmad Alsadeh
* Date: 1/8/2024

---

هل تريدني:

✅ أن أضيف أيضًا **أوامر OpenSSL خطوة بخطوة** في README لإعداد الشهادات؟
✅ أم تريد **نسخة عربية بالكامل** بجانب الإنجليزية؟
✅ أم كلاهما معًا؟
