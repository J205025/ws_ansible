NTP Server
===
Systemd timer
---
- https://www.youtube.com/watch?v=DixhIrgMy3M&list=PLtK75qxsQaMKPbuVpGuqUQYRiTwTAmqeI&index=5
 - https://github.com/groovemonkey/tutorialinux-systemd-timers
 - gpsd can provide reference clock information to ntpd or chronyd
 - You can see the output of gpsd to ntpd in real time with the ntpshmmon command.
- $ sudo ntpshmmon
check status
---
- $ lsusb 
- $ ls -al /dev/ttyUSB*
gps check
---
- https://gpsd.gitlab.io/gpsd/gpsmon.html
- $ gpsmon -h
- $ gpsmon -V
- $ gpsmon  /dev/ttyAMA0
- $ gpsmon /dev/ttyUSB0

- 可以通過下面兩個命令來查看連接狀態
- 數據統計：chronyc sources -v
- 源狀態： chronyc sourcestats -v
- 如果想要連續觀察，可以藉助linux的watch命令，即
- watch -n1 chronyc sources -v
- watch -n1 chronyc sourcestats -v
gpsd can provide reference clock information to ntpd or chronyd
---
 - You can see the output of gpsd to ntpd in real time with the ntpshmmon command.
- $ ntpshmmon
- $ chronyc sources -v 
- $ chronyc sourcestats -v
- $ chronyc tracking
- $ cgps
- $ xgps
- $ vcgencmd  
- The vcgencmd tool is used to output information from the VideoCore GPU on the Raspberry Pi. You can find source code for the vcgencmd utility on Github.
- ref: https://blog.gtwang.org/iot/raspberry-pi-vcgencmd-hardware-information/
- $ vcgencmd measure_volts
- $ vcgencmd measure_temp

- $ dmidecode (查 BIOS 主機板 資訊)
檢查 systemd-timesyncd 服務狀態
---
- 手動寫入時間
- $- systemctl status systemd-timesyncd
- $ timedatectl
- $ sudo timedatectl set-ntp no
- $ sudo timedatectl set-time "2016-11-12 18:10:40"
- $ sudo timedatectl set-ntp yes
- $ timedatectl set-timezone "Asia/Taipei"  或用sudo dpkg-reconfigure tzdata

