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

To install:
- Parsec
- Syncthing
- KVM/Qemu (with running Nvidia gpu)
  Inside Wind11 VM:
  - Inventor
  - Fusion360
  - WinProLadder
  - EasyBuilderPRO
 
- VSCode
- Mail -> Thunderbird ?
- 
