# Unshitted Systemd
## A fork of Systemd solving every issue it's ever had.
### Fuck the mantainers
---
## "Why should I use Unshitted Systemd?"
Do you like the ease of Systemd, but don't love how slow and buggy it is? 
Do you hate how Systemd uses AI code and Age Verification? Well, this doesn't do either!

Here's what Unshitted Systemd fixes
- https://github.com/systemd/systemd/issues/437  - Using timeX.google.com by default for NTP (Which gives irregular time and is google bullshit)
- https://github.com/systemd/systemd/issues/1143 - PID1 stuck printing "Time has been changed" after changing time past 2038 on 32bit systems
- Systemd locks down /etc and makes it read-only - This doesn't.
- Systemd used to wait 20 seconds before fully logging out to let processes exit... this is obviously stupid af, as it wastes time on good computers, and isn't long enough for bad computers. It now actually waits for all processes to exit, Then fully logs out.

Speedups? My system saw a 4.5 second boot time speedup! With stock systemd, I'd boot in 23.5 seconds, now, I boot in 19!

And I'm fixing more issues and speeding things up every day!

## How to install:

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
