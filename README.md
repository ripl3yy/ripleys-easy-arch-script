
# Ripley's Script Hub

Hello! Welcome to my script hub! This is a personal project of mine that I created to upload the various bash scripts that I've created and or are working on.

I am very new to bash scripting and Linux in general, so if my code is messy, I do apologize! I'm still learning and figuring things out! But, I can assure you that the scripts do work as intended!

## Ripley's Easy Arch Script

**This isn't a script to install Arch entirely**, this is just something that installs my daily programs from pacman and Flatpak, installs and sets up the [Starship](https://starship.rs/) prompt, and downloads all of my wallpapers for me.

If you're interested in what packages and Flatpaks are installed, you can [check them here](https://github.com/ripl3yy/ripleys-script-hub/blob/main/package%20list/InstalledPkgs.md). If you install the Flatpaks before installing flatpak itself via pacman, they won't show up until you restart your system.

If the pacman installer fails, you might need to have the `multilib` repo enabled. You can follow this guide [here](https://wiki.archlinux.org/title/Official_repositories#Enabling_multilib).

⚠️ A quick note for those running GNOME, installing Discover **will** install various other KDE applications. To avoid this, please open the script in Text Editor (Gnome's default text editor) and remove `discover packagekit-qt5` from the script. (you can find them easily by doing `Ctrl + F` then typing in the package names)

## Ripley's Easy Drivers

This is still a **major** work in progress. But, in it's current state, it is working and does install accordingly. I tried to make it as user-friendly as possible with support for those on AMD/Nvidia cards on either Debian, Arch, OpenSUSE Tumbleweed, and Fedora.

**For AMD users on Fedora: the amdgpu driver is shipped by default and is maintained by Red Hat. If you are wanting to install the drivers which is maintained by AMD instead of Red Hat, you can find a .rpm on [the AMD website](https://www.amd.com/en/support/download/linux-drivers.html). Make sure to select 'RHEL x86 64-bit'. From there, open terminal and enter `cd ~/Downloads/` then enter `sudo dnf install (file name)` Tip: you can hit tab after typing in the first 3 or 4 letters and it will autocomplete.**

**For Nvidia users on Fedora: Nvidia did NOT make [38 branch drivers](https://developer.download.nvidia.com/compute/cuda/repos/). If you are still on Fedora 38, I strongly urge you to upgrade to Fedora 39 using either Discover or Gnome Software (depending on your DE) before installing drivers.**

If there are any errors in which packages to install, please **submit a pull request!** Everything I had pulled from for everything was either the [Installing Drivers guide from the Lutris team](https://github.com/lutris/docs/blob/master/InstallingDrivers.md) or the wiki pages for their respective distro.

## Before you run the script(s):
### ℹ️ If you're running the driver script, replace `script.sh` with `install_drivers.sh`!

### Make sure you have git installed (auto-skipped if already installed)
#### *This is respective of an Arch-based system. Please install git through your respective package manager (apt, dnf, zypper, etc.).*

```bash
  sudo pacman -S --needed git
```

### Clone this repository

```bash
  git clone https://github.com/ripl3yy/ripleys-script-hub
```

### cd into the folder

```bash
  cd ripleys-script-hub/
```

### Make the script executable

```bash
  sudo chmod u+x script.sh
```

```bash
  ./script.sh
```
