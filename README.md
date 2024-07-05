# APTweak

**APTweak** stands for *Aim for Performance Tweak* Module. This module is designed to boost your device's performance by tweaking system properties and settings using ADB Shell.

If you're familiar with apps like Brevent and Bugjaeger, you can install this module directly on your Android device.

> [!WARNING]  
> PLEASE USE THIS AT YOUR OWN RISK!  
> I am not responsible for any issues that may occur on your device after using this module.
> If your device becomes laggy, uninstall the module and reboot your device.
> This may be due to some configurations being incompatible with your device.
>
> After installing this module, your device may consume significantly more battery.
> Therefore, it is **NOT RECOMMENDED** to use this module for daily use.

## Usage

- Clone this repository
- Install the module using ADB Shell
  ```bash
  adb shell sh APTweak/core install
  ```

---

If you're having lag issue after installation, try to fix by using this command:

```bash
adb shell sh APTweak/core fix
```

And if not worked, uninstall this module and reboot your device.

To uninstall this module, you can do this by using command:

```bash
adb shell sh APTweak/core uninstall
```

---

Developed by [Ryuu Mitsuki](https://github.com/mitsuki31).
