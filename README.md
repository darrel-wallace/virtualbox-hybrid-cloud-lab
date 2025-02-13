# VirtualBox Hybrid Cloud Lab

This document outlines the steps to create a hybrid cloud environment.

## Part 1: VirtualBox Network Configuration

This part focuses on setting up the necessary networks within VirtualBox.

1. **Open VirtualBox Manager:**
    - Open the VirtualBox application.

2. **Create NAT Network:**
    - Navigate to the NEtwork Manager: Go to 'Tools' -> 'Network'.
    - Select the "NAT Networks" tab.

    ![Initial Network Manager Window](screenshots/part1-network-manager-initial.png)

    - Click the "Create" button to add a new NAT network.
    - Rename the newly created network to 'cloud-nat-network'.
    - Set the IPv4 Prefix to '172.16.0.0/24'.
    - Ensure that the "Enable DHCP" checkbox is checked.

    ![NAT Network Created](screenshots/part1-nat-network-config.png)

    - Click "Apply"

    **Note:** Internal networks will be defined implicitly during the VM configuration process.

## Part 2: Create Virtual Machines

This part involves creating the eight virtual machine sneeded for the lab environment.

1. **Create VMs:**
    - For each VM, click 'Machine' -> 'New' button in VirtualBox Manager.

    ![Create VM Dialog - Initial](screenshots/part2-create-vm-cli1-initial.png)

    - Configure the VM settings:
        - Name and Operating System
            - **Name:** 'cli1'
            - **Folder:** (Choose where to store the VMs)
            - **ISO Image:** (Leave blank)
            - **Type:** 'Microsoft Windows'
            - **Version:** 'Windows 11 (64-bit)'
            - **Skip Unattended Installation:** Ensure this is *unchecked*

        ![Name and Operating System](screenshots/part2-create-vm-cli1-name-os.png)

        - Hardware
            - **Base Memory:** '4096 MB'
            - **Processors:** (Leave at default)

        ![Hardware Settings](screenshots/part2-create-vm-cli1-hardware.png)

        - Hard Disk
            - **File Size:** '64 GB'

        ![Hard Disk Settings](screenshots/part2-create-vm-cli1-harddisk.png)

        - Click 'Finish' to create the virtual machine.

        ![New VM added to VirtualBox Manager](screenshots/part2-vm-cli1-created.png)