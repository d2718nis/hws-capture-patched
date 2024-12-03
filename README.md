# ACASIS AC-4HDMI Patched Driver

This is a patched version of the Linux driver [available](https://www.acasis.com/pages/acasis-product-drivers) on the official ACASIS website. The patch removes the dependency on `libbsd`, which is [not present](https://sourceware.org/git/?p=glibc.git;a=commit;h=454a20c8756c9c1d55419153255fc7692b3d2199) in `glibc` versions earlier than 1.38. Additionally, it addresses the `videobuf2` API change [introduced](https://lkml.iu.edu/hypermail/linux/kernel/2312.0/06197.html) in Linux kernel 6.8 and later.

## Build and Install

1. Ensure that the `linux-headers` package for your current kernel is installed. The package name may vary depending on your Linux distribution
2. Run the installation script:
```shell
bash ./install.sh
```

## Verify Installation

Two scripts are included in the `play/` directory to verify if the capture card works. You may need additional dependencies to run them. Example:
```shell
bash ./play/play2.sh
```

## Uninstall

To remove the driver, execute the uninstall script:
```shell
bash ./uninstall.sh
```
