# Fedora_Setup
Fedaora on MSI Laptop setup

Links: 
- https://www.youtube.com/watch?v=m8xj2Py8KPc&t=605s
- https://blandmanstudios.medium.com/tutorial-the-ultimate-linux-laptop-for-pc-gamers-feat-kvm-and-vfio-dee521850385
- https://www.youtube.com/watch?v=cTNkb-qG0Dc&t=232s
- https://github.com/bayasdev/envycontrol

# 0. After installation:
```bash
sudo dnf update
```

And install NVIDIA drivers:
```bash
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
sudo dnf install akmod-nvidia
sudo dnf install xorg-x11-drv-nvidia-cuda
```

To see what processes are using nvidia card:
```bash
watch -n 1 nvidia-smi
```


Install Envycontrol for easy GPU switching:
```bash
sudo dnf copr enable sunwire/envycontrol
sudo dnf install python3-envycontrol
sudo dnf install polkit
```

Install from Software app:
- GNOME Tweaks
- Extensions
- Chrome
- Virtual Machine Manager

Install KVM/QEMU Virtualization support:
```bash
sudo dnf group install --with-optional virtualization
sudo systemctl start libvirtd
sudo systemctl enable libvirtd
```

Install Win11 in VM following this article:
https://sysguides.com/install-a-windows-11-virtual-machine-on-kvm


To install:
- ZeroTier:
  ```bash
  curl -s https://install.zerotier.com | sudo bash
  ```
- Parsec
- Syncthing
- KVM/Qemu (with running Nvidia gpu)
  Inside Wind11 VM:
  - Inventor
  - Fusion360
  - WinProLadder
  - EasyBuilderPRO

To create Win11 bootable usb:
Link: https://www.youtube.com/watch?v=6db5F9C5p_k
```bash
sudo dnf install gparted
sudo gparted 
```

After installing Windows11 following this:
Link: https://www.youtube.com/watch?v=6UQZ5oQg8XA

install refind for nicer boot menu:
Link: https://www.youtube.com/watch?v=HZd4QodEFhA

- VSCode
- Mail -> Thunderbird ?
- 
