# Paqet-Tunnel-Manager
Management script for paqet: raw socket KCP-based tunnel for firewall/DPI bypass. Supports kharej server and Iran client configurations.

## Quick Start

# Install prerequisites (Run on both servers (as root))
Run the script to install the prerequisites
Press option 0 and then option 1 to install the prerequisites
```bash
bash <(curl -fsSL https://raw.githubusercontent.com/behzadea12/Paqet-Tunnel-Manager/main/paqet-manager.sh)
```

##Installation Steps
# Step 1: Setup Server (Kharej – VPN Server)
Run the script:
```bash
bash <(curl -fsSL https://raw.githubusercontent.com/behzadea12/Paqet-Tunnel-Manager/main/paqet-manager.sh)
````
### Configuration Steps
1. **Select option 2** (Kharej)
2. **Enter a custom name** for the tunnel between the two servers
3. **Press Enter** *(automatic)*
4. **Press Enter** *(automatic)*
5. **Press Enter** *(automatic)*
6. **Specify the port** used between the two servers (e.g. `555`)
7. **Save the generated secret key**, then press **`Y`** to continue
8. **Select option 1**
9. **Select option 2**
10. **Enter V2Ray / OpenVPN port(s)**
    Single: `555` — Multiple: `555,666,777`

# Step 2: Setup Server (Iran – Client(Entry Point))
### Configuration Steps
1. **Select option 3** (Iran)
2. **Enter the Kharej server IP**
3. **Specify the port** used between the two servers (e.g. `555`)
4. **Enter the secret key** generated on the server(Kharej)
5. **Enter a custom name** for the tunnel between the two servers
6. **Press Enter** *(automatic)*
7. **Press Enter** *(automatic)*
8. **Press Enter** *(automatic)*
9. **Select option 1**
10. **Select option 2**
11. **Enter V2Ray / OpenVPN port(s)**
    Single: `555` — Multiple: `555,666,777`

## Troubleshooting: Paqet Installation Issues

If Paqet fails to install automatically during configuration  
(i.e. you see "Failed to install Paqet" or the script gets stuck when adding a new config in **Server/Kharej** or **Client/Iran** mode), follow these simple steps:

1. **Manually download the Paqet binary**  

   Visit the official releases page:  
   https://github.com/hanselime/paqet/releases

   - Choose the **latest release** (currently `v1.0.0-alpha.13` or newer — always pick the most recent one).  
   - Download the file that matches your server architecture:

     - `paqet-linux-amd64-*.tar.gz` → for most 64-bit servers (x86_64 / amd64)  
     - `paqet-linux-arm64-*.tar.gz` → for ARM-based servers (aarch64 / arm64)

2. **Place the downloaded file in this exact folder**  

   Move or copy the `.tar.gz` file to:

   ```bash
   /root/paqet/
   ```
   If the folder doesn't exist, create it first:
   ```bash
    mkdir -p /root/paqet
   ```

3. Run the manager script again
   The script will automatically detect the file inside /root/paqet/, use it instead of trying to download again, extract it, and complete the installation.
   ```bash
   bash <(curl -fsSL https://raw.githubusercontent.com/behzadea12/Paqet-Tunnel-Manager/main/paqet-manager.sh)
   ```


## ⚠️ If There Is Any Problem...

**Send a message to my Telegram ID right away:**

**@behzad_developer**

I'm usually online and will help you as soon as possible!
