## Install Qemu

### Arch linux
```bash
sudo pacman -Sy
sudo pacman -S qemu-guest-agent
```
### Ubuntu Debian
```bash
sudo apt-get install qemu-guest-agent
```

### Redhat
```bash
sudo yum install qemu-guest-agent
```

## Start Qemu Agent
```bash
sudo systemctl start qemu-guest-agent
```
## Enable autostart
```bash
sudo systemctl enable qemu-guest-agent
```
