# firstgithuborigin



wsl2  ubuntu22.04 Git 不用fast

## 1. 快速入门

### 1.1 创建仓库

  新建项目文件夹，在文件夹中执行`git init`，出现.git的子目录

### 1.2 从远程仓库clone现有的

  ``git clone [url]``也可以自定义本地仓库名字``git clone [url] dirName``

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

``git branch test

- 切换到 `test` 分支

``git checkout test``

也可以合并上面俩步，`git checkout -b feature_x`。

- 切换到 master 分支

``git checkout master``

- 合并分支 （可能有冲突）

``git merge test``

- 把新建的分支删掉

``git branch -d test``

- 另外，也可以把分支推送到远程仓库 `git push <远程主机名> <本地分支名>:<远程分支名>`

``git push origin test:test``
