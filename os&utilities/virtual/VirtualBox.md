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

## 最佳实践

### 禁用 Window 分享通过 `\\127.0.0.1` 访问 Virtual Box 共享文件

1. 禁用 Window 共享服务 “Server”
2. 启用和关闭 SMB 1.0/CIFS 共享文件服务

    只启用 SMB 1.0/CIFS 客户端
3. 重启系统，检查共享文件端口号

    ```bash
    $ netstat -an | findstr :445
    ```

4. 配置虚拟机映射端口号 445，并启动虚拟机的共享文件服务
5. 资源管理器访问 `\\127.0.0.1`，然后映射驱动盘符

参考 [快速关闭Windows 445 端口的方法| 淡水网志](https://www.restran.net/2017/05/13/windows-stop-445-port/)。
