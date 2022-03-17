
# readme

# 多仓库的使用

1. [原始仓库](https://github.com/go-admin-team/go-admin.git) 用于同步更新 原始的 bug等等，分支为 默认的 master
2. [新仓库地址](https://github.com/penglonghua/go-admin.git) 用于定制开发，分支版本为 cloudcms.
3. 使用时，务必跟之前的 master 不冲突，新建文件等等。不修改原始文件.


## 多仓库建立

1. 拉起原始仓库
```shell
git clone https://github.com/go-admin-team/go-admin.git

```

2. 定制分支 cloudcms
```shell
git checkout -b cloudcms

Switched to a new branch 'cloudcms'
```

3. 新建多个远程仓库

先提前建一个空的远程仓库

并命名为  cmsorigin
```shell

git remote add cmsorigin https://github.com/penglonghua/go-admin.git

```

现在本地的就有
```shell
git remote -v
cmsorigin       https://github.com/penglonghua/go-admin.git (fetch)
cmsorigin       https://github.com/penglonghua/go-admin.git (push)
origin  https://github.com/go-admin-team/go-admin.git (fetch)
origin  https://github.com/go-admin-team/go-admin.git (push)

```

***


# 如何合并分支

比如 原始分支 master 有bug修复等等后.需要同步到 cloudcms上.

1. 更新 原始分支 master
```shell
git pull https://github.com/go-admin-team/go-admin.git

```

2. 切换到 要合并的分支上，这里就是  cloudcms
```shell
git checkout cloudcms
```

3. 执行合并分支操作

```shell
git merge master 

```

可以检查到 分支合并更新了.

# 如何推送某个分支到某个仓库

推送本地的 到 新建 远程分支上.

```shell

git push -u cmsorigin master
git push -u cmsorigin cloudcms

```

有默认推送的 ，所以这个地方 必须指明, 不能默认操作.


***


还有后续