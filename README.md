# Overview #

This is an alternative driver for Realtek RTS5129/RTS5139 USB MMC card reader for Linux.\
Based on [asymingt/rts5139](https://github.com/asymingt/rts5139) <sub>(thanks to him)</sub>, packed into dkms module with fix for kernel 6.14.\
Use it if you have issues with builtin rtsx driver.

# Installation #

Firstly, install DKMS if it's not installed

For Ubuntu:
```
sudo apt update
sudo apt install dkms
```
For Fedora:
```
sudo dnf install dkms
```

Then run
```
cd /tmp
git clone https://github.com/why-d0-you-l1v3/rts5139-dkms.git
cd rts5139-dkms
sudo dkms add src
sudo dkms install rts5139/1.0
```

After this reboot and check if it works.

# Uninstalling #
If you want to uninstall it just run

```sudo dkms remove rts5139/1.0```

and reboot.

