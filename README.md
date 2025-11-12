# How to add the PRODUINO UNO 4u board to the Arduino IDE

## Automatic Installation (Recommended)

The easiest way to install the PRODUINO UNO 4u board support is through the Arduino IDE Board Manager.

### Step 1: Add Board Manager URL

1. Open Arduino IDE
2. Go to **File → Preferences** (or **Arduino → Preferences** on macOS)
3. In the "Additional Boards Manager URLs" field, add:
   ```
   https://github.com/cowboydaniel/PRODUINO-UNO-4u/raw/main/package_drazzy.com_index.json
   ```
   - If you already have other URLs there, separate them with a comma or put each on a new line

<img src="https://github.com/user-attachments/assets/preferences-board-manager-url.png" width="75%" height="75%">

### Step 2: Install DxCore with PRODUINO Support

1. Open **Tools → Board → Boards Manager...**
2. In the search box, type `DxCore`
3. Find **"DxCore by Spence Konde"** in the list
4. Select version **1.5.11-produino1** or later from the dropdown
5. Click **Install**

<img src="https://github.com/user-attachments/assets/boards-manager-install.png" width="75%" height="75%">

### Step 3: Select Your PRODUINO Board

After installation, you'll find the PRODUINO boards under **Tools → Board → DxCore**:

- **Produino Uno 4u (no bootloader)** - For UPDI programming
- **Produino Uno 4u (Optiboot)** - For serial programming with bootloader

<img src="https://github.com/user-attachments/assets/3bf714d8-54c0-4a8d-9c62-9cc9a801dd84" width="75%" height="75%">
<br><i>If using Arduino IDE version 1.8.19 or below.</i></br>
</br>

<img src="https://github.com/user-attachments/assets/d0bdf9a2-cebf-4ec0-8d03-f1eeaf5c1f02" width="75%" height="75%">
<br><i>If using Arduino IDE version 2.0 or higher.</i></br>

---

## Manual Installation (Advanced Users)

If you prefer to manually install or need to customize your installation, you can follow these steps:

### Prerequisites

If you haven't already installed DxCore, install it using these instructions: <i><a href="https://github.com/SpenceKonde/DxCore/blob/master/Installation.md#boards-manager-installation-now-strongly-recommended-unless-helping-with-core-development">installing DxCore.</a></i>

### Installation Steps

1. Locate your Arduino15 folder using these instructions: <i><a href="https://support.arduino.cc/hc/en-us/articles/360018448279-Open-the-Arduino15-folder">locating the Arduino15 folder.</a></i>

2. Locate the DxCore in the packages folder. It should look somewhat like the picture below:
   </br>
   <img src="https://github.com/user-attachments/assets/c2e16436-ec51-4670-afee-9fe49067674f" width="75%" height="75%">

3. Download this repository as a zip package

4. Copy the `variants` and `bootloaders` folders from this zip package into the DxCore directory you just located

5. Copy the `boards.txt` from this package and use it to replace the `boards.txt` in your DxCore installation

6. Close and reopen the Arduino IDE

---

## Board Details

The PRODUINO UNO 4u is based on the **AVR128DA28** microcontroller with:
- 128KB Flash
- 16KB SRAM
- 28-pin package
- Arduino UNO form factor with enhanced features

Choose between:
- **No bootloader** version for UPDI programming (full flash available)
- **Optiboot** version for serial programming (requires bootloader burning first)

## Support

For issues or questions about PRODUINO UNO 4u, please visit the [GitHub repository](https://github.com/cowboydaniel/PRODUINO-UNO-4u).

For DxCore documentation and support, visit the [DxCore repository](https://github.com/SpenceKonde/DxCore).
