## Install Qemu

### Ubuntu Debian
```bash
pacman -Sy
apt-get install qemu-guest-agent
```

### Redhat
```bash
yum install qemu-guest-agent
```

## Start Qemu Agent
```bash
systemctl start qemu-guest-agent
```
## Enable autostart
```bash
systemctl enable qemu-guest-agent
```
