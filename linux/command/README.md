# 命令

## 包管理

区别

| 工具\说明 | |
| --- | --- |
| dpkg | 只能安装包，不会安装相应的依赖（Debian 系统最早推出的包管理工具） |
| apt-get / apt-cache | 在 dpkg 基础上实现的可自动安装依赖的包管理工具 |
| aptitude | 对比 apt-get，aptitude 更加指南，并且提供了交互界面 |
| apt | 简化了 apt-get，apt-cache 等命令  |

用法

| 工具\功能 | 查找 | 查看 | 安装 | 更新 | 升级 | 删除 |
| --- | --- | --- | --- | --- | --- | --- |
| dpkg | `dpkg -l | grep xxx` | `dpkg -L xxx` / `dpkg -s xxx` | `dpkg -i /path/to/file` | - | - | `dpkg -r package_name` |
| apt-get / apt-cache | `apt-cache search xxx` | `apt-cache show xxx` / `apt-cache policy xxx` / `apt-cache depends xxx` / `apt-cache rdepends` | `apt-get install xxx` | `apt-get update` | `apt-get upgrade` / `apt-get dist-upgrade` | `apt-get remove package` / `apt-get autoremove` |
| aptitude | `aptitude search xxx` | `aptitude show xxx` | `aptitude install xxx` | `aptitude update` | `aptitude upgrade` / `aptitude full-upgrade` | `aptitude remove` |
| apt | `apt search xxx` | `apt show xxx` | `apt install xxx` | `apt update` | `apt upgrade` | `apt remove xxx`

参考文献

- [What is the difference between dpkg and aptitude/apt-get?](https://askubuntu.com/questions/309113/what-is-the-difference-between-dpkg-and-aptitude-apt-get)
- [有多少人用 apt 命令而不是用 apt-get 命令的？](https://www.v2ex.com/t/357932)

### dpkg

### aptitude

- aptitude update
