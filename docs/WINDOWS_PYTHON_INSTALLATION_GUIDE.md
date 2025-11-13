# Windows Python Installation Guide

## Step-by-Step Instructions with Screenshots

### Step 1: Download Python

1. Go to https://www.python.org/downloads/
2. Click the blue "Download Python" button (latest version)
3. Save the installer to your computer

---

### Step 2: Run the Installer

1. Find the downloaded file (usually in Downloads folder)
2. Double-click to run the installer
3. You'll see a window with installation options

---

### Step 3: IMPORTANT - Installation Options

#### ✅ MANDATORY - Add Python to PATH

**Look for this option in the installer:**

```
☑ Add Python 3.xx to PATH
```

**MUST be CHECKED (✓) - This is CRITICAL!**

If you miss this step, Python won't work from Command Prompt!

---

#### Optional Features (Recommended)

Check these boxes for better experience:

```
Optional Features:
☑ Documentation
☑ pip
☑ tcl/tk and IDLE
☑ Python test suite
☑ py launcher
```

---

### Step 4: Advanced Options

Look for "Advanced Options" or similar section:

```
Advanced Options:
☑ Associate files with Python
☑ Create shortcuts for installed applications
☑ Add Python to environment variables
```

**ALL of these should be CHECKED (✓)**

The key one is: **"Add Python to environment variables"**

---

### Step 5: Complete Installation

1. Click "Install Now" or "Customize installation"
2. Wait for installation to complete
3. You may see "Setup was successful" - Click "Close"

---

### Step 6: Verify Installation

1. **Open Command Prompt:**
   - Press `Win + R`
   - Type `cmd`
   - Press Enter

2. **Type this command:**
   ```cmd
   python --version
   ```

3. **You should see:**
   ```
   Python 3.11.x (or higher)
   ```

   ✅ If you see this - Python is installed correctly!
   ❌ If you see "python is not recognized" - Go back to Step 3 and check "Add Python to PATH"

---

### Step 7: Verify pip

Still in Command Prompt, type:
```cmd
pip --version
```

You should see:
```
pip 24.x.x from C:\Users\...
```

✅ If you see this - pip is ready!

---

## Common Issues & Solutions

### Issue: "python is not recognized"

**Solution:**

1. **Uninstall Python completely:**
   - Settings → Apps → Apps & Features
   - Find "Python 3.xx"
   - Click Uninstall

2. **Restart your computer**

3. **Download Python again** from https://www.python.org/downloads/

4. **Run installer and THIS TIME:**
   - ☑ ADD PYTHON TO PATH (this is the key!)
   - ☑ Add Python to environment variables
   - Click Install

5. **Restart Command Prompt**

6. **Test again:**
   ```cmd
   python --version
   ```

---

### Issue: "pip is not recognized"

**Solution:**

If Python works but pip doesn't:

1. Make sure you checked "pip" during Python installation
2. Use full path:
   ```cmd
   python -m pip --version
   ```

---

## Once Python is Working

1. Open Command Prompt
2. Navigate to your FileSecureSuite folder:
   ```cmd
   cd C:\Users\YourUsername\Downloads\FileSecureSuite
   ```

3. Run the installer:
   ```cmd
   install_filesecure_windows.bat
   ```

4. Follow the prompts

Done! ✅

---

## Visual Checklist

When installing Python, ensure these are CHECKED:

```
Installation Screen:
☑ pip (downloads packages)
☑ Add Python X.X to PATH (CRITICAL!)
☑ Associate files with Python
☑ Create shortcuts for applications

Advanced Options:
☑ Add Python to environment variables
☑ Create shortcuts for installed applications
```

---

## What Each Option Does

| Option | Purpose | Need it? |
|--------|---------|----------|
| **Add Python to PATH** | Allows Command Prompt to find Python | 🔴 **YES** |
| pip | Package installer | 🔴 **YES** |
| Documentation | Python docs (optional) | 🟡 No |
| tcl/tk and IDLE | Development tools | 🟡 No |
| py launcher | Quick Python launcher | 🟡 No |

---

## After Installation - Next Steps

Once Python is verified working:

1. Download FileSecureSuite_Installation.zip
2. Extract it
3. Put all files in same folder with FileSecureSuite_1_0_0.py
4. Run install_filesecure_windows.bat
5. Done!

---

**Key Takeaway:**

❗ **The most common problem is forgetting to check "Add Python to PATH"**

If installation doesn't work, this is 99% of the time the reason!

Re-install and make sure this box is CHECKED! ✓
