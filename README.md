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
You are done and can install whatever you want. This should serve as a really nice base. Below is an exhaustive list of what I usually install:
```
pipewire
wireplumber
pipewire-audio
pipewire-pulse
pipewire-jack
pipewire-alsa
bluez
noto-fonts
noto-fonts-cjk
noto-fonts-extra
noto-fonts-emoji
ttf-noto-nerd
ttf-liberation
ttf-jigmo
plasma-desktop
xdg-desktop-portal-gtk
breeze-gtk
kde-gtk-config
firefox
kwallet-pam
plasma-nm
plasma-pa
bluedevil
kscreen
dolphin
gwenview
spectacle
okular
ark
7zip
unrar
papirus-icon-theme
ffmpegthumbs
kdegraphics-thumbnailers
plasma-systemmonitor
mpv
yt-dlp
foot
fastfetch
sddm
sddm-kcm
steam
libvirt
qemu-desktop
virt-manager
flatpak
```

