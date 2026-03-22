# Unshitted Systemd
## A fork of Systemd solving every issue it's ever had.
### Fuck the mantainers

How to install:

Bleeding Edge Version:
```bash
git clone https://aur.archlinux.org/unshitted-systemd-git.git
cd unshitted-systemd-git

makepkg -s
sudo pacman -U --nodeps --overwrite '*' \
  unshitted-systemd-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-libs-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-resolvconf-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-sysvcompat-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-tests-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-ukify-260-1-x86_64.pkg.tar.zst
```

Stable Version:
```bash
Stay tuned!
```
