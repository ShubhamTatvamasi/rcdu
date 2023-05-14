# rcdu

### Ubuntu Server 20.04.3 LTS

Node 1 | IPv4
---|---
Subnet | 192.168.6.0/24
Address | 192.168.6.10
Gateway | 192.168.6.1
Name Servers | 8.8.8.8, 8.8.4.4

Node 2 | IPv4
---|---
Subnet | 192.168.4.0/24
Address | 192.168.4.10
Gateway | 192.168.4.1
Name Servers | 8.8.8.8, 8.8.4.4

Node 3 | IPv4
---|---
Subnet | 192.168.5.0/24
Address | 192.168.5.10
Gateway | 192.168.5.1
Name Servers | 8.8.8.8, 8.8.4.4


User: rcdu \
Pass: rcduwash

Xen: root \
Pass: rcdurama

XO: xo \
Pass: rcdurama

---

List the `xo-ce` VM:
```bash
xe vm-list | grep -C 1 xo-ce
```

Start the VM:
```bash
xe vm-start uuid=29549638-fec4-2d3f-1d5f-fbac95d83900
```
