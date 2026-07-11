MPC-Qt AppImage with VA-API (Linux)

This repository contains the AppDir structure and custom files used to build my Linux AppImage of MPC-Qt with VA-API hardware video acceleration.

About

This project is not the complete source code of MPC-Qt.

The original binaries were installed from Arch Linux using:

yay -S mpc-qt

or

paru -S mpc-qt

The actual MPC-Qt binaries and required libraries are obtained from a locally built installation and are not included in this repository.

The purpose of this repository is to track changes to the AppDir structure, launcher, icons, configuration files, and packaging layout.

Runtime Requirements

This AppImage is intentionally debloated and is approximately 3 MB in size.

Instead of bundling large libraries, it uses the libraries already installed on your Linux system.

For proper operation, your system should provide:

FFmpeg libraries and codecs.
GPU video drivers with VA-API and/or VDPAU support.
Standard system libraries required by MPC-Qt.

This AppImage is intended for Linux distributions where multimedia libraries are already installed.

Building

After preparing a complete Mpc-qt.AppDir, the AppImage is created with:

ARCH=x86_64 ./appimagetool.AppImage ./Mpc-qt.AppDir MPC-Qt-VAAPI-x86_64.AppImage
License

Packaging files and custom scripts are provided as-is.

MPC-Qt and its dependencies remain under their respective licenses.
