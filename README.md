# FileSecureSuite v1.0

Enterprise-grade file encryption with AES-256-GCM and RSA-4096.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)

---

## Features

- **AES-256-GCM Encryption** - Military-grade symmetric encryption with authentication
- **RSA-4096 Key Exchange** - Robust asymmetric encryption for key distribution
- **Cross-Platform** - Windows, macOS, and Linux support
- **Secure Key Derivation** - PBKDF2 with configurable iterations
- **Interactive CLI** - User-friendly terminal interface with progress bars
- **QR Code Generation** - Share encrypted keys via QR codes
- **HMAC Verification** - Integrity checking for all encrypted data

---

## Quick Start

### Installation

```bash
# Windows
python -m pip install -r requirements.txt
python FileSecureSuite_1_0_0.py

# macOS / Linux
python3 -m pip install -r requirements.txt
python3 FileSecureSuite_1_0_0.py
```

### Automated Installers

**Windows:**
```cmd
install_filesecure_windows.bat
```

**Linux:**
```bash
bash install_filesecure_linux.sh
```

**macOS:**
```bash
bash install_filesecure_macos.sh
```

---

## Requirements

- **Python 3.8** or higher
- **pip** (Python package manager)
- Internet connection (for first-time installation)

### Dependencies

All automatically installed:
- `cryptography>=41.0.0` - Encryption primitives
- `qrcode[pil]>=8.0` - QR code generation
- `colorama>=0.4.6` - Colored terminal output
- `tqdm>=4.66.0` - Progress bars
- `pyperclip>=1.8.2` - Clipboard operations

---

## Usage

Launch the application:

```bash
python3 FileSecureSuite_1_0_0.py
```

### Main Features

1. **Encrypt Files** - Secure files with AES-256-GCM
2. **Decrypt Files** - Restore encrypted files
3. **Text Encryption** - Encrypt/decrypt text directly
4. **Generate Keys** - Create RSA-4096 key pairs
5. **Manage Keys** - Import/export encryption keys
6. **Generate QR Codes** - Share keys securely

---

## Security

- Uses NIST-approved cryptographic algorithms
- No plaintext key storage
- Secure random salt generation
- File permissions restricted to owner only
- HMAC-based integrity verification

---

## Installation Guide

Detailed setup instructions available in:
- [INSTALLATION_INSTRUCTIONS.md](INSTALLATION_INSTRUCTIONS.md)
- [WINDOWS_PYTHON_INSTALLATION_GUIDE.md](WINDOWS_PYTHON_INSTALLATION_GUIDE.md)
- [README_INSTALLERS.md](README_INSTALLERS.md)

---

## Troubleshooting

### Python Not Found (Windows)
1. Download Python: https://www.python.org/downloads/
2. During installation, **CHECK "Add Python to PATH"**
3. Restart Command Prompt
4. Try again

### Python Not Found (Linux)
```bash
# Ubuntu/Debian
sudo apt install python3 python3-pip python3-venv -y

# Fedora
sudo dnf install python3 python3-pip -y

# Arch
sudo pacman -S python python-pip -y
```

### pip Not Found
```bash
python -m pip install cryptography  # Windows
python3 -m pip install cryptography  # Linux/macOS
```

---

## Contributing

Contributions welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

---

## Support

- **Issues:** https://github.com/yourusername/FileSecureSuite/issues
- **Discussions:** https://github.com/yourusername/FileSecureSuite/discussions

---

**FileSecureSuite v1.0** - Enterprise encryption for everyone
