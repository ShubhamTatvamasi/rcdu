# clone

clone VM:
```bash
virt-clone \
  --original Ubuntu_20_04_3_Source_11 \
  --name Blockchain_Besu_21 \
  --file /var/lib/libvirt/images/Blockchain_Besu_21.qcow2
```

update address IP:
```bash
sudo vim /etc/netplan/00-installer-config.yaml
```

apply network changes:
```bash
sudo netplan apply
```
