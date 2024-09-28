# Risk: The Game of Global Domination (1996) (Unofficial) (Flatpak)
## Installing
- Install the Wine Flatpak and the mono/gecko extensions (This Flatpak uses them as a base)
```console
flatpak install flathub org.winehq.Wine
```
- Install the GameScope Flatpak (This Flatpak uses it to launch the game)
```console
flatpak install flathub org.freedesktop.Platform.VulkanLayer.gamescope
```
- Download Risk.flatpak from releases
- Install Risk.flatpak (sudo needed for installing single use Flatpak bundle)
```console
sudo flatpak install Risk.flatpak
```
## Launching
- Launch the Risk Flatpak (Either search for the app in your menu and click it) or
```console
flatpak run com.hasbro.Risk
```
## Uninstalling
- Remove Risk Flatpak
```console
flatpak remove com.hasbro.Risk
```
## Downloading/Cloning this repo
- Click the green button to download zip and extract once downloaded or clone repo with
```console
git clone --recurse-submodules https://github.com/ChrisHobday/com.hasbro.Risk
```
## Building
- Install Flatpak builder
```console
flatpak install flathub org.flatpak.Builder
```
- Install the platform this Flatpak will be using
```console
flatpak install flathub org.freedesktop.Platform//23.08 org.freedesktop.Sdk//23.08
```
- Build the Flatpak with Flatpak Builder (Run this from within the com.hasbro.Risk directory)
```console
flatpak run org.flatpak.Builder --force-clean --repo=repo build-dir com.hasbro.Risk.yml
```
## User installation while building
- Replace last Building step with
```console
flatpak run org.flatpak.Builder --force-clean --repo=repo --user --install build-dir com.hasbro.Risk.yml
```
## Building single use Flatpak bundle like in the releases (After having followed the Building steps above)
- Build the Flatpak bundle (Run this from within the com.hasbro.Risk directory after having followed the Building steps above)
```console
flatpak build-bundle repo Risk.flatpak com.hasbro.Risk
```
## Troubleshooting
- Check if Flatpak is installed
```console
flatpak list | grep Risk
```
- Enter Flatpak in command line mode
```console
flatpak run --command=sh com.hasbro.Risk
```
## Flatpak locations
- Installation directory             = /var/lib/flatpak/app/com.hasbro.Risk/
- Installation directory (User mode) = ~/.local/share/flatpak/app/com.hasbro.Risk/
- User cache directory               = ~/.var/app/com.hasbro.Risk/cache/
- User config directory              = ~/.var/app/com.hasbro.Risk/config/
- User data directory                = ~/.var/app/com.hasbro.Risk/data/
- Wine prefix                        = ~/.var/app/com.hasbro.Risk/data/WinePrefix