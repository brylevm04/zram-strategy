# About
This repository offers you a possible strategy of using ZRAM.

The scripts in this repository will set up:
- A ZRAM device with disksize 200% of physical memory, with memlimit 85% of physical memory, and with ZSTD compression algorithm
- A ZRAM device with disksize 200% of physical memory, with memlimit 150% of physical memory, with ZSTD compression algorithm. Also an ext4 filesystem with no journalling will be created on this ZRAM device with /tmp mounted on this device.

# Installation
```
wget https://github.com/maksim-brylev/zram-strategy/archive/refs/heads/main.zip
unzip main.zip
cd zram-strategy-main
cp zram-config-on /usr/local/bin
chmod +x /usr/local/bin/zram-config-on
cp zram-config-off /usr/local/bin
chmod +x /usr/local/bin/zram-config-off
cp zram-config.service /etc/systemd/system
systemctl enable zram-config
```
