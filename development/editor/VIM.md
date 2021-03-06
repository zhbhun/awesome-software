# VIM

- https://github.com/vim-awesome/vim-awesome
- https://github.com/akrawchyk/awesome-vim
- [Vim 从入门到精通](https://github.com/wsdjeg/vim-galore-zh_cn#vim-%E9%85%8D%E7%BD%AE%E9%9B%86%E5%90%88)
- https://linhaorong.top/blog/vim/
- https://github.com/yangyangwithgnu/use_vim_as_ide

## 快捷键

![vim-cn.gif](./assets/vim-cn.gif)

- [VIM Cheet Sheet](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/tools/vim.txt)

### 模式切换

- Insert：`i`
- Noraml：`ESC` 
- Command：`:`
- Visual：`v`

### 光标定位

- 上下左右

    - 向左移动一格：`h`
    - 向下移动一行：`j`
    - 向上移动一行：`k`
    - 向又移动一格：`l`

- 行定位

    - 到当前行开头：`0`
    - 到当前行第一个非空字符：`^`
    - 到当前行末尾：`$`
    - 到当前行最后一个非空字符：`g_`
    - 到第一行：`gg`
    - 到最后一行：`G`
    - 到第几行：`ngg` / `nG`

- 词汇定位

    - 到下一个单词的开头：`w`
    - 到下一单词的结尾：`e`
    - 到下一个空格分隔字符串的开头：`W`
    - 到下一个空格分隔字符串的结尾：`E`
    - 到前一个单词的开头：`b`
    - 到前一个空格分隔字符串的开头：`B`
    - 到与当前光标匹配的下一个单词：`*`
    - 当与当前光标匹配的前一个单词：`#`
    - 到与当前光标所在括号相对应的另一半：`%`

### 插入操作

- 光标后插入：`a`
- 光标前插入：`i`
- 当前行之后插入新行：`o`
- 当前行之前插入新行：`O`

### 查找与替换

- [在 Vim 中优雅地查找和替换](https://harttle.land/2016/08/08/vim-search-in-file.html)

#### 查找

在 normal 模式下按下 `/` 即可进入查找模式，输入要查找的字符串并按下回车。Vim 会跳转到第一个匹配，按下 n 查找下一个，按下 N 查找上一个。

Vim 查找支持正则表达式，例如 `/vim$` 匹配行尾的 "vim"。需要查找特殊字符需要转义，例如 `/vim\$` 匹配 "vim$"。

- 查找：`/foo`

    在 normal 模式下按下 `/` 即可进入查找模式，输入要查找的字符串并按下回车。Vim 会跳转到第一个匹配，按下 n 查找下一个，按下 N 查找上一个。

- 正则匹配：`/vim$`

    Vim 查找支持正则表达式，例如 `/vim$` 匹配行尾的 "vim"。需要查找特殊字符需要转义，例如 `/vim\$` 匹配 "vim$"。

- 大小写敏感查找：`/foo\C`
- 大小写不敏感查找：`/foo\c`
- 查找当前词

    - 查找光标所在单词匹配的单词：`*`
    - 查找光标所在单词匹配的字符序列：`g*`

#### 替换

```
:{作用范围}s/{目标}/{替换}/{替换标志}
```

- 替换当前行：`:s/foo/bar/g`
- 替换全文：`:%s/foo/bar/g`
- 替换选区：`:'<,'>s/foo/bar/g`

    在 Visual 模式下选择区域后输入 `:`，Vim 即可自动补全为 `:'<,'>`。

- 替换指定行

    - 5-21 行：`:5,12s/foo/bar/g`
    - 当前行与接下来两行：`:.,+2s/foo/bar/g`

其他标志

- g：全部替换
- i: 大小写不敏感
- I：大小写敏感
- c：需要确认

    回车后 Vim 会将光标移动到每一次匹配字符出现的位置，并提示：`replace with bar (y/n/a/q/l/^E/^Y)?`，按下 y 表示替换，n 表示不替换，a 表示替换所有，q 表示退出查找模式，l 表示替换当前位置并退出。

### 选区 & 拷贝 & 粘贴 & 删除

- 选区

    - 自由选择；normal -> v -> 移动光标
    - 行选择：normal -> V -> 上下移动光标

- 拷贝

    - 拷贝当前行及其后面一行：`y`
    - 拷贝当前行：`yy`
    - 拷贝多行：`nyy`
    - 从光标位置开始拷贝至当前单词的结尾：`ye`
    - 从光标位置开始拷贝至下一单词的开头：`yw`
    - 从光标位置开始拷贝至当前单词的开头：`yb`
    - 从光标位置开始拷贝至行尾：`y$`
    - 从光标位置开始拷贝至行首：`y0`
    - 选区拷贝：选区 -> `p`

- 粘贴

    - 光标之后粘贴：`p`
    - 光标之前粘贴：`P`

- 删除

    - 剪切当前行：`dd`
    - 剪切多行：`ndd`
    - 从光标位置开始剪切至当前单词的结尾：`de`
    - 从光标位置开始剪切至下一单词的开头：`dw`
    - 从光标位置开始剪切至上一单词的开头：`db`
    - 从光标位置开始剪切至行尾：`d$`
    - 从光标位置开始剪切至行首：`d0`
    - 剪切光标位置所在字符：`x`

### 撤销 & 取消撤销

- 撤销：`u`
- 取消撤销：`ctrl+r`

### 多行编辑

- [Vim下多行同时编辑与删除技巧](https://www.jianshu.com/p/50d5b6cfd73b)
- [技巧：Vim 的纵向编辑模式](https://www.ibm.com/developerworks/cn/linux/l-cn-vimcolumn/index.html)

### 其他

- 重复命令：`.`
- 缩进：`<<` / `>>`

## 常见问题

### 撤销与回退操作

- [vim 撤销 回退操作](https://blog.csdn.net/xiongzhengxiang/article/details/7206691)
- [handleKeys is not overriding VS Code Ctrl+R and Ctrl+F shortcuts](https://github.com/VSCodeVim/Vim/issues/3501)

## 配置

- https://spacevim.org/cn/
- [vimrc](https://github.com/amix/vimrc)
- https://spacevim.org/
- https://github.com/liangxianzhe/oh-my-vim
- https://github.com/mhinz/vim-galore
- https://github.com/yangyangwithgnu/use_vim_as_ide
- [Vim 配置入门](http://www.ruanyifeng.com/blog/2018/09/vimrc.html)
- [可能是 Windows 下最漂亮的 Gvim 配置了](https://keelii.com/2016/06/13/awsome-window-vimrc/)

### 包管理

- https://github.com/tpope/vim-pathogen
- https://github.com/VundleVim/Vundle.vim
- https://github.com/junegunn/vim-plug
- https://github.com/egalpin/apt-vim

### 主题

- [solarized](https://github.com/altercation/solarized)
- [dracula-theme](https://github.com/dracula/dracula-theme)

### 插件

- https://vimawesome.com/
- [Vundle.vim](https://github.com/VundleVim/Vundle.vim)
- [YouCompleteMe](https://github.com/ycm-core/YouCompleteMe)
- [fzf](https://github.com/junegunn/fzf)
