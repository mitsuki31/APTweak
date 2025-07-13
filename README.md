# APTweak

**APTweak** stands for *Aim for Performance Tweak* Module. This module is designed to boost your device's performance by tweaking system properties and settings using ADB Shell.

If you're familiar with apps like Brevent and Bugjaeger, you can install this module directly on your Android device.

> [!WARNING]  
> PLEASE USE THIS AT YOUR OWN RISK!  
> I am not responsible for any issues that may occur on your device after using this module.
> If your device becomes laggy, uninstall the module and reboot your device.
> This may be due to some configurations being incompatible with your device.
>
> After installing this module, your device may consume more significantly battery.
> Therefore, it is **NOT RECOMMENDED** to use this module for daily use.

## Usage

- Clone this repository (requires [Git](https://git-scm.com/))
> If you don't have [Git](https://git-scm.com/) installed, install it using your package manager (`apt` or `pkg` for Termux).  
> ```bash
> apt install git -y
> ```
  ```bash
  git clone https://github.com/mitsuki31/APTweak.git
  ```

- Alternative method, [download the repository directly](https://github.com/mitsuki31/APTweak/archive/refs/heads/master.zip) (don't forget to extract it).

- Install the module using ADB Shell
  ```bash
  adb shell sh path/to/APTweak/core --install
  ```

> [!NOTE]  
> If you're using application similar to Brevent that ADB-based, the command should be like this:
> ```bash
> sh path/to/APTweak/core --install
> ```

## Commands

```
Expected arguments:
    [-i|-u|-f]
    [--install|--uninstall|--fix]
    [install|uninstall|fix]
```

| Command | Description |
| ------- | ----------- |
| `-i` \| `--install` \| `install` | Use and install this module to system (modifying system properties and settings). |
| `-f` \| `--fix` \| `fix` | Perform fix for incompatible tweaks. If still can't resolve the problem, please uninstall using `-u` command. |
| `-u` \| `--uninstall` \| `uninstall` | Uninstall and remove this module tweaks from system (please reboot the device when done). |

> [!IMPORTANT]  
> After installing this module, **do not reboot your device!** Some configuration might be changed to their default value after reboot, but some of them might not. This can cause to unexpected system behavior for some devices (but as far from my experience, it totally fine and just make sure you reinstall it if the reboot was undesired action).
> 
> However, it is recommended to uninstall it first and then reboot to ensure the system configurations are fully reverted back to their defaults.

## FAQ

### I'm having a lagging issue after installed it

If you're having lag issue after installation, try to fix by using `--fix` command:

```bash
adb shell sh path/to/APTweak/core --fix
```

And if the issue still persist, consider to uninstall this module and reboot your device. It might be your device incompatible with the module.

To uninstall this module, you can do this by using `--uninstall` command:

```bash
adb shell sh path/to/APTweak/core --uninstall
```

### How to check if this module not compatible with my device?

I'm unsure to answer this. In every Android system -- which is also Linux-based system -- has their own readable logging system, but some devices may restrict (or the worst case, locked by the manufacture) even for read-only operation (or we can say, requires **root** permission).

To check your device compatibility can be check within the system log after installing the module, if the log giving some errors (along with the tweak command and the reason) it might be your device is incompatible with "that" tweak.

You can search in communities on how to get the system log from your device. But I'm not telling you to root your device.

## License

Copyright &copy; 2024 [Ryuu Mitsuki](https://github.com/mitsuki31). Licensed under the [MIT license](./LICENSE).
