# KCM-Colorful
Change your KDE Plasma's color based on a picture.

## Requirements
* Qt5
* KDE Frameworks 5
* cmake
* extra-cmake-modules

## Build
```
git clone --recursive https://github.com/IsoaSFlus/kcm-colorful.git
cd kcm-colorful
mkdir build
cd ./build
cmake ../
make
sudo make install
#Then set your plasma desktop theme to "Colorful" for best experience.
```

## Installation
### Archlinux (AUR)
```
yaourt -S kcm-colorful-git # or any other aur helper
```
Thanks for [@VOID001](https://github.com/VOID001)'s work.

## Screenshots
![a](https://raw.githubusercontent.com/IsoaSFlus/kcm-colorful/master/screenshots/a.png)
![b](https://raw.githubusercontent.com/IsoaSFlus/kcm-colorful/master/screenshots/b.png)

## TODO
- [x] Implement CLI helper
- [x] Port color extraction code to C++
- [ ] Implement KCM
- [ ] Improve color selection by ML

## Postscript
This project is very prototype yet. It has a cli helper now. **Usage**:
```
Usage: kcmcolorfulhelper [options]
Helper for kcm-colorful.
Project address: https://github.com/IsoaSFlus/kcm-colorful

Options:
  -h, --help                  Displays this help.
  -p, --picture <file>        Picture to extract color.
  -c, --color <colorcode>     Set color manually, eg: #1234ef.
  -n, --palette-number <int>  Set the number of colors of palette in the first
                              color extraction. Valid number is between 1 to 16,
                              default is 8.
  -s, --set-as-wallpaper      Set picture specified by "-p" as wallpaper.
```

**If you want to make your KDE look like the screenshots above, just follow these steps.**

First，open KDE's systemsettings->Desktop Behavior->Desktop Effects. Find "blur" and enable it(You can set the Blur strength and Noise strength to preferable value). And disable the "Background contrast".

Then，open KDE's systemsettings->Workspace Theme->Desktop Theme, set your desktop theme to “Colorful”.

Third，install [BreezeBlurred](https://github.com/alex47/BreezeBlurred)，this project provide a blurred version of Breeze window decoration. After installation, open KDE's systemsettings->Application Style->Window Decorations. Find the item named "BreezeBlur" and click "Configure BleezeBlur". Disable "Draw window backbround gradient" and set the Opacity(I'll recommend 60%, because it is the same as desktop theme's).

Finally，if your are curious about the dock on the Screenshots，just check out [Latte-Dock](https://github.com/psifidotos/Latte-Dock).
