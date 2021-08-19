# install-ubuntu20-on-dell-with-rst-off

1. Make bootable ubuntu
  Refer https://askubuntu.com/questions/1233623/workaround-to-install-ubuntu-20-04-with-intel-rst-systems for the next steps
2. Change the settings in windows to open in safe mode
3. Go to bios and change the SATA operation to ACHI
4. Open the windows in safe mode
5. Change windows to open in normal mode and reboot

#Create partition for ubuntu and continue

6. Plug in installation medium and install ubuntu
7. After successfull installation, open ubuntu by pressing e and adding nomodeset on second last line
8. Open and install the latest nvidia driver
9. sudo apt install --reinstall nvidia-prime
10. sudo prime-select nvidia
11. sudo update-initramfs -u
12. Add the following lines to the file "/etc/initramfs-tools/modules"
nvidia
nvidia-drm
nvidia-modeset

https://forums.developer.nvidia.com/t/black-screen-after-install-of-nvidia-driver-ubuntu/109312/4
https://forums.developer.nvidia.com/t/black-screen-after-install-of-nvidia-driver-ubuntu/109312/4
