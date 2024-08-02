# Git 命令大全

## 配置

- `git config --global user.name "Your Name"`  
  设置全局用户名

- `git config --global user.email "your.email@example.com"`  
  设置全局用户邮箱

- `git config --list`  
  查看当前的Git配置

## 仓库操作

- `git init`  
  初始化一个新的 Git 仓库

- `git clone <repository>`  
  克隆一个远程仓库到本地

- `git remote add origin <url>`  
  添加远程仓库

- `git remote -v`  
  查看远程仓库信息

- `git remote remove origin`  
  移除远程仓库

- `git fetch`  
  从远程仓库获取更新但不合并

- `git pull`  
  从远程仓库获取并合并更新

- `git push`  
  将本地分支推送到远程仓库

## 分支操作

- `git branch`  
  列出所有本地分支

- `git branch <branch-name>`  
  创建一个新分支

- `git checkout <branch-name>`  
  切换到指定分支

- `git checkout -b <branch-name>`  
  创建并切换到新分支

- `git merge <branch-name>`  
  合并指定分支到当前分支

- `git branch -d <branch-name>`  
  删除本地分支

- `git branch -D <branch-name>`  
  强制删除本地分支

- `git branch -r`  
  列出所有远程分支

## 提交操作

- `git status`  
  查看工作区和暂存区的状态

- `git add <file>`  
  将文件添加到暂存区

- `git add .`  
  将当前目录下所有更改的文件添加到暂存区

- `git commit -m "commit message"`  
  提交暂存区的更改，并附上提交信息

- `git commit --amend`  
  修改最近一次提交的提交信息或内容

- `git log`  
  查看提交历史记录

- `git log --oneline`  
  以简洁的格式查看提交历史记录

- `git diff`  
  查看工作区和暂存区之间的差异

- `git diff --staged`  
  查看暂存区和最近一次提交之间的差异

## 撤销操作

- `git reset <file>`  
  从暂存区移除文件，但保留工作区的更改

- `git reset --hard`  
  丢弃所有本地更改（慎用）

- `git revert <commit-id>`  
  撤销某次提交的更改，并生成一个新的提交

- `git stash`  
  暂存当前工作区的更改

- `git stash pop`  
  恢复最近一次暂存的更改

- `git stash list`  
  查看所有暂存的更改

## 标签操作

- `git tag`  
  列出所有标签

- `git tag <tag-name>`  
  创建一个新标签

- `git tag -d <tag-name>`  
  删除标签

- `git push origin <tag-name>`  
  推送标签到远程仓库

- `git push --tags`  
  推送所有标签到远程仓库

## 其他常用命令

- `git show <commit-id>`  
  查看指定提交的详细信息

- `git blame <file>`  
  查看文件每一行的最后修改记录

- `git cherry-pick <commit-id>`  
  从其他分支中挑选提交

- `git rebase <branch-name>`  
  将当前分支的更改移到指定分支之上

- `git reflog`  
  查看 Git 操作记录

- `git clean -fd`  
  删除工作区中未跟踪的文件和目录

## 远程操作

- `git push origin <branch-name>`  
  将本地分支推送到远程仓库

- `git pull origin <branch-name>`  
  从远程分支拉取更新并合并

- `git remote update`  
  更新所有远程分支的信息

- `git remote show origin`  
  查看远程仓库的详细信息
