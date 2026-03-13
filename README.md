# linux-lvm-filesystem-expansion
Linux project demonstrating online filesystem expansion using LVM without downtime.
# Online Filesystem Expansion using LVM

## Objective
To extend filesystem storage without downtime using LVM.

## Commands Used

### Check Disk Information
```bash
lsblk
df -h
pvs
vgs
lvs
pvcreate /dev/sdb
vgextend vg_data /dev/sdb
lvextend -L +10G /dev/vg_data/lv_data
xfs_growfs /data
df -h
lsblk
