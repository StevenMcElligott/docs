# GPU for Apps

## iGPU

Some Intel GPU's that use the `i915` driver, in `TrueNAS SCALE`,
do not show up on apps out of the box. To fix that we need to force probe the GPU driver.

> Make sure you have:
>
> - Checked the `Enable GPU support` in `Apps` -> `Settings` -> `Advanced Settings`
> - You have **NOT** added the GPU in `System Settings` -> `Advanced` -> `Isolated GPU Device(s)`

Enter the `Shell`

```shell
dmesg | grep i915
```

Example output:

```shell
root@truenas[~]# dmesg | grep i915
[    5.980845] i915 0000:00:10.0: Your graphics device 4692 is not properly supported by the driver in this
               kernel version. To force driver probe anyway, use i915.force_probe=4692
```

Grab the ID, for me it is `4692` and run this

```shell
midclt call system.advanced.update '{"kernel_extra_options": "i915.force_probe=4692"}'
```

Reboot your server. You should now be able to use it for apps.
