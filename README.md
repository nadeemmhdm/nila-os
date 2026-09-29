<div align="center">

# Nila OS

### Your computer. Your intelligence.

**An experimental, offline-first AI-native Linux project focused on privacy, control, and transparent permissions.**

[![Website](https://img.shields.io/badge/Website-Live-8adba0?style=for-the-badge)](https://nadeemmhdm.github.io/nila-os/)
[![Project stage](https://img.shields.io/badge/Stage-Developer%20Preview-e8b86a?style=for-the-badge)](docs/STATUS.md)
[![License](https://img.shields.io/badge/License-MIT-91a7ff?style=for-the-badge)](LICENSE)
[![Website deployment](https://github.com/nadeemmhdm/nila-os/actions/workflows/pages.yml/badge.svg)](https://github.com/nadeemmhdm/nila-os/actions/workflows/pages.yml)

[Explore the website](https://nadeemmhdm.github.io/nila-os/) · [VM setup](docs/VM_SETUP.md) · [Releases](https://github.com/nadeemmhdm/nila-os/releases) · [Development status](docs/STATUS.md)

</div>

---

> [!IMPORTANT]
> **Nila OS is an experimental developer preview, not a complete or verified operating system.** This repository currently publishes the project website, setup documentation, and project policies. It does **not** provide a tested bootable ISO or a fully integrated local AI assistant.

## Overview

Nila OS is a proposed Debian-based desktop experience designed to keep AI inference local, put users in control of privileged actions, and make installation and recovery understandable. The roadmap includes a lightweight local assistant, an independent permission gateway, auditable task execution, and recovery tools. These are **design goals**, not claims of completed functionality.

## Project pillars

| Area | Design direction | Current state |
|:--|:--|:--|
| Local AI | Lightweight CPU-compatible models with offline-first operation | Planned; no bundled model |
| Permission controls | Explicit approvals before sensitive AI actions | Not independently verified |
| Isolation and audit | Restricted workspaces and inspectable activity history | Experimental roadmap |
| Resilience | Emergency AI-free mode, watchdog, update verification, rollback | Planned |
| VM experience | Clear Debian/VirtualBox development path | Documentation available |
| Project website | Responsive landing page with accessible animated icons | Published |

See the [implementation status](docs/STATUS.md) for the current scope and limitations.

## Getting started

### Option 1: Explore the website

Visit **[nila-os project website](https://nadeemmhdm.github.io/nila-os/)** to read about the vision and find source and setup links.

### Option 2: Prepare a development VM

1. Install [VirtualBox](https://www.virtualbox.org/) and download an [official Debian installer](https://www.debian.org/distrib/).
2. Create a Debian 64-bit VM. Suggested configuration for a host with sufficient resources: **4 GB guest RAM, 2 vCPU, 35 GB dynamically allocated storage**, NAT networking.
3. Install Debian with the XFCE desktop and take a clean snapshot.
4. Follow the complete **[VM setup guide](docs/VM_SETUP.md)**.

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y git python3 python3-venv python3-pip curl
git clone https://github.com/nadeemmhdm/nila-os.git
cd nila-os
```

These commands prepare the development environment; they do **not** install a custom Nila OS distribution.

## Downloads and releases

- **[Releases](https://github.com/nadeemmhdm/nila-os/releases)** — versioned developer previews when published.
- **[Download repository source](https://github.com/nadeemmhdm/nila-os/archive/refs/heads/main.zip)** — current source and documentation.
- **Bootable ISO:** unavailable until the image is built, independently installed in a VM, and published with checksums.

Do not mistake a source archive for an installable OS image.

## Roadmap

- [x] Publish the project website and responsive navigation.
- [x] Publish VM setup documentation and project policies.
- [ ] Publish and test the Python developer backend in this repository.
- [ ] Integrate and benchmark a CPU-friendly local model in the VM.
- [ ] Implement and audit privileged permission mediation.
- [ ] Produce a reproducible Debian-based ISO.
- [ ] Verify clean VM boot, installation, offline behavior, updates, and recovery.

## Repository layout

```text
.github/workflows/   GitHub Pages and release automation
site/                Static project website
docs/                VM setup and implementation status
README.md            Project overview
SECURITY.md          Vulnerability reporting and limitations
CONTRIBUTING.md      Contribution guidelines
LICENSE              MIT license
```

## Security and contributions

Security-critical features are experimental. Do not rely on this project to protect sensitive files or devices. Never commit credentials, personal memory, encryption keys, VM images, or tokens.

Read [SECURITY.md](SECURITY.md) before reporting a vulnerability and [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes. Contributions, documentation corrections, and reproducible test reports are welcome.

---

<div align="center">

**Built openly. Designed for user control.**

[Website](https://nadeemmhdm.github.io/nila-os/) · [GitHub Issues](https://github.com/nadeemmhdm/nila-os/issues) · [License](LICENSE)

</div>
