# Git 使用说明

## 介绍

此项目使用Git进行版本控制。Git是一个分布式版本控制系统，旨在处理从小型到大型项目的所有内容，并以速度和效率著称。本文件将指导您如何克隆、提交、更改、推送和拉取项目代码。

## 安装Git

首先，请确保您已在计算机上安装了Git。如果未安装，请访问[Git官网](https://git-scm.com/)下载并安装适合您操作系统的版本。

### Windows

下载并运行安装程序，按照默认设置安装。

### MacOS

使用Homebrew安装：

```bash
brew install git
```

### Linux

在Debian/Ubuntu系统上：

```bash
sudo apt-get install git
```

在Fedora系统上：

```bash
sudo dnf install git
```

## 配置Git

在首次使用Git之前，您需要配置您的用户名和电子邮件地址。这些信息会包含在每个提交中。

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## 基本使用

### 克隆仓库

要开始使用此项目，首先需要克隆仓库。在命令行终端中运行以下命令：

```bash
git clone https://github.com/username/repository.git
```

将`username`替换为您的GitHub用户名，并将`repository`替换为仓库名称。

### 创建分支

在进行任何更改之前，建议您创建一个新的分支：

```bash
git checkout -b feature-branch
```

将`feature-branch`替换为您新分支的名称。

### 查看分支

您可以使用以下命令查看所有分支：

```bash
git branch
```

### 切换分支

要切换到其他分支，使用以下命令：

```bash
git checkout branch-name
```

将`branch-name`替换为目标分支的名称。

### 添加更改

在对文件进行更改后，可以通过以下命令添加这些更改：

```bash
git add .
```

这将添加所有更改的文件。您也可以添加单个文件：

```bash
git add filename
```

将`filename`替换为文件的名称。

### 提交更改

接着，提交更改：

```bash
git commit -m "描述您的更改"
```

请将`描述您的更改`替换为对更改的简短描述。

### 查看提交日志

您可以查看提交历史记录：

```bash
git log
```

### 推送更改

将更改推送到远程仓库：

```bash
git push origin feature-branch
```

### 拉取最新更改

在开始新的工作之前，确保您的仓库是最新的：

```bash
git pull origin main
```

### 合并分支

在完成工作后，可以将您的分支合并回主分支：

```bash
git checkout main
git merge feature-branch
```

### 解决冲突

在合并分支时，如果出现冲突，Git会提示您。手动解决这些冲突后，添加解决后的文件并重新提交：

```bash
git add .
git commit -m "解决冲突"
```
### git常见命令
1.初始化工作区: git init
2.查看当前工作区的代码文件状态：git status
3.将工作区的代码文件提交到暂存区：git add 文件名
4.将暂存区的代码文件提交到本地仓库：git commit -m '提交信息'
5.差异化比较：
    1）工作区和暂存区：git diff 文件名
    2）暂存区和本地仓库：git diff --cached 文件名
    3）工作区和本地仓库: git diff HEAD 文件名
6.版本回退：回退哪个版本
       1）回退到上一个版本(即提交位置):git reset --hard HEAD^
       2)回退到指定版本：git reset --hard 版本号
7.查看提交日志：
       1）git log/git reflog(特点是查看的提交版本号比较短)
8.撤销工作区：git checkout 文件名
9.将代码从暂存区撤销到工作区：git reset HEAD 文件名
10.分支：
        1）创建分支：git branch 分支名
        2）查看分支：git branch
        3)切换分支：git checkout 分支名
        4）合并分支（如果将其他分支合并到master主分支上。那么需要切换到master上）：git merge 分支名
        5）删除分支：git branch -d 分支名