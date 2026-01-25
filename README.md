# Device_Finder: Advanced Network Device Discovery Tool

[![zread](https://img.shields.io/badge/Ask_Zread-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQuOTYxNTYgMS42MDAxSDIuMjQxNTZDMS44ODgxIDEuNjAwMSAxLjYwMTU2IDEuODg2NjQgMS42MDE1NiAyLjI0MDFWNC45NjAxQzEuNjAxNTYgNS4zMTM1NiAxLjg4ODEgNS42MDAxIDIuMjQxNTYgNS42MDAxSDQuOTYxNTZDNS4zMTUwMiA1LjYwMDEgNS42MDE1NiA1LjMxMzU2IDUuNjAxNTYgNC45NjAxVjIuMjQwMUM1LjYwMTU2IDEuODg2NjQgNS4zMTUwMiAxLjYwMDEgNC45NjE1NiAxLjYwMDFaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00Ljk2MTU2IDEwLjM5OTlIMi4yNDE1NkMxLjg4ODEgMTAuMzk5OSAxLjYwMTU2IDEwLjY4NjQgMS42MDE1NiAxMS4wMzk5VjEzLjc1OTlDMS42MDE1NiAxNC4xMTM0IDEuODg4MSAxNC4zOTk5IDIuMjQxNTYgMTQuMzk5OUg0Ljk2MTU2QzUuMzE1MDIgMTQuMzk5OSA1LjYwMTU2IDE0LjExMzQgNS42MDE1NiAxMy43NTk5VjExLjAzOTlDNS42MDE1NiAxMC42ODY0IDUuMzE1MDIgMTAuMzk5OSA0Ljk2MTU2IDEwLjM5OTlaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik0xMy43NTg0IDEuNjAwMUgxMS4wMzg0QzEwLjY4NSAxLjYwMDEgMTAuMzk4NCAxLjg4NjY0IDEwLjM5ODQgMi4yNDAxVjQuOTYwMUMxMC4zOTg0IDUuMzEzNTYgMTAuNjg1IDUuNjAwMSAxMS4wMzg0IDUuNjAwMUgxMy43NTg0QzE0LjExMTkgNS42MDAxIDE0LjM5ODQgNS4zMTM1NiAxNC4zOTg0IDQuOTYwMVYyLjI0MDFDMTQuMzk4NCAxLjg4NjY0IDE0LjExMTkgMS42MDAxIDEzLjc1ODQgMS42MDAxWiIgZmlsbD0iI2ZmZiIvPgo8cGF0aCBkPSJNNCAxMkwxMiA0TDQgMTJaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00IDEyTDEyIDQiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIxLjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K&logoColor=ffffff)](https://zread.ai/YanivHaliwa/devices_finder)
[![deepwiki](https://img.shields.io/badge/Ask_DeepWiki-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2IiByeD0iMiIgZmlsbD0iI2ZmZiIvPgo8dGV4dCB4PSI4IiB5PSIxMSIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZm9udC1mYW1pbHk9IkFyaWFsLCBIZWx2ZXRpY2EsIHNhbnMtc2VyaWYiIGZvbnQtc2l6ZT0iNyIgZm9udC13ZWlnaHQ9IjcwMCIgZmlsbD0iIzAwMCI+RFc8L3RleHQ+Cjwvc3ZnPgo%3D&logoColor=ffffff)](https://deepwiki.com/YanivHaliwa/devices_finder)

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



