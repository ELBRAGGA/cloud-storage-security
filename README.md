# Secure Cloud Storage Simulator

A console-based cloud storage system with security features, written in C++17.  
This project demonstrates authentication, role-based access control, file metadata management, and security best practices relevant to cloud security engineering.

## Features
- **User Registration** with salted SHA‑256 password hashing.
- **Login with Account Lockout** after 5 failed attempts.
- **Multi‑Factor Authentication (MFA)** simulation.
- **Role‑Based Storage Limits**: Free (1 GB), Premium (10 GB), Admin (100 GB).
- **File Management**: Upload, list, search, delete files with metadata (region, type, encryption flag).
- **Data Residency Selection**: Asia, Europe, America, Global.
- **Audit Logging** of all security‑related events.
- **Admin Dashboard**: View users, unlock accounts, see security metrics.

## Technologies Used
- C++17 (std::filesystem, std::random, etc.)
- SHA‑256 (via CommonCrypto on macOS, self‑contained on other platforms)
- Console UI with input validation

## How to Build
### On macOS (with Xcode)
1. Open Xcode and create a new Command Line Tool project.
2. Replace the contents of `main.cpp` with the provided source.
3. Set **C++ Language Dialect** to C++17 (Build Settings → C++ Language Dialect).
4. Build and run (⌘R).

### On Linux / Other Platforms
Compile with:
```bash
g++ -std=c++17 main.cpp -o cloud_app -lstdc++fs