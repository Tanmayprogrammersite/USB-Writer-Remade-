# USB Writer (Remade!)

A lightweight, native USB-writing toolkit for Arch Linux, built with **C++20 and Qt6 Widgets**.

## Features

- Native graphical user interface.
- Removable-device detection using Linux system information.
- ISO image selection.
- Device capacity and status information.
- Windows ISO compatibility warnings — planned.
- Raw USB writing and progress reporting — under development.
- Legacy GRUB bootloader integration — planned for version 3.0.

## Requirements

- Arch Linux or a compatible Arch-based distribution.
- Git.
- CMake.
- GCC or another C++20-compatible compiler.
- Qt6 Base (Widgets).

## Fetch the Source Code

Clone the repository:
bash
git clone https://github.com/Tanmayprogrammersite/USB-Writer-Remade-.git
cd usb-writer-remade


## Install Build Dependencies

On Arch Linux, run:

```bash
sudo pacman -S --needed base-devel cmake qt6-base git
```

## Build from Source

Configure the project:

```bash
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
```

Compile the application:

```bash
cmake --build build -j2
```

Run the application:

```bash
./build/usb-writer-remade
```

## Project Structure

```text
usb-writer-remade/
├── CMakeLists.txt
├── LICENSE
├── README.md
├── src/
│   ├── app/
│   │   └── main.cpp
│   ├── devices/
│   │   ├── DeviceInfo.hpp
│   │   ├── DeviceManager.hpp
│   │   └── DeviceManager.cpp
│   ├── gui/
│   │   ├── MainWindow.hpp
│   │   └── MainWindow.cpp
│   ├── writer.hpp
│   └── writer.cpp
└── packaging/
    └── usb-writer-remade.desktop
```

## Safety Notice

Writing an ISO directly to a USB drive can permanently erase all data on the selected device. Always verify the target device and back up important files before proceeding.

**USB Writer (Remade!) is still under development.** Features marked as planned or under development are not yet complete. Do not assume that the current build can create a bootable
