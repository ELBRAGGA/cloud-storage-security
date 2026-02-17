```
# Secure Cloud Storage Simulator

[![C++](https://img.shields.io/badge/C++-17-blue)](https://isocpp.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A console-based cloud storage system built with C++17 that demonstrates core cloud security engineering concepts including authentication, authorization, encryption, and audit logging.

## 🚀 Features

### 🔐 Security
- **Salted SHA-256 password hashing** – Secure password storage with unique salts
- **Account lockout** – Automatic lockout after 5 failed login attempts
- **Multi-factor authentication (MFA)** – 6-digit code simulation
- **Audit logging** – All security events logged with timestamps
- **Role-based access control** – Free, Premium, and Admin roles with different storage limits

### ☁️ Cloud Storage
- **File management** – Upload, list, search, and delete files
- **Data residency** – Choose storage region (Asia, Europe, America, Global)
- **Storage quotas** – 1GB Free, 10GB Premium, 100GB Admin
- **File metadata** – Type detection, descriptions, public/private flags
- **Encryption flag** – Simulated "encrypt at rest" option

### 👤 User Management
- **Registration** – With password strength validation
- **Profile management** – View and update security settings
- **MFA toggle** – Enable/disable multi-factor authentication
- **Storage usage monitor** – Visual progress bar

### 👑 Admin Features
- **User overview** – List all users with their roles and status
- **Account management** – Unlock locked accounts
- **Security dashboard** – View system-wide metrics

## 🛠️ Technologies Used

- **C++17** – Modern C++ features (filesystem, random, etc.)
- **SHA-256** – Cryptographic hashing (CommonCrypto on macOS)
- **File I/O** – Persistent storage for users and file metadata
- **STL** – Vectors, maps, algorithms, string manipulation

## 📋 Prerequisites

- C++17 compatible compiler (g++, clang, or MSVC)

## 🔧 Installation & Build

### macOS (with Xcode)
```bash
git clone https://github.com/ELBRAGGA/cloud-storage-security.git
cd cloud-storage-security
g++ -std=c++17 cloud_storage.cpp -o cloud_app
./cloud_app
```

### Linux
```bash
g++ -std=c++17 cloud_storage.cpp -o cloud_app -lstdc++fs
./cloud_app
```

### Windows (with MinGW)
```bash
g++ -std=c++17 cloud_storage.cpp -o cloud_app.exe -lstdc++fs
cloud_app.exe
```

## 🎮 How to Use

1. Run the application: `./cloud_app`
2. Main Menu Options: 1=Login, 2=Create account, 3=Exit

## 📁 Project Structure

```
cloud-storage-security/
├── cloud_storage.cpp          # Main source code
├── README.md                   # This file
├── cloud_users.dat             # User database (auto-generated)
├── cloud_data/                  # File metadata (auto-generated)
│   └── [username].dat           # Per-user file records
└── cloud_system.log             # Audit log (auto-generated)
```

## 🔒 Security Features Explained

| Feature | Implementation | Purpose |
|---------|---------------|---------|
| Password Hashing | SHA-256 with 16-byte random salt | Prevents password recovery from database |
| Account Lockout | 5 failed attempts → locked | Prevents brute-force attacks |
| MFA | 6-digit code simulation | Adds second factor of authentication |
| RBAC | Free/Premium/Admin roles | Enforces least privilege principle |
| Audit Logging | All security events logged | Provides traceability and forensics |

## 📬 Contact

**Yahya Elbragga**  
GitHub: [@ELBRAGGA](https://github.com/ELBRAGGA)  
Project Link: [https://github.com/ELBRAGGA/cloud-storage-security](https://github.com/ELBRAGGA/cloud-storage-security)
