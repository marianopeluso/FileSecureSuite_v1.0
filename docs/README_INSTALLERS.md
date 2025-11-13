# FileSecureSuite - Installation Files

## What You Need

Choose based on your operating system:

### Windows
- **File:** `install_filesecure_windows.bat`
- **What to do:** Double-click or run in Command Prompt
- **Also need:** `FileSecureSuite_1_0_0.py` in the same folder

### Linux
- **File:** `install_filesecure_linux.sh`
- **What to do:** `bash install_filesecure_linux.sh`
- **Also need:** `FileSecureSuite_1_0_0.py` in the same folder

### macOS
- **File:** `install_filesecure_macos.sh`
- **What to do:** `bash install_filesecure_macos.sh`
- **Also need:** `FileSecureSuite_1_0_0.py` in the same folder

---

## Quick Start (3 Steps)

1. **Download all three files:**
   - `install_filesecure_*.bat/.sh` (for your OS)
   - `FileSecureSuite_1_0_0.py`
   - Put them in the same folder

2. **Run the installer:**
   - **Windows:** Double-click `install_filesecure_windows.bat`
   - **Linux:** `bash install_filesecure_linux.sh`
   - **macOS:** `bash install_filesecure_macos.sh`

3. **Follow the prompts:**
   - Confirm Python installation
   - Choose if you want a virtual environment (recommended: yes)
   - Wait for dependencies to install
   - See "Ready to launch" message

---

## What the Installer Does

✅ Checks for Python 3.8+  
✅ Offers to create a virtual environment (optional)  
✅ Installs all dependencies (cryptography, qrcode, colorama, tqdm, pyperclip)  
✅ Tells you exactly how to launch the app  

---

## After Installation

The installer will tell you how to run the app. Typically:

**Windows:**
```cmd
python FileSecureSuite_1_0_0.py
```

**Linux/macOS (with venv):**
```bash
source venv/bin/activate
python3 FileSecureSuite_1_0_0.py
```

**Linux/macOS (without venv):**
```bash
python3 FileSecureSuite_1_0_0.py
```

---

## System Requirements

- **Python 3.8 or higher** (not pre-installed? Download from https://www.python.org)
- **Internet connection** (for first installation only)
- **5-10 minutes** for complete setup

---

## If Something Goes Wrong

**Windows - Python not found:**
1. Download Python: https://www.python.org/downloads/
2. During install, CHECK "Add Python to PATH"
3. Restart Command Prompt
4. Try installer again

**Linux - Python not found:**
```bash
# Ubuntu/Debian
sudo apt install python3 python3-pip python3-venv -y

# Fedora
sudo dnf install python3 python3-pip -y

# Arch
sudo pacman -S python python-pip -y
```

**macOS - Python not found:**
```bash
# Using Homebrew
brew install python@3.11
# OR download from https://www.python.org/downloads/macos/
```

---

## Full Documentation

See `INSTALLATION_INSTRUCTIONS.md` for detailed step-by-step guide.

---

**Ready to go!** 🚀
