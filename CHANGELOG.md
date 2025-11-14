# Changelog

All notable changes to FileSecureSuite are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.2] - 2025-11-14

### Fixed
- **SyntaxError in QR code display** (line 1372)
  - Fixed f-string expression containing backslash character
  - Moved newlines outside f-string expression for Python 3.6+ compatibility
- **QR code viewer not opening on Linux/macOS**
  - Fixed subprocess calls not properly backgrounding image viewers
  - Improved xdg-open and eog compatibility
  - Added proper error handling for missing viewers

### Improved
- Cross-platform image viewer handling (Windows/Linux/macOS)
- Subprocess error handling and fallback mechanisms
- Headless environment detection and handling
- File permission handling across platforms

### Tested On
- Windows 10/11 (CMD)
- Linux Desktop (GNOME/KDE/XFCE)
- Kali Linux (Headless SSH)
- Remote Desktop environments

---

## [1.0.1] - 2025-11-13

### Fixed
- Cross-platform line ending normalization (CRLF → LF)
- UTF-8 encoding issues on Linux systems
- File encoding standardization for Python 3.6+ compatibility

---

## [1.0.0] - 2025-11-13

### Added
- Core encryption features with AES-256-GCM and RSA-4096
- Interactive CLI menu system with color-coded output
- File encryption/decryption with HMAC verification
- Text encryption/decryption from command line
- RSA key pair generation and management
- QR code generation for key sharing
- PBKDF2 key derivation with configurable iterations
- Batch file processing capabilities
- Cross-platform support (Windows, macOS, Linux)
- Automated installers for all platforms
- Progress bars for file operations
- Clipboard integration for key management

### Security
- AES-256-GCM for authenticated encryption
- RSA-4096 for asymmetric encryption
- PBKDF2 with SHA-256 for key derivation
- HMAC-based integrity verification
- Secure random salt generation
- Restrictive file permissions (owner only)
- No plaintext key storage

### Documentation
- Comprehensive README with features and quick start
- Detailed installation instructions for all platforms
- Windows Python installation guide
- Installer usage documentation

---

## Future Releases

### Planned for v1.1.0
- Command-line interface improvements (argparse)
- Performance optimizations
- Better error messages
- Password strength meter

### Planned for v2.0.0
- GUI application (Tkinter/PyQt)
- Streaming encryption for large files
- Compression before encryption
- Certificate-based encryption

---

**Current Version:** 1.0.2  
**Release Date:** 2025-11-14  
**Status:** Production Ready
