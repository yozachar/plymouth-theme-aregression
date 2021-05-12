# Aregression

[![Open Source Love png1](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://opensource.org/) [![Gitmoji](https://img.shields.io/badge/gitmoji-%20😎-FFDD67.svg)](https://gitmoji.dev/) [![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/iesdevs/iedc/pulls)

A sleek boot-up progress bar for Arch Linux

![preview](preview.gif)

## Installing

Follow instruction on [ArchWiki](https://wiki.archlinux.org/title/plymouth) to install and setup Plymouth.

### AUR

```bash
➜ yay -S plymouth-theme-aregression
```

### Manual

- Clone this repository:

    ```bash
    ➜ sudo git clone https://github.com/joe733/aregression /usr/share/plymouth/themes/aregression
    ```

### Usage

This is well documented in the same ArchWiki page. Nevertheless you can execute the following commands:

- List all themes

    ```bash
    ➜ sudo plymouth-set-default-theme -l               # You should see aregression listed
    ```

- Change theme test theme

    ```bash
    ➜ sudo plymouth-set-default-theme aregression
    ➜ sudo plymouthd                                   # Start plymouthd
    ➜ sudo plymouth --show-splash                      # Use Ctrl + Alt + F6 to quit
    ➜ sudo plymouth --quit                             # Quit plymouthd
    ```

- If everything is fine update initramfs

    ```bash
    ➜ sudo plymouth-set-default-theme -R aregression
    # OR
    ➜ mkinitcpio -P
    ```

## Removal

### AUR

```bash
yay -Rs plymouth-theme-aregression                     # ⚠️  Perform manual removal after this
```

### Manual

- Remove the theme folder

    ```bash
    ➜ sudo mv /usr/share/plymouth/themes/aregression ~/
    ➜ sudo rm -rf ~/aregression                        # ⚠️  Dangerous command! Double check your directory
    ```

## Credits

- Original project [Darwin Plymouth Theme](https://www.gnome-look.org/content/show.php/Darwin+Plymouth?content=170649)
- Derived from [ubuntu-darwin](https://github.com/ashutoshgngwr/ubuntu-darwin)
- Inspired by [arch-beat](https://github.com/nenad/arch-beat) and [arch10](https://github.com/manilarome/plymouth-theme-arch10)
