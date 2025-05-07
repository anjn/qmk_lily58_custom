## Changes from original

- Disabled tri layers so that layer 3 can be activated using a signle key.

## How to compile and flash

```
# Install and setup QMK
python3 -m pip install --user qmk
qmk setup
sudo cp ~/qmk_firmware/util/udev/50-qmk.rules /etc/udev/rules.d/
mkdir ~/qmk_userspace

# Clone this repository
cd ~/qmk_firmware/keyboards
git clone https://github.com/anjn/qmk_lily58_custom.git lily58_custom

# Compile and flash
qmk compile -kb lily58_custom/rev1 -km default
qmk flash -kb lily58_custom/rev1 -km default
```
