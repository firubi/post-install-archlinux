# Post-install settings
### Enable system services
```
systemctl enable NetworkManager.service
systemctl enable firewalld.service
systemctl enable fstrim.timer
systemctl enable reflector.timer # make sure to first edit /etc/xdg/reflector/reflector.conf
```
Reboot. Then default firewall default zone: `firewall-cmd --set-default-zone=trusted`. The default is usually public. Then reboot once again.  

### Hooks
Make the directory /etc/pacman/hooks and place the hooks in this repository there. 

### Set up sbctl
If you want to use sbctl with limine, the only thing you need to sign is the bootloader itself. Limine does its own checks and [bypasses EFI chainloading and signature checks](https://wiki.cachyos.org/configuration/secure_boot_setup/#limine).

### Done
You are done and can install whatever you want. This should serve as a really nice base. If desired, you can even set up your own MAC. 
