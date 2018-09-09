# Root Nexus 9 devices

## Prerequisites 

### Android Studio
It is required to have adb tool and usb drivers.

## Unlock OEM
Go to adb.exe location.
Run command in cmd:
```cd /d D:\android\sdk\platform-tools```

Run command in cmd to see attached devices:
```adb devices```

Should show something like this:
```
List of devices attached
HT51GWV00231    device
```

Run command in cmd:
```adb reboot bootloader```

After the device switches to the boot mode
Run command in cmd:
```fastboot devices```

Should show something like this:
```HT51GWV00231    fastboot```

Run command in cmd:
``fastboot oem unlock```

Confirm operation on the device.
Restart device after that.

## Root device
Switch device to the fastboot mode.
```fastboot boot```

Get files for rooting and run next commands
```fastboot boot inject.img```
```fastboot flash boot patched.img```




