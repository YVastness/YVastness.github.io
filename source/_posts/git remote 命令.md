---
title: git remote 命令
date: 2023-3-03 13:23:05
tags: Git
---
``git remote``命令用于在远程仓库的操作。

显示所有远程仓库：

```bash
git remote -v
```

以下我们先载入远程仓库，然后查看信息：

```bash
$ git clone https://github.com/tianqixin/runoob-git-test  
$ cd runoob-git-test
$ git remote -v  
origin  https://github.com/tianqixin/runoob-git-test (fetch)  
origin  https://github.com/tianqixin/runoob-git-test (push)
```

**origin** 为远程地址的别名。

显示某个远程仓库的信息：

```bash
git remote show [remote]
```

例如：

```bash
$ git remote show https://github.com/tianqixin/runoob-git-test
* remote https://github.com/tianqixin/runoob-git-test
  Fetch URL: https://github.com/tianqixin/runoob-git-test
  Push  URL: https://github.com/tianqixin/runoob-git-test
  HEAD branch: master
  Local ref configured for 'git push':
    master pushes to master (local out of date)
```

添加远程版本库：

```
git remote add [shortname] [url]
```

shortname 为本地的版本库，例如：

```bash
# 提交到 Github
$ git remote add origin git@github.com:tianqixin/runoob-git-test.git
$ git push -u origin master
```

其他相关命令：

```bash
git remote rm name  # 删除远程仓库
git remote rename old_name new_name  # 修改仓库名
```
