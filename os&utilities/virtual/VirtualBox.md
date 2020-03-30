# VirtualBox

- [虚拟机VirtualBox怎么添加新的虚拟硬盘](https://blog.csdn.net/love__coder/article/details/8270856)

## Manjaro

常见问题

- 按照增强功能时总是报错：`this system is currently not set up to buile kernel modules`

    ```bash
    # 查看并记录内核版本，例如 5.4.28
    $ sudo uname -a
    # 将查到的内核版本替换下面的 xxx，例如 5.4.28，替换后变为 linux54（忽略小版本号）
    $ sudo pacman -S linux{xxx}
    $ sudo pacman -S linux-headers
    $ sudo pacman -Syyu
    # 重启再次安装增强功能
    ```

    [【Linux】在VirtualBox-6.0中安装Manjaro18.0](https://blog.csdn.net/u010168781/article/details/89854178)

- 不支持调整分辨率

    需要在 VirtualBox 中将虚拟机的显卡控制器调整为 VBoxSVGA，且关闭 3D 加速（否则无法保存），然后启动虚拟机去设置相应的分辨率。

    [Manjaro guest on VirtualBox not able to get the full resolution](https://unix.stackexchange.com/questions/499938/manjaro-guest-on-virtualbox-not-able-to-get-the-full-resolution)
