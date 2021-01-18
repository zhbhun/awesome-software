# [Zsh](http://www.zsh.org/)

## 安装配置

- [Installing ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- [Oh My Zsh](https://ohmyz.sh/)

## 基础教程

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
    ```

### 使用技巧

参考文献

- [zsh+on-my-zsh配置教程指南（程序员必备）【已备份】](https://segmentfault.com/a/1190000013612471)
- [用 zsh 提高生产力的 5 个技巧](https://linux.cn/article-10047-1.html)

### 目录快捷跳转

- 在当前目录下输入 .. 或 ... ，或直接输入当前目录名都可以跳转，你甚至不再需要输入 cd 命令了。
- 目录浏览和跳转：输入 d，即可列出你在这个会话里访问的目录列表，输入列表前的序号，即可直接跳转。
- 在你知道路径的情况下，比如 /usr/local/bin 你可以输入 cd /u/l/b 然后按进行补全快速输入。
- 智能跳转，安装了 autojump 之后，zsh 会自动记录你访问过的目录，通过“j + 目录名”可以直接进行目录跳转，而且目录名支持模糊匹配和自动补全，例如你访问过 hadoop-1.0.0 目录，输入 j hado 即可正确跳转。j --stat 可以看你的历史路径库。

### 自动补全

- 连按两次 Tab 会列出所有的补全列表并直接开始选择，补全项可以使用 ctrl + n/p/f/b 上下左右切换
- 命令选项补全，在zsh中只需要键入 tar -<tab> 就会列出所有的选项和帮助说明
- 命令参数补全。键入 kill <tab> 就会列出所有的进程名和对应的进程号

### 命令历史记录

一旦在 shell 敲入正确命令并能执行后，shell 就会存储你所敲入命令的历史记录（存放在 `~/.zsh_history` 文件中），方便再次运行之前的命令。

- 可以按方向键 ↑ 和 ↓ 来查看之前执行过的命令。
- 可以用 r 来执行上一条命令
- 使用 ctrl-r 来搜索命令历史记录
- 更智能的历史命令，在用或者方向上键查找历史命令时，zsh 支持限制查找。比如，输入 ls ,然后再按方向上键，则只会查找用过的 ls 命令。而此时使用则会仍然按之前的方式查找，忽略 ls。

### 命令别名

可以简化命令输入，在 `.zshrc` 中添加 `alias shortcut='this is the origin command'` 一行就相当于添加了别名。在命令行中输入 alias 可以查看所有的命令别名。 

## 进阶使用

### 共享 Shell 配置

如果原来使用的 bash，需要继承原有的环境变量等配置，可以将原有的配置提取到一个独立的文件中，然后在 `.bashrc` 和 `.zshrc` 末尾加上 `source .xxxrc`。

- [解决OSX使用oh-my-zsh后.bash_profile自定义失效](http://to-u.xyz/2016/08/07/zsh-bash/)

## 常见问题

### 安装 NVM

拷贝 `.bashrc` 的 nvm 配置到 `.zshrc` 即可。

- [How to run “nvm” in “oh my zsh”?](https://stackoverflow.com/questions/47009776/how-to-run-nvm-in-oh-my-zsh)
- https://github.com/lukechilds/zsh-nvm

## 参考文献

- [oh-my-zsh：Github 上排名第 1 的程序员生产力工具](https://github.com/showcases/productivity-tools?s=stars)
