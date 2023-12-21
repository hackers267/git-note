# 使用技巧

## 让`gitui`等记住你的密码

```bash
git config --global credential.helper store
```

使用以上命令,可以让`gitui`等记住你的密码。

## 仓库太大，使用`git clone`无法下载或下载用时太长

当我们使用`git clone`克隆仓库的时候，如果仓库太大，下载时间会很长。在这个时候，我们可以使用`git clone --depth 1 --branch main https://github.com/user/repo`来加速。

- depth 1 只克隆最近一次的提交
- branch main 只克隆main分支内容

## 设置 _git_ 初始化仓库时的默认分支

如果想要在初始化仓库的时候修改默认分支 _master_ 为 _main_ ，可以使用下面的命令

```shell
git config --global init.defaultBranch main
```
