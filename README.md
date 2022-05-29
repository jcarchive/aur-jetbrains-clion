# AUR package for Jetbrains - Clion
This repo contains an Arch User Repository package for Clion following the next standard for the installation:

1. App files directory: `/usr/share/jetbrains-clion`
2. Executable `clion` directory: `/usr/bin/clion`

* The executable in `/usr/bin` is installed as symbolic link to the `clion` bin inside the app files.

## * Notes

This package may differ from the "official" in the AUR repository in the directories used for the installation and the steps used. The purpose of this package and others 
ones in this account is for install all the programs that I used following certain standard (i.e. using `/usr/share/{pkgname}` for app files and `/usr/bin/{execname}`
for executable) and in some cases clean the installation steps from some bloat.
