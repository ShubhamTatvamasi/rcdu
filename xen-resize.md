# xen resize

Check if your file system has been changed to GPT:
```bash
fdisk -l /dev/sda
```

Fix GPT:
```bash
sgdisk -e /dev/sda
```

Now resize /dev/sda3 partition:
```bash
fdisk /dev/sda
```

Change partition sector:
```
p -> see old values
d -> delete 3 number drive
n -> create new drive with 3 number with same start sector
t -> change drive 3 type to Linux LVM it was 31 number for me.
p -> see new values
w -> save changes
```
> `reboot` after this

---

check the volumes:
```bash
pvscan
```

Resize phisical volume:
```bash
pvresize /dev/sda3
```

Extend Logical volume:
```bash
lvextend --resizefs -l +100%FREE /dev/mapper/XSLocalEXT--c43bd674--eda4--5ab4--498f--75978ad83704-c43bd674--eda4--5ab4--498f--75978ad83704
```
> `reboot` after this
