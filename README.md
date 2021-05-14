# Aregression

[![Open Source Love png1](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://opensource.org/) [![Gitmoji](https://img.shields.io/badge/gitmoji-%20😎-FFDD67.svg)](https://gitmoji.dev/) [![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/iesdevs/iedc/pulls)

A sleek boot-up progress bar for Arch Linux

![preview](preview.gif)

## Installing

Follow instructions on ArchWiki to install and setup [Plymouth](https://wiki.archlinux.org/title/plymouth).

🐧 **AUR**

```bash
➜ yay -S plymouth-theme-aregression
```

🙌 **Manual**

- Clone this repository:

    ```bash
    ➜ sudo git clone https://github.com/joe733/aregression /usr/share/plymouth/themes/aregression
    ```

## Usage

This is well documented in the same ArchWiki page. Nevertheless you can execute the following commands:

- List all themes

    ```bash
    ➜ sudo plymouth-set-default-theme -l               # You should see aregression listed
    ```

- Change theme test theme

    ```bash
    ➜ sudo plymouth-set-default-theme aregression
    ➜ sudo plymouthd                                   # Start plymouthd
    ➜ sudo plymouth --show-splash                      # ⚠️ Use Ctrl + Alt + F6 to quit
    ➜ sudo plymouth --quit                             # Quit plymouthd
    ```

- If everything is fine update initramfs

    ```bash
    ➜ sudo plymouth-set-default-theme -R aregression
    # OR
    ➜ mkinitcpio -P
    ```

## Removal

🐧 **AUR**

```bash
yay -Rs plymouth-theme-aregression                     # ⚠️ Perform manual removal after this
```

🙌 **Manual**

- Remove the theme folder

    ```bash
    ➜ sudo mv /usr/share/plymouth/themes/aregression ~/
    ➜ sudo rm -rf ~/aregression                        # ⚠️ Dangerous command! Double check your directory
    ```

## Troubleshooting

- Double check if you've followed the steps mentioned in the [ArchWiki](https://wiki.archlinux.org/title/plymouth) to install Plymouth
- Make sure that your login manager has the Plymouth daemon enabled, see ArchWiki on how to do it.
- It's known that lower screen resolution have scaling issue. For now it works well with 1920 x 1080 displays. I'm working on it.
- Try using installing a grub theme, and see if any graphic driver is causing resolution issues. Related: https://askubuntu.com/questions/362722/how-to-fix-plymouth-splash-screen-in-all-ubuntu-releases
- Does your grub file contains this line `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"`?
- If nothing works create an [issue](https://github.com/joe733/plymouth-theme-aregression/issues).

## Credits

- Original project [Darwin Plymouth Theme](https://www.gnome-look.org/content/show.php/Darwin+Plymouth?content=170649)
- Derived from [ubuntu-darwin](https://github.com/ashutoshgngwr/ubuntu-darwin)
- Inspired by [arch-beat](https://github.com/nenad/arch-beat) and [arch10](https://github.com/manilarome/plymouth-theme-arch10)
