# readme

关于分支:

1. 查询一个仓库有哪些分支:包含远程分支

```shell
git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/nft
  remotes/origin/v1.1.0
  remotes/origin/v1.2

```

2.  切换到远程分支

git checkout -b [本地分支名nft]  [远程分支名 remotes/origin/nft]

```shell
git checkout -b nft remotes/origin/nft
Branch 'nft' set up to track remote branch 'nft' from 'origin'.
Switched to a new branch 'nft'

```

* 查询当前分支
```shell
git branch 
  master
* nft

```

* 我现在已经在  `nft`分支上了,如何推送到 远程的 nft上?


暂时待定...



```shell

```



* 如何把 master 分支修改名字为 main分支:

 先查看一下 原先的分支:
```shell
git branch 
* master

```

后修改为 main的.
```shell
git branch -M main

git branch        
* main

```

***

