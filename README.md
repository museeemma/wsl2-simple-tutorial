# wsl2-simple-tutorial
tutorial for setting up any linux distribution e.g kali and  setting up a bootable device
# How to Install WSL2 on Windows or alternatetively boot linux  from your external disk e.g flashdisk

<b>Windows Subsystem for Linux</b> _(WSL)_ allows you to run a Linux enviroment directly on your windows machine without the need to separate virtual machine or dual booting .its like an app that lets you experience linux distributions likee.g kali or ubuntu

## THESE IS FOR WSL
### first step
#### 1. Check Windows Version and WSL Version
Ensure you are using a compatible version of Windows that supports WSL. You can check your Windows version by running __**winver**__ in the windows search bar.
**it must be Windows 10 (version 1903 and higher) or Windows 11.** 
#####
The first you need to do is to enable virtualisation feature on your laptop or pc.

### Open Windows Features:

Press Win + R to open the Run dialog.
Type **optionalfeatures** and press Enter.
Enable Virtual Machine Platform and enable **hype v**

### method  2. Enable Virtual Machine Platform using powershell



1. In the same PowerShell window, run:

    ``` powershell
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    ```

**then run**
```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

### 3. Restart Your Computer

Restart your computer to apply the changes.

 #### Verify  if Virtualization is Enabled ##
Open Task Manager:<br>
1. Press Ctrl + Shift + Esc to open Task Manager.<br>
1. Check Virtualization Status:<br>
1. Go to the Performance tab.<br>
1. Select CPU in the left pane.<br>
1. Look for the Virtualization section in the right pane. It should indicate Enabled if virtualization is correctly set up.<br>
### 4. Set WSL2 as the Default Version

After your computer restarts, set WSL2 as the default version:

1. Open PowerShell as Administrator and run:

    ```powershell
    wsl --set-default-version 2
    ```

### 5. Install a Linux Distribution

Now, you can install a Linux distribution of your choice from the Microsoft Store.Here is the link 
[linux distribution](https://www.microsoft.com/p/kali-linux/9pkr34tncv07)

1. Open the Microsoft Store and search for your preferred Linux distribution (e.g., Ubuntu).
2. Click on the distribution you want to install and click `Get` to download and install it.

### 6. Launch the Linux Distribution

After the installation is complete, launch the Linux distribution from the Start menu.

1. On the first launch, you will need to create a user account and password.

### 7. Verify the Installation

To verify that you are using WSL2, open your installed Linux distribution and run:

```sh
wsl --list --verbose
```
## how to run linux on a external hard drive e.g flashdisk
### _requirements_
1. A USB drive with at least 8 GB of storage.
2. A USB bootable creation tool e.g **Rufus** for Windows
### steps
#### Step1
<kbd>Download the Kali Linux ISO:<kbd>
#### step2
<kbd>Download a USB Bootable Creation Tool **rufus**</kbd>

#### Open Rufus:

<KBD>In Rufus, select your USB drive under "Device."
THEN
Click on "Select" and choose the downloaded Kali Linux ISO file.
Configure Rufus:
#### SET THIS SETTINGS
Partition scheme: MBR for BIOS or UEFI.<BR>
File system: FAT32.<BR>
Start the Process:
### HOW TO RUN
 As your computer starts up, enter the BIOS settings. This is usually done by pressing a specific key during the boot process.
1. F2: Dell, Acer
1. F12: Lenovo, HP
1. ESC: HP, Toshiba
1. DEL: MSI, ASUS
   
### CHANGE BOOT ORDER
#### Set USB as First Boot Device:

1.Change the boot order to prioritize the USB drive.<BR> 2.Move the USB drive to the top of the list or select it as the primary boot device.<BR>
3. Save Changes and Exit:<BR>
4.Save your changes
