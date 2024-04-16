# Aregression

[![Open Source Love png1](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://opensource.org/) [![Gitmoji](https://img.shields.io/badge/gitmoji-%20😎-FFDD67.svg)](https://gitmoji.dev/) [![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/iesdevs/iedc/pulls)

A sleek boot-up progress bar for Arch Linux

![preview](preview.gif)

## Installing

Follow instructions on ArchWiki to install and setup [Plymouth](https://wiki.archlinux.org/title/plymouth).

🙌 **Manual**

```bash
# Clone this repository:
$ git clone https://github.com/joe733/plymouth-theme-aregression.git aregression

# You should see aregression listed
$ sudo plymouth-set-default-theme -l

# Change plymouth theme
$ sudo plymouth-set-default-theme -R aregression
```

🐧 **AUR**

```bash
➜ yay -S plymouth-theme-aregression
```

## Removal

🐧 **AUR**

```bash
# Perform manual removal after this
$ yay -Rs plymouth-theme-aregression
```

🙌 **Manual**

```bash
# Dangerous command! Double check your directory/path
$ sudo rm -rf /usr/share/plymouth/themes/aregression
```

## Troubleshooting

- Double check if you've followed the steps mentioned in the [ArchWiki](https://wiki.archlinux.org/title/plymouth) to install Plymouth
- It's known that lower screen resolution has scaling issue. For now it works well with `1920 x 1080` displays. I'm working on it.
- Try using installing a grub theme, and see if any graphic driver is causing resolution issues. Related: <https://askubuntu.com/questions/362722/how-to-fix-plymouth-splash-screen-in-all-ubuntu-releases/>
- Does your grub file contains this line `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"`?
- If nothing works create an [issue](https://github.com/joe733/plymouth-theme-aregression/issues).

## Credits

- Original project [Darwin Plymouth Theme](https://www.gnome-look.org/content/show.php/Darwin+Plymouth?content=170649)
- Derived from [ubuntu-darwin](https://github.com/ashutoshgngwr/ubuntu-darwin)
- Inspired by [arch-beat](https://github.com/nenad/arch-beat) and [arch10](https://github.com/manilarome/plymouth-theme-arch10)
