# Shell

- [Fish shell 入门教程](http://www.ruanyifeng.com/blog/2017/05/fish_shell.html)

## 入门教程

- 查看当前环境的 Shell

    ```shell
    $ echo $SHELL
    ```

- 查看系统安装了哪些 Shell 

    ```shell
    $ cat /etc/shells
    ```

- 修改当前环境的 Shell

    ```shell
    $ chsh -s $(which zsh)
    `
