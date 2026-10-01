# Huawei EchoLife HG8145v5 OpenWrt — recovery resolution

**Status:** REVERSE-ENGINEERING HISTORY / PROCEDURE NOT RECOVERED

A prior HG8145v5 unit had reportedly been successfully flashed with OpenWrt using a LAN file-send/boot-time method remembered as similar to TFTP. That successful unit later became unavailable after flood/mud damage, and the original image/procedure had not been documented.

Later recovery work established only partial clues:

- spare HG8145v5 and HG8145v5V2 hardware existed for comparison;
- UART/bin-dump recovery was considered;
- generic Huawei Ethernet/TFTP boot clues were found;
- stock WAP/CLI access and some bridge/VLAN behavior were explored;
- no verified OpenWrt image, exact boot command sequence, partition map or reproducible flashing procedure was recovered.

## Resolution

Do not publish a guessed firmware image or flashing recipe.

A future recovery should first obtain and preserve full flash/UART evidence from a sacrificial matching unit, identify SoC/flash/partition layout, verify bootloader recovery paths, and only then attempt a reproducible OpenWrt port with rollback/recovery documentation.
