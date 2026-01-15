
先設定 /boot/firmware/config.txt
最後加入:
For raspberry Pi 5 NVMe:
dtparam=pciex1_gen=3
For raspberry DAC HAT:
dtoverlay=hifiberry-dacplus,slave


最後使用 sudo rpi-eeprom-config --edit 修改開機順序（BOOT_ORDER）為 0xf416，再次重開機即可。
使用 sudo rpi-eeprom-config --edit 修改 eeprom 設定，原本的開機順序（BOOT_ORDER）為 0xf461。


#----------------------------------------------
Ansible







mpd.service(Port:6600)
                      - "For Pi       Audio"  
                      - "For Pc       Audio"  port:8300
                      - "For Icecast Audio"-->
-- mpd.service            to : icecast2.service:  192.168.2.253:8600/mpdstream.ogg       
-- ezstream.service       to : icecast2.service:  192.168.2.253:8600//ezstream.ogg

Pi_Media_Server(Port:8100)
Pi_Mpd_Server(Port:8200)

