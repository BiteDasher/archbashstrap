# archbashstrap
Install/Bootstrap Arch Linux system without using pacman \
If you have ever wanted to install Arch Linux from another distribution, then you have come across the need to download `pacman`. Now there is no need for this, it is enough to have a basic set of utilities to install

### For termux users:
Execute the script with the NOCHROOT=1 option if you do not have `root access` or `chroot`

## How-to use:
`archbashstrap --help`

## How-to generate `packages` file:
You can grab `packages` file from this repository (only base group), or create your own. To create file `packages` with all the required packages for the `base` group, make sure you have installed the `pacman-contrib` package, run following command on Arch Linux machine and then copy `packages` to your local pc
```
pactree -l -u -s base > packages
```
If you installed this package from the `AUR`, you can take the `packages` file from the file `/usr/share/archbashstrap/packages`

At the moment, you can create a file only with the "base" group, using the `core` and `extra` repositories, since the rest are difficult to parse and provide a package selection dialog. Anyway, you can install other packages after bootstrap.

## Dependencies:
`sed` \
`coreutils` \
`curl` \
`tar` \
`zstd` (because of new packages compression method) \
`xz`
