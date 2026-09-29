# Virtual Machine Setup — Nila OS Development

> There is currently **no verified bootable Nila OS ISO**. These steps prepare a Debian VM for development and future Nila OS installation. They do not install a complete custom OS.

## Host requirements

- Windows, Linux or macOS host with hardware virtualization enabled.
- Suggested for an 8 GB host: 4 GB VM RAM (reduce if the host becomes unstable), 2 vCPU, dynamically allocated 35 GB virtual disk.
- Internet is required for Debian and initial package downloads; offline local inference is a future goal.

## Steps

1. Install Oracle VirtualBox from https://www.virtualbox.org/ and download an official Debian installer from https://www.debian.org/distrib/.
2. VirtualBox → **New** → name **Nila OS Dev** → Linux / Debian (64-bit). Choose the Debian ISO you downloaded.
3. Set **4096 MB RAM**, **2 CPU cores**, and a **35 GB dynamically allocated VDI**. Enable EFI only if appropriate for your chosen Debian installation; use NAT networking initially.
4. Start the VM, install Debian with XFCE desktop and create your own strong administrator password. Do **not** use default credentials such as nila/nila.
5. Update Debian inside the VM:

   ```bash
   sudo apt update && sudo apt upgrade -y
   sudo apt install -y git python3 python3-venv python3-pip curl
   ```

6. Clone this repository:

   ```bash
   git clone https://github.com/nadeemmhdm/nila-os.git
   cd nila-os
   ```

7. This repository currently publishes the website and project documentation only. The developer backend and ISO builder will be added after review; do not expect `./scripts/install.sh` to exist yet.
8. Take a VirtualBox snapshot called **Clean Debian Base** before installing future experimental components.

## Security

Use NAT rather than bridged networking until remote services are audited. Do not forward API ports or expose Telegram tokens. Keep the VM separate from sensitive host files. A VM cannot enforce password protection against host-side power-off.

## Future installation

When a bootable ISO is actually published, a checksum, release notes, VM boot test results and verified download link will be provided on the website.
