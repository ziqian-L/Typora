[Git教程 - 廖雪峰的官方网站 (liaoxuefeng.com)](https://www.liaoxuefeng.com/wiki/896043488029600)

### 设置用户名和邮箱

~~~
设置/修改邮箱
git config --global user.email "email"

设置/修改用户名
git config --global user.name "name"

查看邮箱地址
git config user.email

查看用户名
git config user.name
~~~

##创建版本库

首先选择一个文件夹，右键，选择Git Bash Here，打开命令行界面

~~~
创建一个版本库
git init

取消对这个文件夹的git初始化
rm -rf .git
~~~

将文件夹添加到缓存区，添加到缓存区后才能提交到仓库

~~~
将文件夹添加到缓存区
git add file

提交到仓库
git commit -m ""
~~~

### 版本回退

~~~
如果git status告诉你有文件被修改过，用git diff可以查看修改内容。

查看提交历史
git log
git log --pretty=oneline

版本回退
回退到上一个版本
git reset --hard HEAD^
git reset --hard 版本号

HEAD指向的版本就是当前的版本

查看命令历史
git reflog
~~~

### 工作区和暂存区

![git-repo](https://www.liaoxuefeng.com/files/attachments/919020037470528/0)

### 管理修改

> 第一步，对readme.txt做一个修改
>
> 然后，添加
>
> ~~~
> git add file
> ~~~
>
> 然后，再修改
>
> 提交
>
> ~~~
> git commit -m ""
> ~~~
>
> 此时git status发现第二次的修改没有提交

当使用`git add`命令后，在工作区的第一次修改被放入暂存区，准备提交，但是，在工作区的第二次修改并没有放入暂存区，所以，`git commit`只负责把暂存区的修改提交了，也就是第一次的修改被提交了，第二次的修改不会被提交。

提交后，用`git diff HEAD -- readme.txt`命令可以查看工作区和版本库里面最新版本的区别

那怎么提交第二次修改呢？你可以继续`git add`再`git commit`，也可以别着急提交第一次修改，先`git add`第二次修改，再`git commit`，就相当于把两次修改合并后一块提交了：

第一次修改 -> `git add` -> 第二次修改 -> `git add` -> `git commit`

### 撤销修改

~~~
丢弃工作区的修改
git restore -- file

丢弃暂存区的修改
git restore --staged file
~~~

### 删除文件

删除在版本库中的文件

~~~
删除文件管理器中的文件
rm file 或直接在文件管理器中删除

如果要恢复，使用以下指令
git restore -- file
该指令其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”

如果要彻底删除
git rm file
再git commit -m “”
~~~

`rm`命令就是在工作区删文件
`git rm`就是删文件，并且把删文件的修改提交到暂存区
相当于`rm`删文件后，`git addd`提交，保存修改

##远程仓库

~~~
创建SSH key
$ ssh-keygen -t rsa -C "ziqian303030@163.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/ziqian/.ssh/id_rsa):
Created directory '/c/Users/ziqian/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/ziqian/.ssh/id_rsa
Your public key has been saved in /c/Users/ziqian/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:OD/l0FJbJ7Oca6CnTxYar1KAh6A9kmYpjeD3WqATtsk ziqian303030@163.com
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|. .              |
|o*.. o    . + .  |
|*B+oo o. o + *   |
|*.*.o.o.S * +    |
| E   o o.X o .   |
|  . o  .= * o    |
|   .  .  B .     |
|       .o..      |
+----[SHA256]-----+

查看SSH公钥
cd ~/.ssh
cat id_rsa.puh
~~~

将创建的SSH key添加到github/gitee中

### 添加远程库：先有本地库，后有远程库的时候，如何关联远程库

在github/gitee中创建一个空仓库：learngit

然后我们需要将本地仓库关联到远程仓库

使用

~~~
git remote add shortname url
~~~

其中的shortname是远程库的名字，这个名字并不在本地仓库和远程仓库出现，而是作为文件推送时的标识，这样git才知道你想将文件推送到哪个远程仓库
例如，我在github有两个仓库
一个是学习用的，名字叫learngit，我给它的shortname是learn。如果我要将本地仓库关联到它，代码为：

~~~
git remote add learn git@github.com:ziqian-L/learngit.git
~~~

另一个是我写的项目代码，名字叫code，我给它的shortname是code。如果我要将本地仓库关联到它，代码为：

~~~
git remote add code git@github.com:ziqian-L/code.git
~~~

这两行代码最后的尾巴是创建时提供的

在本地运行`git remote add origin git@github.com:ziqian-L/learngit.git`，将本地仓库关联到github
如果是gitee，运行`git remote add gitee git@gitee.com:ziqian_null/learngit.git`

可以用`ssh -T git@github.com`测试本地密钥与GitHub公钥配对是否成功

如果在`ssh -T git@github.com`时出现了问题，可以参考[SSH连接GitHub提示ssh: connect to host github.com port 22: Bad file number](https://blog.csdn.net/cekiasoo/article/details/53055838)

最后，运行`git push -u origin master`或`git push -u gitee master`将文件推送到远程仓库

从现在起，只要本地作了提交，就可以通过命令`git push origin master`把本地`master`分支的最新修改推送至GitHub
如果是gitee可以通过命令`git push gitee master`

~~~
查看远程库信息
git remote -v

解除了本地和远程的绑定关系，例如origin。注：这没有物理上删除远程库。远程库本身并没有任何改动。要真正删除远程库，需要登录到GitHub，在后台页面找到删除按钮再删除。
git remote rm origin
~~~

>要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；
>
>关联一个远程库时必须给远程库指定一个名字，`origin`是默认习惯命名；
>
>关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容；
>
>此后，每次本地提交后，只要有必要，就可以使用命令`git push origin master`推送最新修改；

### 从远程库克隆：从零开发，最好的方式是先创建远程库，然后从远程库克隆

创建一个新的仓库，名字叫`gitskills`

勾选`Initialize this repository with a README`下面的`Add a README file`，这样GitHub会自动为我们创建一个`README.md`文件

用命令`git clone`克隆一个本地库：

~~~
git clone git@github.com:ziqian-L/gitskill.git
~~~

>要克隆一个仓库，首先必须知道仓库的地址，然后使用`git clone`命令克隆。
>
>Git支持多种协议，包括`https`，但`ssh`协议速度最快

##分支管理

### 创建和合并分支

~~~
创建并切换dev分支
git checkout -b dev或者git switch -c dev
该命令等同于：git branch dev 、git checkout dev这两条命令

查看当前分支
git branch

切换回master分支
git checkout master或者git switch master

合并制定分支到当前分支
即处于master时，使用以下命令可以使dev合并到master
git merge dev

删除分支git branch -d dev


~~~

>查看分支：`git branch`
>
>创建分支：`git branch <name>`
>
>切换分支：`git checkout <name>`或者`git switch <name>`
>
>创建+切换分支：`git checkout -b <name>`或者`git switch -c <name>`
>
>合并某分支到当前分支：`git merge <name>`
>
>删除分支：`git branch -d <name>`

### 解决冲突

>当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。
>
>解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交。
>
>用`git log --graph`命令可以看到分支合并图。
>
>`git log --graph --pretty=oneline --abbrev-commit`也可以看到分支合并图

### 分支管理策略

通常，合并分支时，如果可能，Git会用`Fast forward`模式，但这种模式下，删除分支后，会丢掉分支信息。

如果要强制禁用`Fast forward`模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息。

准备合并`dev`分支，请注意`--no-ff`参数，表示禁用`Fast forward`：

```
$ git merge --no-ff -m "merge with no-ff" dev
Merge made by the 'recursive' strategy.
 readme.txt | 1 +
 1 file changed, 1 insertion(+)
```

因为本次合并要创建一个新的commit，所以加上`-m`参数，把commit描述写进去。

在实际开发中，我们应该按照几个基本原则进行分支管理：

首先，`master`分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面干活；

那在哪干活呢？干活都在`dev`分支上，也就是说，`dev`分支是不稳定的，到某个时候，比如1.0版本发布时，再把`dev`分支合并到`master`上，在`master`分支发布1.0版本；

你和你的小伙伴们每个人都在`dev`分支上干活，每个人都有自己的分支，时不时地往`dev`分支上合并就可以了。

所以，团队合作的分支看起来就像这样：

![git-br-policy](https://www.liaoxuefeng.com/files/attachments/919023260793600/0)

>Git分支十分强大，在团队开发中应该充分应用。
>
>合并分支时，加上`--no-ff`参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而`fast forward`合并就看不出来曾经做过合并。

### Bug分支

用`git stash list`命令看工作现场存到哪去了

工作现场还在，Git把stash内容存在某个地方了，但是需要恢复一下，有两个办法：

一是用`git stash apply`恢复，但是恢复后，stash内容并不删除，你需要用`git stash drop`来删除；

另一种方式是用`git stash pop`，恢复的同时把stash内容也删了

你可以多次stash，恢复的时候，先用`git stash list`查看，然后恢复指定的stash，用命令：

```
git stash apply stash@{0}
```

>修复bug时，我们会通过创建新的bug分支进行修复，然后合并，最后删除；
>
>当手头工作没有完成时，先把工作现场`git stash`一下，然后去修复bug，修复后，再`git stash pop`，回到工作现场；
>
>在master分支上修复的bug，想要合并到当前dev分支，可以用`git cherry-pick <commit>`命令，把bug提交的修改“复制”到当前分支，避免重复劳动。

### Feature分支

>开发一个新feature，最好新建一个分支；
>
>如果要丢弃一个没有被合并过的分支，可以通过`git branch -D <name>`强行删除。

### 多人协作

因此，多人协作的工作模式通常是这样：

1. 首先，可以试图用`git push origin <branch-name>`推送自己的修改；
2. 如果推送失败，则因为远程分支比你的本地更新，需要先用`git pull`试图合并；
3. 如果合并有冲突，则解决冲突，并在本地提交；
4. 没有冲突或者解决掉冲突后，再用`git push origin <branch-name>`推送就能成功！

如果`git pull`提示`no tracking information`，则说明本地分支和远程分支的链接关系没有创建，用命令`git branch --set-upstream-to <branch-name> origin/<branch-name>`。

这就是多人协作的工作模式，一旦熟悉了，就非常简单。

 >- 查看远程库信息，使用`git remote -v`；
 >- 本地新建的分支如果不推送到远程，对其他人就是不可见的；
 >- 从本地推送分支，使用`git push origin branch-name`，如果推送失败，先用`git pull`抓取远程的新提交；
 >- 在本地创建和远程分支对应的分支，使用`git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致；
 >- 建立本地分支和远程分支的关联，使用`git branch --set-upstream branch-name origin/branch-name`；
 >- 从远程抓取分支，使用`git pull`，如果有冲突，要先处理冲突。

### Rebase

- rebase操作可以把本地未push的分叉提交历史整理成直线；
- rebase的目的是使得我们在查看历史提交的变化时更容易，因为分叉的提交需要三方对比。

## 标签管理

