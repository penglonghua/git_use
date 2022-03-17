
# git 多仓库管理

使用场景

在一个开源的项目上定制自己的版本开发.
因为开源的可能有bug,所以要保持 同步更新, 而自己的定制开发版本也要推送到不同的 版本上.

实际上 这种情况还真会用到.

* 1.多个仓库
* 2.分支的使用和合并.


应该是都会使用到这个.

下面是以 go-admin 为例:



开源项目地址:

https://github.com/go-admin-team/go-admin


有3个分支:

* master
* dev
* 1.3.x



## 开始操作

***

1. clone 原始的git 仓库

```shell

git clone https://github.com/go-admin-team/go-admin.git

```

```shell
git remote -v

origin	https://github.com/go-admin-team/go-admin.git (fetch)
origin	https://github.com/go-admin-team/go-admin.git (push)

```

2. 新建本地分支, 只用于自己的定制项目.

```shell

git checkout -b cloudcms
Switched to a new branch 'cloudcms'

```

现在的分支结构为 

```shell
git branch 
* cloudcms
  master
```

3. 添加远程仓库地址:

因为已经有  origin 仓库地址了, 所以这个地方 新建一个名字,区分一下即可.


```shell

git remote add cmsorigin https://github.com/penglonghua/go-admin.git

git remote -v
cmsorigin       https://github.com/penglonghua/go-admin.git (fetch)
cmsorigin       https://github.com/penglonghua/go-admin.git (push)
origin  https://github.com/go-admin-team/go-admin.git (fetch)
origin  https://github.com/go-admin-team/go-admin.git (push)





```

4. 推送本地的所有分支 到 新建 远程分支上.

```shell

git push -u cmsorigin master
git push -u cmsorigin cloudcms

```

测试一下 查询所有的分支.

```shell
git branch -a
  cloudcms
* master
  remotes/cmsorigin/cloudcms
  remotes/cmsorigin/master
  remotes/origin/1.3.x
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
```

后面约定为 只需要修改,和部署 cloudcms 分支即可.



***

那么现在的问题就剩下了, 如何 合并分支了.

因为 原始的 master 修复 bug 之后,如何 合并到 另外的分支上面.


更新 原始的 master

```shell
git pull https://github.com/go-admin-team/go-admin.git
```

1. 首先 回道 cms 分支上.
```shell
git checkout cms

```
2. 执行合并操作

```shell

git merge master  (同步该分支即可.)

```















如何添加 远程仓库 


```shell

https://github.com/penglonghua/go-admin.git

```


```shell
git remote add myorigin https://github.com/penglonghua/go-admin.git
git branch -M main
git push -u myorigin main
```



