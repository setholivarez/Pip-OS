
# Pip OS ![arch](https://img.shields.io/badge/Architecture-ARMv7--A-blue) ![ver](https://img.shields.io/badge/Version-0.0.1.0-green)

This is the repository for the Operating System used in Pip-Boy products.

## Supported hardware

The kernel is compatible with the following Broadcom boards, as they share the same underlying architecture :

- BCM2835
- BCM2836
- BCM2837

The model BCM2711 should be supported in the future.

## Building from sources

### Requirements 

- An ARM toolchain compatible to your machine ([GNU ARM](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads))
- An emulator to test the OS (we use [QEMU](https://www.qemu.org/download/))

```sh
cd build 
export BCM=2837 # Build for BCM2837 board

make clean
make
make run # Requires QEMU installed on your machine
```

## References

Peripheral manual for BCM2835 ARM chip (useful to get Memory Mapped IO addresses):
[BCM2835 ARM Peripherals](https://www.raspberrypi.org/app/uploads/2012/02/BCM2835-ARM-Peripherals.pdf)