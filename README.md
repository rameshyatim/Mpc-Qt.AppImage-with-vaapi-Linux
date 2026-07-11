MPC-Qt AppImage with VA-API (Linux)

This repository contains the AppDir structure and custom files used to build my Linux AppImage of MPC-Qt with VA-API hardware video acceleration.

About

This project is not the complete source code of MPC-Qt.

The actual MPC-Qt binaries and required libraries are obtained from a locally built installation and are not included in this repository.

The purpose of this repository is to track changes to the AppDir structure, launcher, icons, configuration files, and packaging layout.

Building
THE ORIGINAL BINARIES WAS DOWNLOADED FROM:

yay -S mpc-qt || paru -S mpc-qt
After preparing a complete Mpc-qt.AppDir, the AppImage is created with:

ARCH=x86_64 ./appimagetool.AppImage ./Mpc-qt.AppDir Mpc-Qt-with-vaapi-x86_64.AppImage
Notes
Linux only.
Includes support for VA-API hardware acceleration.
This repository is intended as the packaging template rather than a complete build environment.
License

Packaging files and custom scripts are provided as-is.
MPC-Qt and its dependencies remain under their respective licenses.
