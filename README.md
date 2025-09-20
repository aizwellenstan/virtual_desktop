## 🖥️ Virtual Monitor Setup Guide

### 🔧 Installation

1. **Run `install.bat` with administrator privileges.**

2. **Activate the virtual monitor:**
   ```bash
   deviceinstaller64 enableidd 1
   ```
   - Run this command up to **four times** to add up to **four virtual monitors** on Windows 10.
   - On a **32-bit system**, replace `deviceinstaller64` with `deviceinstaller`.

3. **Automated Setup (Recommended):**
   - Use the included batch file `usbmmidd.bat` to automate the setup.
   - It detects your system architecture and runs the correct version of `deviceinstaller`.
   - To use it, **right-click** on `usbmmidd.bat` and select **"Run as Administrator"**.

---

### 🖼️ Display Configuration

- After activation, a **high-definition monitor** will appear in your system's Display Settings.
- Default resolution: **1920x1080 pixels**.
- To specify custom resolutions, refer to the included `idd_instructions.txt` file.
- You can reposition, extend, or configure the virtual monitor just like a physical one.

---

### 🔄 Managing Virtual Monitors

- **Deactivate:**
  ```bash
  deviceinstaller64 enableidd 0
  ```
  - Run multiple times if you’ve added more than one virtual display.

- **Reactivate:**
  ```bash
  deviceinstaller64 enableidd 1
  ```

---

### 🧹 Uninstalling Drivers

To completely remove the virtual display drivers:

- Option 1: Use **Device Manager** to uninstall `USB Mobile Monitor Virtual Display`.
- Option 2: Run the following commands:
  ```bash
  deviceinstaller64 stop usbmmidd
  deviceinstaller64 remove usbmmid
  ```
