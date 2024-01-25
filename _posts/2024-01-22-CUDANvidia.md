---
layout: post
title: "Resintall CUDA and NVidia drivers"
---

I posted this since many people asked me how to reinstall CUDA and Nvidia drivers properly. This tutorials never failed me.

**Important Considerations**
> The CUDA version displayed by `nvidia-smi` doesn't necessarily reflect the CUDA version used in your PyTorch.
> 
> `nvidia-smi` and `nvcc` report different versions because they serve different purposes. `nvidia-smi` indicates the highest CUDA version supported/installed by your driver, while `nvcc -V` reveals the CUDA installation version your terminal points to. Generally, if `nvidia-smi` shows a CUDA version equal to or higher than that of `nvcc -V`, there's no need for concern. This discrepancy is typical, as newer drivers can support older CUDA toolkits.

**Checking CUDA Version**
```bash
nvcc -V
```

**Reinstalling Driver and CUDA to a Specific Version**
1. Switch to tty3: Press Ctrl + Alt + F3.
2. Unload `nvidia-drm`:
    - Switch to multi-user.target:
    ```bash
    sudo systemctl isolate multi-user.target
    ```
    - Check if nvidia-drm is in use:
    ```bash
    lsmod | grep nvidia.drm
    ```
    - Unload nvidia-drm:
    ```bash
    sudo modprobe -r nvidia-drm
    ```
    - Confirm nvidia-drm is unloaded:
    ```bash
    lsmod | grep nvidia.drm
    ```
3. Remove existing CUDA and NVIDIA Drivers:
    ```bash
    sudo apt --purge remove "cublas*" "cuda*" "nvidia*"
    sudo rm -rf /usr/local/cuda*
    sudo apt-get autoremove && sudo apt-get autoclean
    ```
4. Reboot and repeat step 2.
5. Install the NVIDIA Driver:
    - Download the driver from [NVIDIA's website](https://www.nvidia.com/Download/index.aspx?lang=en-us).
    - Log out from the GUI and switch to a terminal (Ctrl + Alt + F2 or F3).
    - Stop the current X-Server:
      ```bash
      sudo service lightdm stop
      ```
    - Enter runlevel 3:
      ```bash
      sudo init 3
      ```
    - Navigate to the directory containing the downloaded installer.
    - Make the installer executable:
      ```bash
      chmod +x ./your-nvidia-file.run
      ```
    - Run the installer:
      ```bash
      sudo ./your-nvidia-file.run
      ```
    - Reboot your system.
6. Download and Install a Specific CUDA Version:
    - Follow the installation procedure outlined here: [CUDA Installation Guide](https://developer.nvidia.com/cuda-11-8-0-download-archive).
    - It's recommended to use the network installer.
    - Remember to specify the version during installation:
      ```bash
      sudo apt-get -y install cuda-11.8
      ```
7. Set Environment Variables:
    - Adjust for your CUDA version and shell (e.g., bash, zsh). Check your shell with `echo $0`.
    - Add these lines to your shell configuration file:
      ```bash
      echo 'export PATH=/usr/local/cuda-11.8/bin:$PATH' >> ~/.bashrc
      echo 'export LD_LIBRARY_PATH=/usr/local/cuda-11.8/lib64:$LD_LIBRARY_PATH' >> ~/.bashrc
      ```
8. Reboot your system.
9. Install CuDNN (Optional):
    - Download from the [CuDNN Archive](https://developer.nvidia.com/rdp/cudnn-archive).

**References**
- [YouTube Tutorial](https://www.youtube.com/watch?v=5eJTzhGe2QE)
- [Unix StackExchange Discussion on Unloading nvidia-drm](https://unix.stackexchange.com/questions/440840/how-to-unload-kernel-module-nvidia-drm)
- [AskUbuntu on Installing NVIDIA .run Files](https://askubuntu.com/questions/149206/how-to-install-nvidia-run)