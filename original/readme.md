Backup your partitions
----------------------------------------
Your device should be already rooted.

Connect to the device
```
> adb shell
> su
```
Get list of the partitions
```
# ls -al /dev/block/platform/*/by-name
```
Get dump of 'boot' and 'recovery' partitions
```
# dd if=/dev/block/mmcblk0p11 of=/storage/sdcard0/boot.img bs=4096
# dd if=/dev/block/mmcblk0p10 of=/storage/sdcard0/recovery.img bs=4096
# dd if=/dev/block/mmcblk0p9 of=/storage/sdcard0/recovery2.img bs=4096
```
Disconnect from the device
```
exit
exit
```
Download images to PC
```
adb pull /storage/sdcard0/boot.img
adb pull /storage/sdcard0/recovery.img
adb pull /storage/sdcard0/recovery2.img
```
