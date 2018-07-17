
Debian
====================
This directory contains files used to package mnosd/mnos-qt
for Debian-based Linux systems. If you compile mnosd/mnos-qt yourself, there are some useful files here.

## mnos: URI support ##


mnos-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install mnos-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your mnos-qt binary to `/usr/bin`
and the `../../share/pixmaps/mnos128.png` to `/usr/share/pixmaps`

mnos-qt.protocol (KDE)

