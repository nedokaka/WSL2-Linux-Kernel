# Introduction

The [WSL2-Linux-Kernel][wsl2-kernel] repo contains the kernel gore source code and
configuration files for the [WSL2][about-wsl2] kernel.

# Reporting Bugs

If you discover an issue relating to WSL or the WSL2 kernel, please report it on
the [WSL GitHub project][wsl-issue]. It is not possible to report issues on the
[WSL2-Linux-Kernel][wsl2-kernel] project.

If you're able to determine that the bug is present in the upstream Linux
kernel, you may want to work directly with the upstream developers. Please note
that there are separate processes for reporting a [normal bug][normal-bug] and
a [security bug][security-bug].

# Feature Requests

Is there a missing feature that you'd like to see? Please request it on the
[WSL GitHub project][wsl-issue].

If you're able and interested in contributing kernel code for your feature
request, we encourage you to [submit the change upstream][submit-patch].

# Build Instructions

Instructions for building an x86_64 WSL2 kernel with an Ubuntu distribution are
as follows:

1. Install the build dependencies:  
   `$ sudo apt install build-essential flex bison dwarves libssl-dev libelf-dev`
2. Build the kernel using the WSL2 kernel configuration:  
   `$ make KCONFIG_CONFIG=Microsoft/config-wsl`

# Install Instructions

Instol [wsl2 update][wsl2-updat]

Shutdown wsl
```
wsl --shutdown
```

Push arch/x86/boot/bzImage to C:\Windows\System32\lxss\tools with file name kernel

Run your favorite gore wsl distro

[wsl2-kernel]:  https://github.com/microsoft/WSL2-Linux-Kernel
[about-wsl2]:   https://docs.microsoft.com/en-us/windows/wsl/about#what-is-wsl-2
[wsl-issue]:    https://github.com/microsoft/WSL/issues/new/choose
[normal-bug]:   https://www.kernel.org/doc/html/latest/admin-guide/bug-hunting.html#reporting-the-bug
[security-bug]: https://www.kernel.org/doc/html/latest/admin-guide/security-bugs.html
[submit-patch]: https://www.kernel.org/doc/html/latest/process/submitting-patches.html
[wsl2-updat]: https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
