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

Instead of bundling large multimedia libraries, it uses the libraries already installed on the host system.

The following packages are required:

for Debian / Ubuntu / Linux Mint / Pop!_OS
sudo apt install mpv ffmpeg

for Arch Linux / EndeavourOS / Manjaro / CachyOS
sudo pacman -S mpv ffmpeg

for Fedora nobara
sudo dnf install mpv ffmpeg

for openSUSE
sudo zypper install mpv ffmpeg

for Alpine Linux
sudo apk add mpv ffmpeg

for Void Linux
sudo xbps-install -S mpv ffmpeg

for NixOS
nix-env -iA nixpkgs.mpv nixpkgs.ffmpeg

A working GPU driver with VA-API and/or VDPAU support is required for hardware video acceleration.

Make sure your system has the appropriate video drivers installed for your GPU:

Intel / AMD: VA-API support
NVIDIA: VDPAU support or compatible VA-API translation layer

This AppImage is designed for Linux distributions where multimedia libraries are already available in the system.
Building

After preparing a complete Mpc-qt.AppDir, the AppImage is created with:

ARCH=x86_64 ./appimagetool.AppImage ./Mpc-qt.AppDir MPC-Qt-VAAPI-x86_64.AppImage
License

Packaging files and custom scripts are provided as-is.

MPC-Qt and its dependencies remain under their respective licenses.

Design Goal

This AppImage was created with a focus on low disk space consumption.

Instead of including duplicated multimedia libraries inside the package, it uses the existing system libraries already installed on the host.

This keeps the AppImage extremely small (approximately 3 MB) while still providing MPC-Qt with VA-API hardware video acceleration when the required system components are available.
