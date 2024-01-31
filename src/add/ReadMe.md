# Add

`git add` 命令用于把添加内容到索引。

`git add` 命令通常会条体添加现有路径的当前内容，但是通过某些选项，它也可以用于仅添加对工作树文件所有的部分更新或删除工作树中不存在的路径。

*索引* 保存着工作树内容的快照，该快照作为下一次提交的内容。因此，在对工作树进行任何更改之后，以及在运行 `commit` 命令之前，必须使用 `add` 命令将所有新文件或修改过的文件添加到索引中。

`git status` 命令用于获取摘要，说明哪些文化的文件已暂存，准备下一次提交。

## 功能
