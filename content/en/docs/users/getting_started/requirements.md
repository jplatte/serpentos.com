+++
title = 'Requirements'
date = 2024-09-10T23:00:44+08:00
description = "Requirements for Serpent OS"
weight = 10
+++

## Minimum System Requirements

{{< alert color="info" >}}
BOIS/CSM mode is not supported. Please ensure that your system is set to UEFI mode.
{{< /alert >}}

- **Architecture:** x86_64
- **Firmware:** UEFI (CSM Support must be disabled)
- **Processor (CPU):** Quad-core processor with a minimum clock speed of 2GHz
- **System Memory (RAM):** 4GB or more
- **Storage:** Minimum of 40GB available space

## Installer Requirements

To successfully create a bootable USB drive for installing Serpent OS, the following requirements must be met:

- **Network:** An active internet connection is required for installation
- **USB Flash Drive:** Ensure you have a USB flash drive with at least 4GB of free space.

  {{< alert color="warning" >}}
  The process of flashing the ISO will completely erase all existing data on the drive.
  {{< /alert >}}

  {{< alert color="info" >}}
  It is advisable to use a high-quality USB drive to avoid potential issues during the installation process.
  {{< /alert >}}

- **Image Flashing Software:** Utilize one of the following recommended tools to flash the Serpent OS ISO image onto the USB drive:
  - **dd:** A command-line utility available on most Linux distributions for creating bootable USB drives.
  - **Fedora Media Writer:** A reliable and user-friendly tool for creating bootable USB drives.
  - **Rufus:** A widely-used utility that provides advanced options for creating bootable USB drives.
  - **Balena Etcher:** A simple and user-friendly tool for creating bootable USB drives.
  - **Ventoy:** An open-source tool that allows you to create a bootable USB drive for multiple ISO files.

- **Additional Hardware:** A physical keyboard, mouse, and monitor (or screen) are required to interact with the installation process. Ensure that all these peripherals are properly connected to the system before starting the installation.