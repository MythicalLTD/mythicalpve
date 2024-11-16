# MythicalPVE

An legit way to activate proxmox!

## Features

Works for:

- Proxmox VE (5.x or later; 3.x and 4.x [require some manual actions](#compatibility-information-for-old-proxmox-ve-versions))
- Proxmox Mail Gateway (5.x or later)
- Proxmox Backup Server (1.x or later)

Highlights:

- Non-intrusive: zero modification of any system file
- Future-proof: persists between system updates & major upgrades
- Hassle-free: you can uninstall at any time
- Comes with standard Debian package, easy to manage and automate


## Usage

### Installation

1. Download the package 
```bash
curl -Lo mythical-pve.deb https://github.com/mythicalltd/mythicalpve/releases/latest/download/mythical-pve.deb
```
2. Install the package
```bash
dpkg -i mythical-pve.deb
```

Notes:

After installation, please refrain yourself from clicking the "check" button on the "Subscription" page. It will invalidate the cache and temporary revert your instance into an unlicensed status.

The fake subscription status doesn't grant you free access to the enterprise repository. You should switch to the no-subscription repository if not already done. Use the following method:

- [Proxmox VE (PVE)](https://pve.proxmox.com/wiki/Package_Repositories#sysadmin_no_subscription_repo)
- [Proxmox Mail Gateway (PMG)](https://pmg.proxmox.com/pmg-docs/pmg-admin-guide.html#pmg_package_repositories)
- [Proxmox Backup Server (PBS)](https://pbs.proxmox.com/docs/installation.html#proxmox-backup-no-subscription-repository)

### Uninstallation

Run as root:

```shell
apt purge mythical-pve
```

This will revert your system to a "no subscription key" status.