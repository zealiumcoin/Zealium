
Debian
====================
This directory contains files used to package zealiumd/zealium-qt
for Debian-based Linux systems. If you compile zealiumd/zealium-qt yourself, there are some useful files here.

## zealium: URI support ##


zealium-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install zealium-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your zealiumqt binary to `/usr/bin`
and the `../../share/pixmaps/zealium128.png` to `/usr/share/pixmaps`

zealium-qt.protocol (KDE)

