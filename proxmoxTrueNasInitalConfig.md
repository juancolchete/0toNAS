# IOMMU
[reference](https://pve.proxmox.com/wiki/PCI(e)_Passthrough)
## If using INTEL
```
nano /etc/default/grub
```
On GRUB_CMDLINE_LINUX_DEFAULT add following value
```
intel_iommu=on
```
## If using AMD
```
nano /etc/default/grub
```
On GRUB_CMDLINE_LINUX_DEFAULT add following value
```
iommu=pt
```
## edit /etc/modules
```
nano /etc/modules
```
Append these following values
```
vfio
vfio_iommu_type1
vfio_pci
```
## to apply changes
```
update-initramfs -u -k all
```
```
reboot
```
## Create your trueNAS VM and add your HDs
With your trueNAS proper created do

```
ls -la /dev/disk/by-id/
```
Copy IDs related to each HD and do, sample with 3 HD setup, note scsi is increase for each time you add a new HD starting at 1 because 0 is the system
```
qm set 100 -scsi1 /dev/disk/by-id/sataID
```
```
qm set 100 -scsi2 /dev/disk/by-id/sataID
```
```
qm set 100 -scsi3 /dev/disk/by-id/sataID
```