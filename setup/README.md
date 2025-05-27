## Steps to Enable Hostname Discovery on Jetson Nano
1 - Install Avahi Daemon
Open a terminal on your Jetson Nano and run:
```
sudo apt update
sudo apt install avahi-daemon
```

2 - Start and Enable Avahi Daemon
Ensure the Avahi service is running and set to start on boot:
```
sudo systemctl enable avahi-daemon
sudo systemctl start avahi-daemon
```

3 - Verify Hostname
Check your current hostname:
```
hostnamectl
```

4 - If you wish to change it to something more recognizable:
```
sudo hostnamectl set-hostname jetson-nano

```

5 - Test Hostname Resolution
From another device on the same network, try pinging your Jetson Nano using its hostname:
```
ping jetson-nano.local
```

Repeat for other devices:
```
 ping jetson-tx2.local
 ping jetson-nano0.local
 ping jetson-nano1.local
 ping jetson-nano2.local
 ping jetson-nano3.local
 ping jetson-nano4.local
```