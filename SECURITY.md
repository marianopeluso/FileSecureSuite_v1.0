# 🔒 FileSecureSuite - Security Policy

**FileSecureSuite - Enterprise-grade file encryption with AES-256-GCM and RSA-4096**

## Release Verification

All FileSecureSuite releases are cryptographically signed with GPG to ensure authenticity and integrity.

### How to Verify a Release

#### Step 1: Import the Public Key (First Time Only)

```bash
# Download the public key
curl -O https://github.com/marianopeluso/FileSecureSuite/raw/main/filesecuresuite-public-key.asc

# Import it into GPG
gpg --import filesecuresuite-public-key.asc
```

#### Step 2: Download the Release Files

```bash
# Download from GitHub Releases
VERSION="1.0.0"
BASE_URL="https://github.com/marianopeluso/FileSecureSuite/releases/download/v${VERSION}"

# Download archive and signature
curl -LO "${BASE_URL}/filesecuresuite.zip"
curl -LO "${BASE_URL}/filesecuresuite.zip.asc"
curl -LO "${BASE_URL}/filesecuresuite.zip.sha256"
```

#### Step 3: Verify the GPG Signature

```bash
gpg --verify filesecuresuite.zip.asc filesecuresuite.zip
```

**Expected output:**
```
gpg: Signature made [DATE]
gpg:                using RSA key [KEY_ID]
gpg: Good signature from "Mariano Peluso <mariano@peluso.me>" [unknown]
```

✅ **"Good signature"** means the file is authentic and hasn't been tampered with.

⚠️ The warning `[unknown]` is normal and means you haven't personally verified the key owner's identity. This is acceptable for open-source projects.

#### Step 4: Verify the Checksum

```bash
# Verify SHA-256
sha256sum -c filesecuresuite.zip.sha256

# Or manually compare
sha256sum filesecuresuite.zip
cat filesecuresuite.zip.sha256
```

**Expected output:**
```
filesecuresuite.zip: OK
```

### Windows Users

**Install GPG:**
1. Download Gpg4win: https://www.gpg4win.org/download.html
2. Install with default options

**Verify signature:**
```cmd
gpg --verify filesecuresuite.zip.asc filesecuresuite.zip
```

**Verify checksum (without GPG):**
```cmd
certutil -hashfile filesecuresuite.zip SHA256
```
Compare the output with the hash in `filesecuresuite.zip.sha256`

---

## Public Key Fingerprint

**Key ID:** `F20494B9FAB53C10`
**Fingerprint:** `0FD97EB855F7C5BB1048D424F20494B9FAB53C10`

The public key is available:
- In this repository: [`filesecuresuite-public-key.asc`](./filesecuresuite-public-key.asc)
- On keyservers: `keys.openpgp.org`
- In GitHub Releases

To view the fingerprint:
```bash
gpg --fingerprint mariano@peluso.me
```

---

## Security Best Practices

When using FileSecureSuite:

1. **Verify every release** before installation
2. **Use strong passwords** for encryption
3. **Keep private keys secure** and backed up
4. **Verify file integrity** after decryption
5. **Update regularly** to get security patches

---

## Reporting Security Vulnerabilities

We take security seriously. If you discover a security vulnerability in FileSecureSuite:

### Please DO:
- ✅ Email us privately at: **mariano@peluso.me**
- ✅ Provide detailed steps to reproduce
- ✅ Allow us 90 days to fix before public disclosure
- ✅ Include proof-of-concept code if possible

### Please DO NOT:
- ❌ Open a public GitHub issue
- ❌ Disclose the vulnerability publicly before we've patched it
- ❌ Exploit the vulnerability maliciously

### Response Timeline

- **Initial Response:** Within 48 hours
- **Status Update:** Within 7 days
- **Fix Target:** Within 30-90 days (depending on severity)

### Hall of Fame

We'll acknowledge security researchers who responsibly disclose vulnerabilities.

---

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | ✅ Active support  |
| < 1.0   | ❌ No longer supported |

---

## Cryptographic Details

### Encryption Algorithms

**AES-256-GCM:**
- Key size: 256 bits
- IV: 16 bytes (randomly generated)
- Authentication: Built-in GCM authentication
- Mode: Authenticated encryption

**RSA-4096:**
- Key size: 4096 bits
- Padding: OAEP with SHA-256
- Use: Key exchange and asymmetric encryption

**PBKDF2:**
- Hash: SHA-256
- Configurable iterations (default: 100,000+)
- Salt: 16 bytes (randomly generated)

### Random Number Generation

FileSecureSuite uses `os.urandom()` for cryptographic random number generation, which is:
- Suitable for cryptographic use
- Platform-specific (e.g., `/dev/urandom` on Linux, `CryptGenRandom()` on Windows)
- Non-blocking

---

## Dependencies

FileSecureSuite relies on several third-party libraries. We monitor them for vulnerabilities:
- `cryptography` - NIST-approved cryptographic primitives
- `qrcode[pil]` - QR code generation
- `colorama` - Terminal colors
- `tqdm` - Progress bars
- `pyperclip` - Clipboard operations

Run `pip install --upgrade -r requirements.txt` regularly to get security updates.

---

## Compliance

### Open Source License

FileSecureSuite is released under the MIT License. See [LICENSE](./LICENSE) file for details.

### Export Compliance

This software uses cryptographic functions. Some countries may have restrictions on the import, possession, use, and/or re-export of encryption software. Please check your local laws before using or distributing this software.

---

## Additional Resources

- [Installation Guide](./INSTALLATION_INSTRUCTIONS.md)
- [Quick Start Guide](./QUICKSTART.md)
- [GPG Documentation](https://www.gnupg.org/documentation/)
- [Python Cryptography Library](https://cryptography.io/)

---

## Updates and Announcements

Security updates will be announced via:
- GitHub Releases
- Repository Security Advisories
- Commit messages with `[SECURITY]` tag

Subscribe to repository notifications to stay informed.

---

**Last Updated:** 2025-11-13


