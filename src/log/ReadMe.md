# 日志(历史)

## 只查看单独某个文件的修改历史

如果有需要单独查看某个文件的提交记录，可以使用下面的命令：
```shell
git log filename
```

在单独查看想个文件的提交记录的时候，如果还想查看每次变化的内容，可以使用下面的命令：
```shell
git log -p filename
```

## 在查看时，同时显示文件名

如何在使用`git log`时需要同时显示对应的文件名，我们只需要使用`--name-only`选项即可。如

```shell
git log --name-only
```

如何同时需要查看文件状态，那么可以使用`--name-status`选项。如

```shell
git log --name-status
```

同时我们也可以结合其它的选项来使用这两个命令，如下:

```shell
git log --name-only --oneline
git log --name-status --oneline
```
