2.1.1 Open terminal. <br />
2.1.2 Enter `echo options hid_apple fnmode=0 | sudo tee -a /etc/modprobe.d/hid_apple.conf`. <br />
2.1.3 Enter `sudo dracut --force` if you're using Fedora; if you're using a Debian-based distro, enter `sudo update-initramfs -u`. <br />
2.1.4 Reboot your PC.

### NOTE: If that doesn't work, you might have to change `fnmode` to "2".
