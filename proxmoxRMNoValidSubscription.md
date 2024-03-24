# No valid subscription
You do not have a valid subscription for this server. Please visit www.proxmox.com to get a list of available options.

Open widget toolkit
```bash
cd /usr/share/javascript/proxmox-widget-toolkit
```

Backup file
```bash
cp proxmoxlib.js proxmoxlib.js.bak
```

Open file
```bash
nano proxmoxlib.js
```

Serch for if ( res ==

change if statment to false to never trigger the message
