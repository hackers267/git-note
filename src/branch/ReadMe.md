# 分支操作

根据远程分支创建分支:

```bash
git check -b dev origin/dev
```

## 删除分支

在使用`git`进行分支操作的时候，不仅仅需要创建新的分支，在一些分支不再需要的时候，还需要对分支进行删除。

删除本地分支：
```shell
git branch -d localBranchName
git push origin --delete remoteBranchName
```

需要注意的是，如果你删除的是你所在的分支，Git是不允许的。这个时候，你需要使用`git checkout otherBranchName`
切换到其他分支。然后再进行删除操作。

如果你要删除的分支中有还没有推送或合并的内容，那么`git branch -d`也是不会删除分支的。这个时候，你有两个选择：

- 把没有推送/合并的分支进行推送/合并
- 使用`git branch -D`进行强制删除

删除远程分支使用`git push origin --delete remoteBranchName`命令。其有一个简短的命令形式：

```shell
git push <remote> :<branch>
```
请注意命令中在远程名称和分支之间的`:`。

如果在删除远程分支时报错，可以先使用下面的命令同步分支：
```shell
git fetch -p
```