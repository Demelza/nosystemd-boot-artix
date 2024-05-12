# nosystemd-boot-artix
systemd-boot for Artix Linux

You need to use --skippgpcheck with makepkg or add the systemd PGP keys to build this. This only packages the following files:

- /usr/bin/bootctl
- /usr/bin/kernel-install
- /usr/lib/libsystemd-shared-255.6-1.so
- /usr/lib/systemd/boot/efi/linuxx64.efi.stub
- /usr/lib/systemd/boot/efi/linuxx64.elf.stub
- /usr/lib/systemd/boot/efi/systemd-bootx64.efi
