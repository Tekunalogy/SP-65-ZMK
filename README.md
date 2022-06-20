# "Southpaw-65" Nice!Nano Firmware
These are the steps to build the firmware for yourself, if you want to make changes.

First you need to complete the setup mentioned [here](https://zmk.dev/docs/development/setup).

Anytime you want to build the software from a new terminal instance, `cd` into the main `zmk/` directory and run the following:
```bash
source zephyr/zephyr-env.sh
```

Next, the command to build the firmware is:
```bash
west build -p -b nice_nano -- -DSHIELD=sp6
```

After that, the `zmk.uf2` file will be available at the following path:
```
ZMK/app/build/zephyr/zmk.uf2
```

# Troubleshooting
## Why isn't the name of the device changing when I build the firmware?
To fix this, you can first try checking the following file:
```
ZMK/app/build/zephyr/.config
```

If the file is showing the incorrect device name, try deleting the file and rebuilding.

If the file is showing the correct device name, then try deleting the following folder, and rebuilding:
```
ZMK/app/build/
```
If that doesn't work, you may need to contact [ZMK](https://zmk.dev) for support or ask the community discord.