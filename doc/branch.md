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

***

## 分支的合并等等


 新建本地分支
 ```shell
 git branch dev-xxx
 
 ```

 切换到新建分支
 ```shell

 git checkout dev-xxx
 ```

 新建分支并切换到新分支上
 
 ```shell

 git checkout -b dev-xxx
 ```


推送某个分支:

```shell

git push origin dex-xxx

```

如何切换到某个分支:

git checkout dev-xxx
git chekcout master



***

多个仓库下 某个分支的处理:
比如 这个地方 想要拉起 某个仓库下的某个分支:

```shell
 git branch -a                                          
* main
  remotes/comorigin/main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main

```

本地并没有显示出 远程的所有分支:

现在同步一下:
```shell

git remote -v
comorigin       http://192.168.125.151:3000/penglonghua/cloudcms-new.git (fetch)
comorigin       http://192.168.125.151:3000/penglonghua/cloudcms-new.git (push)
origin  https://github.com/penglonghua/cloudcms-new.git (fetch)
origin  https://github.com/penglonghua/cloudcms-new.git (push)

同步一下 远程的某个分支
git fetch comorigin

同步后
 git branch -a      
* main
  remotes/comorigin/liubo/202206
  remotes/comorigin/main
  remotes/comorigin/yueluo-dev
  remotes/origin/HEAD -> origin/main
  remotes/origin/main



```

现在就可以 检出某个分支了:
```shell
git checkout -b yueluo-dev remotes/comorigin/yueluo-dev
```



***


> https://www.jianshu.com/p/4b95058088c2

1. 查询本地分支
```shell
git brance
```

2. 查看远程分支
```shell
git branch -r
```

3. 查看所有分支
```shell
git branch -a
```

4. 本地创建新的分支
```shell
git branch [branch name]
```

5. 切换到新的分支
```shell
git checkout [branch name]
```

6. 创建+切换分支
```shell
git checkout -b [branch name]
```

7. 将新分支推送到github
```shell
git push origin [branch name]
```

8. 删除本地分支
```shell
git branch -d [branch name]
```

9. 删除github 远程分支
```shell
git push origin :[branch name]
```

`分支名前的冒号代表删除。`











