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
- CMake (optional, for building)

## 🔧 Installation & Build

### macOS (with Xcode)
```bash
# Clone the repository
git clone https://github.com/ELBRAGGA/cloud-storage-security.git
cd cloud-storage-security

# Compile
g++ -std=c++17 cloud_storage.cpp -o cloud_app

# Run
./cloud_app
