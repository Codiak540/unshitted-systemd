<h1>Unshitted Systemd</h1>
<hr />
<h2> A fork of Systemd trying to solve every issue it's ever had.
</h2>
<hr />

<strong><i>
This is a fork of systemd, do not bother the official systemd about issues or questions related to this fork
</strong></i>

<hr />

<h2> "Why should I use Unshitted Systemd?"</h2>
Do you like the ease of Systemd, but don't love how slow and buggy it is? 
Do you hate how Systemd uses AI code and stores your private data? Well, this fixes those "Features"!

Here's what Unshitted Systemd fixes
<ul>
<li> https://github.com/systemd/systemd/issues/437  - Using timeX.google.com by default for NTP (Which gives irregular time and is google bullshit)</li>
<li> https://github.com/systemd/systemd/issues/1143 - PID1 stuck printing "Time has been changed" after changing time past 2038 on 32bit systems</li>
<li> Systemd locks down /etc and makes it read-only - This doesn't.</li>
<li> Systemd used to wait 90 seconds before fully logging out to let processes exit... this is obviously stupid af, as it wastes time on good computers, and isn't long enough for bad computers. It now actually waits for all processes to exit, Then fully logs out.</li>
<li> Optimized binfmt</li>
</ul>

Here's what Unshitted Systemd removes
<ul>
<li>All AI Code </li>
<li> Fields for the Users Birthday </li>
<li> Fields for the Users Real Name </li>
</ul>

Speedups? My system saw a 4.5 second boot time speedup! With stock systemd, I used to boot in 23.5 seconds, now, I boot in 19!

And I'm planning on fixing more issues and speeding things up every day!
<hr />
<h2>How to install:</h2>

<h3>Bleeding Edge Version:</h3>
```bash

git clone https://aur.archlinux.org/unshitted-systemd-git.git
cd unshitted-systemd-git

makepkg -si
```

If makepkg -si doesn't work, do
```bash

makepkg -s

sudo pacman -U --nodeps --overwrite '*' \
  unshitted-systemd-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-libs-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-resolvconf-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-sysvcompat-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-tests-260-1-x86_64.pkg.tar.zst \
  unshitted-systemd-ukify-260-1-x86_64.pkg.tar.zst
```

Or you can use an AUR helper, such as paru or yay `paru unshitted-systemd-git` or `yay unshitted-systemd-git`

<h3>Stable Version</h3>
```bash
Stay tuned!
```
