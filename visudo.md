# visudo

edit sudoers:
```bash
sudo visudo
```

don't ask for password for ubuntu:
```bash
ubuntu ALL=(ALL) NOPASSWD:ALL
```

disable swap:
```bash
sudo swapoff -a
```

comment `/swap.img` line:
```bash
sudo vim /etc/fstab
```

add the following in `~/.bashrc`
```bash
export EDITOR=vim
```
