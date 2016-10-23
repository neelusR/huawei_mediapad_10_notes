If device not shown in fastboot mode

```
> lsusb | grep Huawei
> sudo nano /etc/udev/rules.d/70-android.rules
...
> sudo service udev restart
```

Also you can try use VendorID param =)
```
> fastboot -i 0x12d1 devices
```
