# FileSecureSuite - Quick Start Guide

## Installation

### Windows
```bash
python -m pip install -r requirements.txt
python FileSecureSuite_1_0_0.py
```

### macOS / Linux
```bash
python3 -m pip install -r requirements.txt
python3 FileSecureSuite_1_0_0.py
```

### Automated Installers
- **Windows:** `install_filesecure_windows.bat`
- **Linux:** `bash install_filesecure_linux.sh`
- **macOS:** `bash install_filesecure_macos.sh`

---

## Usage

Run the application:
```bash
python3 FileSecureSuite_1_0_0.py
```

### Main Operations
1. **Encrypt Files** - Secure with AES-256-GCM
2. **Decrypt Files** - Restore encrypted files
3. **Text Encryption** - Encrypt/decrypt text
4. **Generate Keys** - Create RSA-4096 key pairs
5. **Manage Keys** - Import/export keys
6. **Generate QR Codes** - Share keys

---

## Requirements
- Python 3.8+
- pip
- Internet (first installation only)

---

## Troubleshooting

**Python not found?**
- Windows: Download from https://www.python.org/downloads/ (check "Add Python to PATH")
- Linux: `sudo apt install python3 python3-pip`
- macOS: `brew install python@3.11`

**pip not found?**
```bash
python -m pip install -r requirements.txt
python3 -m pip install -r requirements.txt
```

---

## Documentation
- [INSTALLATION_INSTRUCTIONS.md](INSTALLATION_INSTRUCTIONS.md) - Full setup guide
- [WINDOWS_PYTHON_INSTALLATION_GUIDE.md](WINDOWS_PYTHON_INSTALLATION_GUIDE.md) - Windows setup
- [README_INSTALLERS.md](README_INSTALLERS.md) - Installer guide

---

## License
MIT License - See [LICENSE](LICENSE)
