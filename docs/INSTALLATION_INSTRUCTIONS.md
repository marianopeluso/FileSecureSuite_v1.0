# FileSecureSuite - Installation Guide

## System Requirements

- **Python 3.8 or higher**
- **pip** (Python package manager)
- Internet connection (for first-time installation)

---

## Installation Instructions

### Windows

1. **Check Python Installation**
   - Open Command Prompt (Press `Win + R`, type `cmd`)
   - Run: `python --version`
   - If you see "Python not found", download from https://www.python.org/downloads/
   - **IMPORTANT:** During installation, CHECK the box "Add Python to PATH"
   - Restart your computer after Python installation

2. **Prepare Installation Directory**
   - Download the `install_filesecure_windows.bat` file
   - Download `FileSecureSuite_1_0_0.py` file
   - Place BOTH files in the same folder (e.g., Desktop or Downloads)

3. **Run the Installer**
   - Right-click on `install_filesecure_windows.bat`
   - Select "Open with" → "Command Prompt"
   - Or simply double-click it
   - The installer will:
     - Check for Python
     - Ask if you want a virtual environment
     - Install all dependencies
     - Confirm when ready to launch

4. **Launch FileSecureSuite**
   - Open Command Prompt in the same directory
   - Run: `python FileSecureSuite_1_0_0.py`

---

### Linux

1. **Check Python Installation**
   - Open Terminal
   - Run: `python3 --version`
   - If Python is not found, install it:
     - **Ubuntu/Debian:** `sudo apt update && sudo apt install python3 python3-pip python3-venv -y`
     - **Fedora/RHEL:** `sudo dnf install python3 python3-pip -y`
     - **Arch:** `sudo pacman -S python python-pip -y`

2. **Prepare Installation Directory**
   - Download the `install_filesecure_linux.sh` file
   - Download `FileSecureSuite_1_0_0.py` file
   - Place BOTH files in the same folder
   - Make the script executable: `chmod +x install_filesecure_linux.sh`

3. **Run the Installer**
   - Open Terminal in that directory
   - Run: `bash install_filesecure_linux.sh`
   - The installer will:
     - Check for Python 3
     - Ask if you want a virtual environment
     - Install all dependencies
     - Confirm when ready to launch

4. **Launch FileSecureSuite**
   - If you created a venv: `source venv/bin/activate`
   - Run: `python3 FileSecureSuite_1_0_0.py`

---

### macOS

1. **Check Python Installation**
   - Open Terminal
   - Run: `python3 --version`
   - If Python is not found, install it:
     - **Using Homebrew (recommended):**
       - Install Homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
       - Install Python: `brew install python@3.11`
     - **Or download directly:** https://www.python.org/downloads/macos/

2. **Prepare Installation Directory**
   - Download the `install_filesecure_macos.sh` file
   - Download `FileSecureSuite_1_0_0.py` file
   - Place BOTH files in the same folder
   - Make the script executable: `chmod +x install_filesecure_macos.sh`

3. **Run the Installer**
   - Open Terminal in that directory
   - Run: `bash install_filesecure_macos.sh`
   - The installer will:
     - Check for Python 3
     - Ask if you want a virtual environment
     - Install all dependencies
     - Confirm when ready to launch

4. **Launch FileSecureSuite**
   - If you created a venv: `source venv/bin/activate`
   - Run: `python3 FileSecureSuite_1_0_0.py`

---

## What Gets Installed?

The installer automatically installs these dependencies:

- **cryptography** (Required) - AES-256-GCM and RSA-4096 encryption
- **qrcode[pil]** - QR code generation for donations
- **colorama** - Colored terminal output
- **tqdm** - Progress bars for large files
- **pyperclip** - Clipboard operations

---

## Troubleshooting

### Python Not Found (Windows)

1. Uninstall Python completely
2. Download from https://www.python.org/downloads/
3. During installation:
   - ✅ CHECK "Add Python to PATH"
   - ✅ CHECK "Install pip"
4. Restart your computer
5. Try again

### Python Not Found (Linux)

Install Python 3:
```bash
# Ubuntu/Debian
sudo apt update && sudo apt install python3 python3-pip python3-venv -y

# Fedora
sudo dnf install python3 python3-pip -y

# Arch
sudo pacman -S python python-pip -y
```

### pip Not Found

Try using the full path:
```bash
# Windows
python -m pip install cryptography

# Linux/macOS
python3 -m pip install cryptography
```

### Installation Fails

If the installer fails:
1. Make sure you have internet connection
2. Try installing each dependency manually:
   ```bash
   pip install cryptography
   pip install qrcode[pil]
   pip install colorama
   pip install tqdm
   pip install pyperclip
   ```

### Permission Denied (Linux/macOS)

If you get "Permission denied":
```bash
chmod +x install_filesecure_linux.sh
bash install_filesecure_linux.sh
```

---

## Virtual Environment vs Global Installation

### With Virtual Environment (Recommended)
- **Pros:** Clean, doesn't affect system Python, easy to uninstall
- **Cons:** Slightly more setup
- Choose "y" when installer asks

### Global Installation
- **Pros:** Simpler, one command
- **Cons:** Affects system Python
- Choose "n" when installer asks

---

## Quick Start (60 seconds)

**Windows:**
```cmd
python -m pip install cryptography
python FileSecureSuite_1_0_0.py
```

**Linux/macOS:**
```bash
python3 -m pip install cryptography
python3 FileSecureSuite_1_0_0.py
```

---

## Support

If you encounter issues:

1. Check that Python 3.8+ is installed: `python --version` (or `python3 --version`)
2. Check that pip is available: `pip --version` (or `pip3 --version`)
3. Ensure both `install_*.sh/.bat` and `FileSecureSuite_1_0_0.py` are in the same directory
4. Try running the installer again

---

**FileSecureSuite v1.0 - Enterprise Encryption Suite**
