# archlinux
My set of archlinux install scripts

## Manjaro

Installation date: 2020-01-09

1. Download [Manjaro XFCE](https://manjaro.org/download/#xfce)
2. Install
    - livecd root password = manjaro
    - en-US
    - Install to existing partition (prev Windows)
    - Install FreeOffice
    - User `arthur`
3. Boot
    - connect wifi
4. Manjaro Hello
    - update mirrors `sudo pacman-mirrors --geoip && sudo pacman -Syyu`
    - choose and install applications*
5. Copy .ssh to new home
    - clone this repo
6. Settings manager
    - [Mouse and touchpad] -> [Touchpad] -> [Tap touchpad to click]
    - [Mouse and touchpad] -> [Buttons and feedback] -> [Reverse scroll direction]
    - [Keyboard] -> [Layout] -> [Add Russian]
    - [Keyboard] -> [Layout] -> [Change layout option] -> Alt+Shift
7. pacman-manager
    - install Telegram Desktop
        - ttf-opensans
    - docker
        - `systemctl enable --now docker`
        - `sudo usermod -aG docker $USER`
    - docker-compose
    - go
    - freerdp
8. bauh (Suggestions)
    - google-chrome (aur)
    - Zoom (Flatpak)
    - Discord
9. Log in
    - Telegram
    - Chrome (enter passphrase)
        - Sign in 1Password (find secret key)
        - YouTube lelpas
10. Manjaro Settings Manager
    - [Time and Date] -> [Set time and date automatically]
    - [Locale Settings] -> [English] -> [Set as default display and format]
11. Git config
    - `git config --global user.email "petuhovskiy@yandex.ru"`
    - `git config --global user.name "Arthur Petukhovsky"`
12. bauh (AUR)
    - golangci-lint-bin
13. Install wireguard
    - Install
        - linux54-headers (linux-headers)
        - dkms
        - wireguard-dkms
        - wireguard-tools
    - `modprobe wireguard`
    - Create config /tmp/name.conf
    - `nmcli connection import type wireguard file name.conf`
    - `nmcli connection up nmcli`
    - `nmcli connection`
14. Enable nvidia card
    - Open Manjaro Settings Manager
    - Auto install proprietary driver
    - Reboot
15. Build Clickhouse
    - install cmake, ninja, python
    - `git clone --recursive --branch master https://github.com/ClickHouse/ClickHouse.git`
    - https://clickhouse.yandex/docs/en/development/build/#build-clickhouse
16. Add OpenVPN
    - `sudo nmcli connection import type openvpn file client.conf`
17. Enable swap
    - `sudo fallocate -l 8G /swapfile`
    - `sudo mkswap /swapfile`
    - `sudo chmod u=rw,go= /swapfile`
    - `sudo swapon /swapfile`
    - `sudo bash -c "echo /swapfile none swap defaults 0 0 >> /etc/fstab"`


## Manjaro VM Fun

Installation date: 2020-01-19

1. Download [Manjaro XFCE](https://manjaro.org/download/#xfce)
2. Install
    - livecd root password = manjaro
    - en-US
    - Erase disk
    - Install FreeOffice
    - User `arthur`
3. Boot
    - [Media] -> [DVD] -> [Eject]
4. Manjaro Hello
    - [Launch at start] = false
    - update mirrors `sudo pacman-mirrors --geoip && sudo pacman -Syyu`
    - choose and install applications*
5. ssh
    - `systemctl enable --now sshd`
    - copy .ssh to new home
    - 
5. Copy .ssh to new home
    - clone this repo
6. Settings manager
    - [Mouse and touchpad] -> [Touchpad] -> [Tap touchpad to click]
    - [Mouse and touchpad] -> [Buttons and feedback] -> [Reverse scroll direction]
    - [Keyboard] -> [Layout] -> [Add Russian]
    - [Keyboard] -> [Layout] -> [Change layout option] -> Alt+Shift
7. pacman-manager
    - install Telegram Desktop
        - ttf-opensans
    - docker
        - `systemctl enable --now docker`
        - `sudo usermod -aG docker $USER`
    - docker-compose
    - go
    - freerdp
8. bauh (Suggestions)
    - google-chrome (aur)
    - Zoom (Flatpak)
    - Discord
9. Log in
    - Telegram
    - Chrome (enter passphrase)
        - Sign in 1Password (find secret key)
        - YouTube lelpas
10. Manjaro Settings Manager
    - [Time and Date] -> [Set time and date automatically]
    - [Locale Settings] -> [English] -> [Set as default display and format]
11. Git config
    - `git config --global user.email "petuhovskiy@yandex.ru"`
    - `git config --global user.name "Arthur Petukhovsky"`
12. bauh (AUR)
    - golangci-lint-bin
13. Install wireguard
    - Install
        - linux54-headers (linux-headers)
        - dkms
        - wireguard-dkms
        - wireguard-tools
    - `modprobe wireguard`
    - Create config /tmp/name.conf
    - `nmcli connection import type wireguard file name.conf`
    - `nmcli connection up nmcli`
    - `nmcli connection`
14. Enable nvidia card
    - Open Manjaro Settings Manager
    - Auto install proprietary driver
    - Reboot
15. Build Clickhouse
    - install cmake, ninja, python
    - `git clone --recursive --branch master https://github.com/ClickHouse/ClickHouse.git`
    - https://clickhouse.yandex/docs/en/development/build/#build-clickhouse
16. Add OpenVPN
    - `sudo nmcli connection import type openvpn file client.conf`
17. Enable swap
    - `sudo fallocate -l 8G /swapfile`
    - `sudo mkswap /swapfile`
    - `sudo chmod u=rw,go= /swapfile`
    - `sudo swapon /swapfile`
    - `sudo bash -c "echo /swapfile none swap defaults 0 0 >> /etc/fstab"`