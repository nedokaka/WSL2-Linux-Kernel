# Introduction

The [WSL2-Linux-Kernel][wsl2-kernel] repo contains the kernel gore source code and
configuration files for the [WSL2][about-wsl2] kernel.

# Reporting Bugs

no.

# Build Instructions

Instructions for building an x86_64 WSL2 kernel with an Ubuntu distribution are
as follows:

1. Install the build dependencies:  
   `$ sudo apt install build-essential flex bison dwarves libssl-dev libelf-dev bc libncurses-dev`
2. Build the kernel using the WSL2 kernel configuration:  
   `$ make KCONFIG_CONFIG=Microsoft/config-wsl`

# Install Instructions

Instol [wsl2 update][wsl2-updat]

Shutdown wsl
```
wsl --shutdown
```

~~Push arch/x86/boot/bzImage to C:\Windows\System32\lxss\tools with file name kernel~~

copy arch/x86/boot/bzImage anywhere you want (except wsl) and create a .wslconfig in %UserProfile% (Windows user home folder)
and put it into a file
```
[wsl2]
kernel=C:\\path\\to\\kernel
```
the path should be spelled with \\\

Run your favorite gore wsl distro

[wsl2-kernel]:  https://github.com/microsoft/WSL2-Linux-Kernel
[about-wsl2]:   https://docs.microsoft.com/en-us/windows/wsl/about#what-is-wsl-2
[wsl-issue]:    https://github.com/microsoft/WSL/issues/new/choose
[normal-bug]:   https://www.kernel.org/doc/html/latest/admin-guide/bug-hunting.html#reporting-the-bug
[security-bug]: https://www.kernel.org/doc/html/latest/admin-guide/security-bugs.html
[submit-patch]: https://www.kernel.org/doc/html/latest/process/submitting-patches.html
[wsl2-updat]: https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
