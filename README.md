# Windows & Microsoft Office Installation Guide

---

## Part 1: Installing Windows

### Step 1: Download Windows

1. Go to the [Microsoft Windows official page](https://www.microsoft.com/en-us/software-download/).
2. Choose the version of Windows you want to install.
3. Select the **ISO image** option and download it.

### Step 2: Create a Bootable USB Drive

- **If the downloaded file is a `.exe`:**
  1. Run the `.exe` file.
  2. Follow the prompts and save the output to a known folder on your computer.

- **If the downloaded file is an `.iso`:**
  1. Download [Rufus](https://rufus.ie/).
  2. Open Rufus.
  3. Under **Device**, select your USB flash drive.
  4. Under **Boot selection**, choose the downloaded ISO file.
  5. Leave the **File partition** settings at their defaults.
  6. Click **Start** and wait for the process to complete.

### Step 3: Boot from the USB Drive

1. Restart your computer and enter the **BIOS/UEFI** settings (usually by pressing `F2`, `F12`, `DEL`, or `ESC` during startup — depends on your machine).
2. Navigate to the **Boot** section and set your USB flash drive as the **primary boot device**.
3. Save and exit BIOS. Your computer will boot from the USB drive.

### Step 4: Install Windows

1. Follow the on-screen instructions to install Windows.
2. Once the installation is complete, the machine will restart.
3. **Remove the bootable USB drive** when prompted (or immediately after the restart begins).

---

## Part 2: Installing Microsoft Office 365

### Step 1: Download the Office Deployment Tool

1. Go to the [Office Deployment Tool page](https://www.microsoft.com/en-us/download/details.aspx?id=49117) on the Microsoft website.
2. Click on it and download it.

### Step 2: Configure Office Using the Customization Tool

1. Go to the [Office Customization Tool](https://config.office.com/).
2. Click on **Configuration**.
3. Click **Export**, then choose **Office Open XML Format**.
4. Save the exported `configuration.xml` file.

### Step 3: Set Up the Office Folder

1. Create a new folder and name it **Office365**.
2. Add both files to it:
   - The Office Deployment Tool (`setup.exe`)
   - The configuration file (`configuration.xml`)
3. Move the **Office365** folder to:
   ```
   C:\Program Files\
   ```

### Step 4: Install Office via Terminal

1. Open **Terminal** (or Command Prompt) as **Administrator**.
2. Change the directory to the Office folder:
   ```cmd
   cd "C:\Program Files\Office365"
   ```
3. Run the following command to begin installation:
   ```cmd
   setup /configure configuration.xml
   ```
4. The Microsoft Office suite will begin installing automatically.

---

## Part 3: Activating Windows & Office

### Activate Using PowerShell

1. Open **PowerShell** as **Administrator**.
2. Run the following command:
   ```powershell
   irm https://get.activated.win | iex
   ```
3. From the menu that appears, select **OHOOK**.
4. Choose **Install OHOOK** to activate.

---

> **Note:** Always ensure your internet connection is stable during installation and activation steps.
