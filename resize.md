# resize

become root
```bash
sudo su
```

check disk partition table:
```bash
cfdisk
```

start fdisk:
```bash
fdisk /dev/sda
```
```bash
p # print partition table
d # delete partitions 2 and 3
n # add a new partition
# check the start sector and end sector
w # write partition table
```

update size:
```bash
resize2fs /dev/mapper/mpatha-part2
```
