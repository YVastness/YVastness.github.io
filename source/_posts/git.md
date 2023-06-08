---
title: Git 增强命令
date: 2022-12-02 13:23:05
category: Git
tags: Git
---
| 命令                                      | 介绍                                                                   |
| ----------------------------------------- | ---------------------------------------------------------------------- |
| git commit -a                             | 参数设置修改文件后不需要执行 git add 命令，直接来提交                  |
| git add -u                                | 表示将已跟踪文件中的修改和删除的文件添加到暂存区，不包括新增加的文件   |
| git status -s                             | 显示短的消息                                                           |
| git restore [--worktree]                  | 删除工作区指定文件最后修改                                             |
| git restore --staged                      | 删除暂存区指定文件最后修改                                             |
| git rm                                    | 将文件从工作区中删除                                                   |
| git rm --cached                           | 把文件从暂存区域移除                                                   |
| git diff                                  | 显示暂存区和工作区的差异                                               |
| git diff --staged                         | 显示暂存区和上一次提交(commit)的差异                                   |
| git diff [first-commit]...[second-commit] | 显示两次提交之间的差异                                                 |
| git mv                                    | 用于移动或重命名一个文件、目录或软连接                                 |
| git log --graph                           | 查看历史中什么时候出现了分支、合并。以下为相同的命令，开启了拓扑图选项 |
| git push -u                               | 第一次提交需要加 -u参数后，后面的提交就直接可以 git push               |
| git branch -r                             |                                                                        |
| git branch -d                             |                                                                        |

1. --cached 和 --staged 是同义词
2. restore 恢复;恢复原状
3. verbose 冗长的;详细信息