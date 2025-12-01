# Post-install settings
### Enable system services
```
systemctl enable NetworkManager.service
systemctl enable firewalld.service
systemctl enable fstrim.timer
systemctl enable reflector.timer # make sure to first edit /etc/xdg/reflector/reflector.conf
```
Reboot. Then default firewall default zone: `firewall-cmd --set-default-zone=trusted`. The default is usually public. Then reboot once again.  


### Done
You are done and can install whatever you want. If desired, you can even set up your own MAC. 
