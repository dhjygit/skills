-  `sudo nvim /etc/pacman.conf` 

  ```shell
  [archlinuxcn]
  # The Chinese Arch Linux communities packages.
  SigLevel = Optional TrustAll
  Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch
  ```

* `sudo pacman -S archlinuxcn-keyring`
* `sudo pacman -Syyu`

