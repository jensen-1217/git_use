# Git 高级命令大全

## 进阶命令

- `git rebase -i <commit-id>`  
  以交互模式重新基于指定提交进行变基操作。可以用来修改历史提交。

- `git reflog expire --expire=now --all-ref`  
  清除所有引用日志记录，释放磁盘空间（注意：这个命令会永久删除日志，谨慎使用）。

- `git stash apply <stash@{n}>`  
  应用指定的暂存更改而不删除暂存记录。`<stash@{n}>` 是 `git stash list` 中的索引。

- `git stash drop <stash@{n}>`  
  删除指定的暂存记录。

- `git shortlog`  
  显示简洁的提交日志，按作者和提交数量汇总。

- `git describe --tags`  
  基于最近的标签显示当前提交的描述。

- `git ls-tree <commit-id>`  
  列出指定提交的树对象内容。

- `git diff --name-status`  
  查看文件的状态变化，包括新增、修改、删除。

## 高级命令

- `git filter-branch`  
  对 Git 历史进行大规模重写，例如更改提交信息、删除文件等。用法复杂且可能会重写历史。

- `git commit-tree`  
  使用树对象创建新的提交对象。

- `git submodule`  
  管理子模块，例如将一个 Git 仓库作为另一个仓库的子目录。

- `git worktree`  
  在同一仓库中管理多个工作区（工作树）。

- `git gc`  
  执行垃圾回收，清理和压缩Git仓库中的无用数据。

- `git bundle`  
  创建和操作 Git 包文件，用于传输和备份。

- `git notes`  
  添加、查看或删除提交的附加注释。

- `git log --graph`  
  可视化显示提交历史的图形表示。

- `git log --pretty=format:"%h %s"`  
  自定义显示提交记录的格式。`%h` 表示提交缩略哈希，`%s` 表示提交消息。

- `git cherry`  
  比较当前分支与指定分支，列出尚未合并的提交。

- `git rerere`  
  记录和重用冲突解决方案。启用 `git config --global rerere.enabled true`。

- `git ls-files`  
  列出所有被 Git 跟踪的文件。

- `git grep`  
  搜索 Git 仓库中的文本内容。

## 远程操作进阶

- `git remote prune origin`  
  清理远程仓库中已删除的分支引用。

- `git remote set-url origin <new-url>`  
  修改远程仓库的 URL。

- `git fetch --all`  
  从所有远程仓库拉取更新。

- `git fetch --depth=<n>`  
  仅获取最近的 `n` 次提交，适用于浅克隆。

- `git push --force-with-lease`  
  强制推送，但会先检查远程分支的状态，避免覆盖他人的工作。

- `git remote show <remote-name>`  
  显示远程仓库的详细信息，包括分支和配置。
