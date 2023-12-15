# Checkout

 *chekctou* 命令用于检出提交记录中的文件，但它最常使用的是分支的切换。当我们直接使用 *git chekcout branch*的时候，我们就实现了分支的切换，但从commit的角度来看，也是实现了指定 *commit* 的检出，因为在 *git* 中，分支名是一个不同于当前分支的 *commit* 的简称。其实，*git*实际执行的也是*git checkout commit*。

如果我们需要只检出某次提交的单个文件，我们可以使用下面的命令：

```shell
git checkout commit -- file_name
```

通过上面的命令，我们就可以把历史提交中文件检出了。如果我们想要从某个分支检出指定的文件，把上面的 *commit* 修改为 分支名称就好了。
