# 🖥️ Windows 10 in Docker Container

![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![KVM](https://img.shields.io/badge/KVM-FF6600?style=for-the-badge&logo=linux&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-10-0078D6?style=for-the-badge&logo=windows&logoColor=white)

A Docker container solution for running Windows 10 with KVM acceleration, providing remote access via VNC and RDP.

## 🚀 Getting Started

### Prerequisites
- Docker installed
- KVM enabled system
- Administrative privileges

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/hopingboyz/windows10vm.git
Navigate to project directory:

bash
cd windows10vm
Build the Docker image:

bash
docker build -t windows10-vm .
Run the Windows 10 VM:

bash
docker run -it --rm \
  --device /dev/kvm \
  -p 6080:6080 \    # VNC access
  -p 3389:3389 \    # RDP access
  -v windows_data:/data \
  -v windows_iso:/iso \
  windows10-vm
🔗 Access Methods
VNC: Connect via http://localhost:6080

RDP: Use any RDP client to connect to localhost:3389

📂 Volume Mounts
Volume	Purpose
windows_data	Persistent VM storage
windows_iso	ISO files directory
⚙️ System Requirements
Linux host with KVM support

Minimum 4GB RAM (8GB recommended)

20GB free disk space
