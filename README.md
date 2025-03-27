# LXC Template for Proxmox - UniFi Controller

This repository provides an LXC template for running the UniFi Network Controller inside a lightweight Proxmox LXC container.

## Features
- Preconfigured Ubuntu/Debian-based LXC template
- Minimal resource usage
- Automatic installation of UniFi Controller
- Optimized networking for Proxmox

## Requirements
- Proxmox VE (latest version recommended)
- Internet connection for downloading packages
- Sufficient resources (CPU/RAM) depending on the number of UniFi devices

## Installation
1. Clone this repository or download the LXC template.
2. Import the LXC template into Proxmox:
   ```sh
   pct create <vmid> /path/to/lxc-template.tar.gz -storage <storage>
   ```
3. Start the container:
   ```sh
   pct start <vmid>
   ```
4. Access the UniFi Controller web interface via `https://<container-ip>:8443`

## Configuration
- Ensure the correct network bridge is assigned.
- Adjust memory and CPU resources as needed in Proxmox.
- Update UniFi Controller regularly via package manager.

## Troubleshooting
If you encounter issues, check logs with:
```sh
journalctl -u unifi -f
```

## Contributing
Pull requests and suggestions are welcome!

## License
This project is licensed under the MIT License.

