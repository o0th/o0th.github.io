---
title: "linux, kernel"
date: 2022-02-14T09:08:42+01:00
draft: false
---

Install a different linux version

```bash
yay -S linux-zen
```

Update grub

```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

Remove linux

```bash
yay -R linux-zen
```
