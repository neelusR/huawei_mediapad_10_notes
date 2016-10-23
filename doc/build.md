# Create recovery from scratch

Prepare
-------
* Pull original boot.img from the device
* Download CyanogenMod sources

Create device directories
```
cd ~/android/system
make -j4 otatools

source build/envsetup.sh
export PATH=~/android/system/out/host/linux-x86/bin:$PATH
./build/tools/device/mkvendor.sh huawei hws10201l ~/Desktop/huawei/original/boot.img
```

Update manually this files (from similar device repositories):
* BoardConfig.mk
* recovery.fstab

Use the following command to set up your build environment:
```
> cd ~/android/system
> lunch cm_hws10201l-eng
```

Make recovery
```
> make recoveryimage
```
