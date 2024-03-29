
# Ripley's Easy Arch Script (REAS)

Hello! Welcome to my post-install script! This is a personal project of mine that I created to help ease the process of getting my Arch install up and going a little quicker. **This isn't a script to install Arch entirely**, but just something that installs my daily programs from pacman and Flatpak, installs and sets up the [Starship](https://starship.rs/) prompt, and downloads all of my wallpapers for me.

I am very new to bash scripting and Linux in general, so if my code is messy, I do apologize! I'm still learning and figuring things out! But, I can assure you that the script does work as intended!

I've made sure to make this script as easy to customize as possible. I know not everyone uses the exact same set of applications I do, which is why I made it the way it is. Below, I'll leave a list of what is installed. A quick reminder that this script does **NOT** install a web browser. If you're using something arch-based, such as Manjaro, EndeavourOS, etc. then you will already have Firefox preinstalled. If you're running vanilla Arch, a simple `sudo pacman -S firefox` will install Firefox to your system.

For new Arch users, I've left a guide below with the commands needed to run the script. All commands there are just copy and paste!

If the pacman installer fails, you might need to have the `multilib` repo enabled. You can follow this guide [here](https://wiki.archlinux.org/title/Official_repositories#Enabling_multilib).

If there is anything I can do to help improve my script or if there is anything that you think I should add to it, please let me know! Either make a pull request or contact me on Discord (_ripl3y) and I'll get back to you as soon as I can!

⚠️ A quick note for those running GNOME, installing Discover **will** install various other KDE applications. To avoid this, please open the script in Text Editor (Gnome's default text editor) and remove `discover packagekit-qt5` from **lines 47 and 135**. This will save your system from being filled with KDE bloat.

## Info about the driver installer script

*Work in progress! A driver install script will be available soon*

## Packages installed

### Installed via pacman

- Discord
- flatpak-kcm
- Discover (GUI frontend for Flatpak and Arch repos)
- packagekit-qt5
- Flatpak (enables the ability to install Flatpak from terminal)
- Steam
- btop
- neofetch
- xdg-desktop-portal-gtk (allows flatpaks to open links in a browser)
- ffmpegthumbs (video thumbnails in dolphin)
- kdenlive

### Installed via Flatpak

- [Spotify](https://flathub.org/apps/com.spotify.Client)
- [Flatseal](https://flathub.org/apps/com.github.tchx84.Flatseal)
- [Planify](https://flathub.org/apps/io.github.alainm23.planify) (genuinely one of my favorite applications, I highly suggest checking it out)
- [Heroic Games Launcher](https://flathub.org/apps/com.heroicgameslauncher.hgl)
- [Video Downloader](https://flathub.org/apps/com.github.unrud.VideoDownloader)
- [Vinegar](https://flathub.org/apps/org.vinegarhq.Vinegar)
- [ProtonUp-Qt](https://flathub.org/apps/net.davidotek.pupgui2)
- [Motrix](https://flathub.org/apps/net.agalwood.Motrix)
- [OBS Studio](https://flathub.org/apps/com.obsproject.Studio)
- [Minecraft Bedrock Launcher](https://flathub.org/apps/io.mrarm.mcpelauncher)
- [Minecraft Launcher (java)](https://flathub.org/apps/com.mojang.Minecraft)
## Before you run the script:

Make sure you have git installed (automatically skipped if already installed)

```bash
  sudo pacman -S --needed git
```

Clone this repository

```bash
  git clone https://github.com/ripl3yy/ripleys-easy-arch-script
```

cd into the folder

```bash
  cd ripleys-easy-arch-script/
```

Make the script executable (if installing drivers, replace script.sh with drivers.sh)

```bash
  sudo chmod u+x script.sh
```
Run the script! (if using the driver install script, replace script.sh with drivers.sh)

```bash
  ./script.sh
```
