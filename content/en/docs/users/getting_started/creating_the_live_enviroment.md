+++
title = 'Creating the Live Environment'
date = 2024-09-10T23:43:21+08:00
description = "Creating a live environment to boot into and run the Serpent OS installer"
weight = 30
+++

## Creating a Bootable USB Drive

{{< alert color="warning" >}}
Creating a bootable USB drive will erase all data on the USB drive. Make sure to back up any important data before proceeding.
{{< /alert >}}

{{< alert color="secondary" >}}
Ensure the USB drive is properly ejected after flashing the ISO to avoid data corruption.
{{< /alert >}}

You'll need your USB drive and the ISO file downloaded from the [Serpent OS download page](https://download.serpentos.com).

### Linux

1. Insert your USB drive into an available USB port on your machine.
2. Open a terminal window and navigate to the directory where the ISO file is located.

```bash
cd ~/Downloads
```

3. Identify the device name of your USB drive by running the following command:

```bash
lsblk
```

Look for the device name of your USB drive, it will be something like `/dev/sdX` where `X` is a letter representing the device.

{{< alert color="warning" >}}
Do not confuse this with the partition name, which will be something like `/dev/sdX1`.
{{< /alert >}}

4. Now run the following command to write the ISO file to the USB drive:

{{< alert color="warning" >}}
Ensure you are using the correct device name for your USB drive to avoid data loss.
{{< /alert >}}

{{< alert color="primary" >}}
This may take some time to complete depending on the size of the ISO file and the speed of your USB drive.
{{< /alert >}}

```bash
sudo dd if=serpentos-<version>.iso of=/dev/sdX bs=4M conv=fsync oflag=direct status=progress
```

This command will write the ISO file to the USB drive and you'll see a progress indicator as it completes.

5. To ensure the write process has completed successfully, run the following command:

```bash
sudo sync
```

Once the command has run, you can safely remove the USB drive from your machine.

### Windows

1. Insert your USB drive into an available USB port on your machine.
2. Download and install [Rufus](https://rufus.ie/), a free and open-source tool for creating bootable USB drives.
3. **TODO**: Add steps for using Rufus to create a bootable USB drive.