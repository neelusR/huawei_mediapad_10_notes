# Update busybox

```
> wget https://www.busybox.net/downloads/binaries/1.21.1/busybox-armv7l
> adb push busybox-armv7l /data/local/tmp/
> adb shell
> su
# mount -o rw,remount /system
# mv /system/bin/busybox /system/bin/busybox.bak
# cat /data/local/tmp/busybox-armv7l > /system/bin/busybox
# chown 0:2000 /system/bin/busybox
# chmod 755 /system/bin/busybox
# mount -o ro,remount /system
# rm /data/local/tmp/busybox-armv7l
```
