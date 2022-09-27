# FirstGithubOrigin



git的常用命令



wsl2  ubuntu22.04 Git 

稳定连接github.com（写在后面）

## 1. 快速入门


### 1.1 创建仓库

  新建项目文件夹，在文件夹中执行`git init`，出现.git的子目录

### 1.2 从远程仓库clone现有的

  ``git clone [url]``也可以自定义本地仓库名字``git clone [url] dirName``

  不用自己手动创建文件夹（自动生成）

## 2. 完整的一次提交流程

### 2.1 进入子目录

``cd  /myProject``

### 2.2 提交到暂存区

``git add .``

### 2.3 提交暂存区修改内容到本地

``git commit -m "添加描述内容"``

### 2.4 推送到远程仓库

``git push``

## 3. 说明

+ 移除文件：``git rm filenme``(从暂存区移除，然后提交)
+ 查看文件状态：``git status``
+ 提交历史：``git log``
+ 只查看某个人提交记录：``git log --author = usr``

### 4. 推送到远程仓库

- 推送到远程仓库：`git push origin master` 推送到远程 `master` 分支
- 如果没有远程仓库，现在想让本地和远程仓库关联， 如下命令添加：`git remote add origin <server>` ,比如我们要让本地的一个仓库和 Github 上创建的一个仓库关联可以这样 `git remote add origin https://github.com/shuangshuangbb/firstgithuborigin`

现在就可以将项目推送到远程仓库了。

### 5.  撤销操作

有时你提交过代码之后，发现一个地方改错了，你下次提交时不想保留上一次的记录；或者你上一次的 `commit` message的描述有误，这时候你可以使用接下来的这个命令：`git commit --amend`。

``git commit --amend``

取消上一步操作，如 `git add` 、 `git commit` 之后。

``git reset filename``

### 6. 分支

分支是用来将特性开发绝缘开来的。在你创建仓库的时候，`master` 是默认的。在其他分支上进行开发，完成后再将它们合并到主分支上。

不同的版本或系统模块并行开发时，我们一般会单独建立一个分支进行开发，最后再合并到主分支。

- 新建本地分支

``git branch test``

- 切换到 `test` 分支

``git checkout test``

也可以合并上面俩步，`git checkout -b feature_x`。

- 切换到 master 分支

``git checkout master``

- 合并分支 （可能有冲突）

``git merge test``

- 把新建的分支删掉

``git branch -d test``

删除远程分支

`git push origin -d release`

- 另外，也可以把分支推送到远程仓库 `git push <远程主机名> <本地分支名>:<远程分支名>`

``git push origin test:test``



### 7. release版本

用`git tag `

`git tag -a v0.0.1 -m "my first tag-release"`

-a 表示标签 -m 后面是描述（可以用日期时间）

用`git tag`查看会出现v0.0.1

用`git show v0.0.1`显示此标签的所有信息

用`git push origin v0.0.1`推送到仓库

`git push origin tag`推送全部




---------------------------------------------

## 1. 利用fastgithub

https://github.com/dotnetcore/FastGithub

fastgithub_linux-x64

可以利用windows下载通过``sudo cd``移动到linux子系统下

在子系统中文件夹内``./fastgithub``运行

**运行之前**

在~/.bashrc最后添加地址和端口

``export http_proxy=127.0.0.1:38457``

``export https_proxy=127.0.0.1:38457``

  添加后``source ~/.bashrc``

  之后运行fastgithub

## 2. 利用微软DNS（不稳定）

**先将``~/.bashrc``中最后的地址#注释掉**

windows更改手动TPC/IPv4代理

4.2.2.1和4.2.2.2



## 3. 身份认证

用`gh auth login`

验证验证码即可进行擦写



## 4. oh-my-zsh

git

定义了有关 git 的 alias常用的有

- gaa = git add --all
- gcmsg = git commit -m
- ga = git add
- gst = git status
- gp = git push



--------------

利用git fls推送大文件

- 当我们下载好git-lfs之后，需要开启/初始化lsf功能：`git lfs install`，之后我们看到`Git LFS initialized.`说明已经初始化完成了！
- 这里推荐2种方式将大型文件添加到lfs管理：
- 文件形式：`git lfs track *.pkl`
- 文件夹形式：`git lsf track model/**`（包含文件夹本身的）；`git lsf track model/*`（不包含文件夹本身的）
- 接下来我们就可以看到在git本地仓库中git给我们构建了一个文件`.gitattributes`
- 查看lfs追踪了哪些文件：`git lfs ls-files`
- 下面就是把新的文件添加到缓存区：`git add .gitattributes`
- 提交缓存区内的文件到本地仓库：`git commit -m "xxxxx"`
- 将本地的大型模型通过git推送到gitlfs中管理：`git push origin master `
