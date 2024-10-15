# Macbook-Pro-Nvidia-GT650M-Ubuntu-22.04
To install the NVIDIA driver and necessary utilities on Ubuntu 22.04 for your MacBook Pro (2011), follow these steps. I'll provide you with the commands to ensure everything you need is included:

Link in German: 
https://rootserver0303.wordpress.com/2024/10/13/macbook-nvidia-gt650m-mit-ubuntu-22-04-jammy/


To install the NVIDIA driver and necessary utilities on Ubuntu 22.04 for your MacBook Pro (2011), follow these steps. I'll provide you with the commands to ensure everything you need is included:

1. **Update your package list**:
   ```bash
   sudo apt update
   ```

2. **Install the required dependencies**:
   ```bash
   sudo apt install build-essential dkms
   ```

3. **Add the graphics drivers PPA** (if you haven't already):
   ```bash
   sudo add-apt-repository ppa:graphics-drivers/ppa
   sudo apt update
   ```

4. **Install the NVIDIA driver (version 470)**:
   ```bash
   sudo apt install nvidia-driver-470
   ```

5. **Install NVIDIA utilities**:
   ```bash
   sudo apt install nvidia-utils-470
   ```

6. **Optional: Install the NVIDIA settings application**:
   ```bash
   sudo apt install nvidia-settings
   ```

7. **Reboot your system**:
   ```bash
   sudo reboot
   ```

### Additional Configuration (if needed)
After rebooting, you can check if the driver is working properly by running:
```bash
nvidia-smi
```
This command should display information about your NVIDIA GPU.

### Troubleshooting
If you encounter any issues:
- Ensure that Secure Boot is disabled in the BIOS settings, as it can prevent the NVIDIA driver from loading.
- If you have installed previous versions of NVIDIA drivers, consider removing them first:
  ```bash
  sudo apt remove --purge '^nvidia-.*'
  ```

Following these steps should set up the NVIDIA driver correctly on your Ubuntu 22.04 installation. Let me know if you need further assistance!
