# Root Nexus 9 devices

## Prerequisites 

### Android Studio
It is required to have adb tool and usb drivers.


### Clear cache partion
It is required to have adb tool and usb drivers.

To clear the system cache you’ll need to power off your Nexus, then:
* Press and hold Volume Down and Power simultaneously until you see the boot screen.
* Use Volume Down to navigate to Recovery Mode.
* Press Power to confirm.
* Wait until you see the Android robot then hold down Power. Press and release Volume Up.
* Navigate with Volume Down to the Wipe Cache Partition option.
* Press Power to select.
* Use Volume Down to highlight the Yes option.
* Press Power to select.
* Press Power to reboot your Nexus.

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
```fastboot oem unlock```

Confirm operation on the device.
Restart device after that.

## Root device
Switch device to the fastboot mode.
```fastboot boot```

Get files for rooting and run next commands
```fastboot boot inject.img```
```fastboot flash boot patched.img```




