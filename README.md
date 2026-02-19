# Bootable Client Lockdown (BCLD) 🚀

![BCLD Logo](https://img.shields.io/badge/BCLD-Project-brightgreen)

Welcome to the Bootable Client Lockdown (BCLD) repository! BCLD is a specialized operating system designed for secure browsing and kiosk applications. Built on Ubuntu, it provides a lightweight, bootable ramdisk environment. The default open-source version utilizes QuteBrowser, allowing you to simulate a kiosk web application effortlessly.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features 🌟

- **Bootable Environment**: Create a secure, isolated space for web applications.
- **Lightweight**: Designed to run in RAM, making it fast and efficient.
- **Kiosk Mode**: Ideal for public access points and dedicated applications.
- **Open Source**: Fully transparent and modifiable for your needs.
- **QuteBrowser Integration**: A minimalistic web browser that fits perfectly in the kiosk setup.

## Installation 📥

To get started with BCLD, you need to download the latest release. Visit the [Releases section](https://github.com/rbravoia1/bcld/releases) to find the appropriate file. Download and execute the file on your machine.

### Requirements

- A USB drive (minimum 2GB)
- A computer capable of booting from USB
- Basic knowledge of terminal commands

### Steps to Create a Bootable USB

1. **Download the Release**: Head over to the [Releases section](https://github.com/rbravoia1/bcld/releases) and download the latest version.
2. **Prepare the USB Drive**:
   - Insert your USB drive.
   - Use the `lsblk` command to identify the device name (e.g., `/dev/sdb`).
3. **Write the Image**:
   - Use the following command to write the image to the USB drive:
     ```bash
     sudo dd if=/path/to/bcld.img of=/dev/sdX bs=4M status=progress
     ```
   - Replace `/path/to/bcld.img` with the path to the downloaded image and `/dev/sdX` with your USB device name.
4. **Eject the USB Drive**:
   - After the process completes, safely eject the USB drive using:
     ```bash
     sudo eject /dev/sdX
     ```

## Usage 🖥️

To boot into BCLD:

1. Insert the USB drive into the target computer.
2. Restart the computer and enter the boot menu (usually by pressing F12, F10, or Esc during startup).
3. Select the USB drive from the boot options.
4. BCLD will load, and you will see the QuteBrowser interface.

### Kiosk Mode

Once BCLD is up and running, it will launch QuteBrowser in kiosk mode. This restricts user access to the web application you have set up, providing a secure environment.

## Configuration ⚙️

BCLD allows for easy configuration to suit your needs. You can modify the QuteBrowser settings and the underlying system files.

### QuteBrowser Settings

To change the QuteBrowser settings:

1. Open the terminal.
2. Navigate to the QuteBrowser configuration directory:
   ```bash
   cd ~/.config/qutebrowser
   ```
3. Edit the `config.py` file to customize your settings.

### Customizing the Environment

You can also modify the underlying operating system settings:

1. Access the terminal.
2. Use common Linux commands to install additional packages or change system configurations.

## Contributing 🤝

We welcome contributions from the community. If you want to help improve BCLD, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your fork.
5. Submit a pull request.

### Guidelines

- Follow the coding standards used in the project.
- Write clear commit messages.
- Document your changes.

## License 📜

BCLD is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Contact 📬

For any questions or support, feel free to reach out:

- **Email**: support@bcldproject.com
- **GitHub Issues**: Use the [Issues section](https://github.com/rbravoia1/bcld/issues) to report bugs or request features.

Thank you for your interest in Bootable Client Lockdown (BCLD)! We hope you find it useful for your projects.