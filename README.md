# Device_Finder: Advanced Network Device Discovery Tool

This repository contains a comprehensive Bash-based network device discovery tool that uses ARP scanning to identify and categorize devices on your local network with intelligent device labeling and vendor identification.

## Main Script

- **devices**: The main Bash script that performs advanced network device discovery with automatic device categorization, vendor identification, and intelligent labeling.

## Key Features

### Network Discovery
- **Automatic Interface Detection**: Intelligently detects and uses the default network interface
- **Manual Interface Selection**: Option to specify network interface (-I flag)
- **Local Network Scanning**: Uses ARP scanning to discover all devices on the local network segment
- **IP and Gateway Auto-Detection**: Automatically identifies local IP, gateway, and network configuration

### Advanced Device Identification
- **Dual-Layer Vendor Lookup**: Primary vendor identification via arp-scan + fallback to comprehensive local MAC OUI database
- **Smart Device Categorization**:
  - **VM Detection**: Automatically identifies virtual machines (VirtualBox, VMware, Hyper-V, QEMU)
  - **Router Identification**: Detects routers via gateway IP matching and vendor analysis
  - **Local Machine Marking**: Automatically identifies and labels the scanning computer
- **Enhanced Output**: Formatted table with IP addresses, MAC addresses, and detailed vendor/device information

### Technical Capabilities
- **Comprehensive MAC Database**: Includes 6MB+ OUI database for vendor identification
- **Robust Error Handling**: Defensive programming with comprehensive error checking
- **Permission Management**: Intelligent sudo handling for network interface access
- **Portable Design**: Self-contained with relative file paths for easy deployment

## How It Works

The script performs the following operations:
1. **Interface Detection**: Automatically detects default network interface or uses specified interface
2. **Network Configuration**: Determines local IP, gateway IP, and MAC address
3. **ARP Scanning**: Performs comprehensive ARP scan of the local network segment
4. **Vendor Resolution**: Identifies device vendors using dual-layer lookup system
5. **Device Classification**: Categorizes devices as VMs, routers, or regular network devices
6. **Formatted Output**: Displays results in organized table format with enhanced labeling

## Installation

Clone the repository using the following command:

```bash
git clone https://github.com/YanivHaliwa/devices_finder.git
cd devices_finder
```

## Usage

### Basic Usage
```bash
# Scan using auto-detected interface
./devices

# Scan using specific interface
./devices -I wlan0

# Show help information
./devices -h
```

### Example Output
```
IP Address      MAC Address       Vendor/Notes
---------------  -----------------  -----------------------------
192.168.1.1     aa:bb:cc:dd:ee:ff  Huawei Technologies (Router)
192.168.1.100   11:22:33:44:55:66  Dell Inc. (This Computer)
192.168.1.150   08:00:27:ab:cd:ef  Oracle VirtualBox (VM)
```

**Important**: This tool is designed to run on the local machine and scan the local network only. It cannot be used to scan remote networks.

## Requirements

- **arp-scan**: Network scanning utility (requires sudo/root privileges)
- **iproute2**: Modern networking utilities (ip command)
- **Bash**: Version 4.0+ with associative arrays support
- **Root/Sudo Access**: Required for raw socket access during ARP scanning

### Installation of Dependencies
```bash
# Ubuntu/Debian
sudo apt-get install arp-scan iproute2

# CentOS/RHEL
sudo yum install arp-scan iproute2
```

## Author

Created by [Yaniv Haliwa](https://github.com/YanivHaliwa) for security testing and educational purposes.



