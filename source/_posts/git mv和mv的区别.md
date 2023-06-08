---
title: git mv 和 mv 的区别
date: 2023-3-02 13:23:05
category: Git
tags: [Git]
---
`git mv`的执行过程：

1. 创建一个和之前文件内容一样的文件，文件名为新的文件名

2. 将原来的文件删除

3. 将删除的文件添加到暂存区

4. 将新建的文件添加到暂存区

   ```bash
   test on master
   ❯ git mv 2.txt 22.txt
   
   test on master [»]
   ❯ git status
   On branch master
   Changes to be committed:
     (use "git restore --staged <file>..." to unstage)
           renamed:    2.txt -> 22.txt
   ```

`mv`的执行过程：只是重命名了一个文件。

但是 git 识别文件变动为：

1. 创建一个和之前文件内容一样的文件，文件名为新的文件名
2. 将原来的文件删除

```bash
test on master
❯ mv 3.txt 33.txt

test on master [✘?]
❯ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    3.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        33.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

**结论：**`git mv`和`mv`的区别就是`mv`最后没有把工作区的文件添加到暂存区。