---
title: "macos, hostname, computer name"
date: 2022-03-09T09:17:42+01:00
draft: false
---

Change hostname

```bash
sudo scutil --set HostName <new host name>
```

Change bonjour hostname

```bash
sudo scutil --set LocalHostName <new host name>
```

Change computer name

```bash
sudo scutil --set ComputerName <new name>
```

Flush dns

```bash
dscacheutil -flushcache
```

Restart

```bash
sudo reboot
```
