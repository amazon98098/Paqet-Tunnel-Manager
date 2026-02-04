# Paqet-Tunnel-Manager
Management script for paqet: raw socket KCP-based tunnel for firewall/DPI bypass. Supports kharej server and Iran client configurations.

## Quick Start

# Install prerequisites
```bash
sudo apt update
sudo apt remove golang-go
sudo add-apt-repository ppa:longsleep/golang-backports -y
sudo apt update
sudo apt install golang-1.25-go
sudo ln -sf /usr/lib/go-1.25/bin/go /usr/bin/go
go version
```

# Run on both servers (as root)
```bash
bash <(curl -fsSL https://raw.githubusercontent.com/behzadea12/Paqet-Tunnel-Manager/main/paqet-manager.sh)
```
