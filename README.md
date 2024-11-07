
Guide for setting up Raspberry Pi with Comitup for headless Wi-Fi configuration


Required hardware : 
Raspberry Pi Zero Wireless WH (Pre-Soldered Header)
https://robu.in/product/raspberry-pi-zero-wireless-wh-pre-soldered-header/
Standard 5V 3A Power Supply with Micro USB Plug
SanDisk Micro SD/SDHC 32GB Class 10 Memory Card

Steps: 
Download Comitup Image: Download the Comitup Raspberry Pi OS image (Lite or full version) from the official website. (https://davesteele.github.io/comitup/)
Flash the SD Card: Use an imaging tool (balenaEtcher software) to write the image to the SD card (Prefer 32GB).
Insert SD and Boot: Insert the SD into the Raspberry Pi and power it ON. SSH is enabled by default; use comitup (case-sensitive) as both username and password. 
Access Comitup Network: If no known Wi-Fi is detected, a comitup-xxxx AP will appear.
Web Interface: Connect to this AP and go to http://comitup.local or 10.0.0.2/24 to manage network connections.
Note: Once your Raspberry Pi boots up, wait a moment and check your Wi-Fi networks on your phone. You should see an open access point named comitup-XXX. Connect to it, and a web interface will automatically open. Select your Wi-Fi router from the list, enter the router password, and submit. The Raspberry Pi will try to connect to your Wi-Fi. Once connected, you can access the Pi via SSH using software like Putty, enabled by default for remote management.
Download Putty from https://www.putty.org/
Network Scanner App: Use an app like Fing (iOS/Android) or Advanced IP Scanner (https://www.advanced-ip-scanner.com/)(Windows) to scan your network and locate devices, including the Raspberry Pi.
After Getting Raspberry pi IP address, You can connect Raspberry pi via Putty software.
Connect via SSH: Once you have your Raspberry Pi’s IP address, use Putty to connect over SSH.
Login: Enter the username (comitup) and password (comitup). The password won’t show as you type—just type it carefully and press Enter.
Access Terminal: You’re now logged in to the Raspberry Pi’s terminal.
Enable VNC Server:
Run sudo raspi-config.
Go to Interface Options > VNC > Enable.
If using Comitup Lite, install a GUI first with sudo apt-get install lightdm.
Set Auto Login (GUI): In System Options of raspi-config, set the boot to auto-login to GUI.
Install VNC Viewer: Install VNC Viewer on your computer, create an account, and log in.
Connect: In VNC Viewer, enter the Raspberry Pi’s IP address and log in with your Pi’s default credentials.
Cloud Access: For remote access, add the Pi to VNC Cloud; free accounts allow up to 5 systems.

