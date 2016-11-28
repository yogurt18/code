# Git
---
## 安装Git
```Git
$ git config --global user.name "Your Name" 
$ git config --global user.email "email@example.com"
$ git config --gobal core.autocrlf false //windows特有问题
```
***
## 创建版本库
```Git
$ mkdir code //创建空目录
$ cd code
$ pwd //显示当前目录
$ git init //把这个目录变成Git可以管理的仓库
$ git add readme.md //把文件添加到仓库
$ git commit -m "wrote a readme file" //把文件提交到仓库
```
### 说明：
> * `-m`后面输入的是本次提交的说明，可以输入任意内容
> * 因为`commit`可以一次提交很多文件，所以你可以多次`add`不同的文件

---
## 版本控制
```Git
$ git status //查看仓库当前状态
$ git diff readme.md //查看具体修改内容
$ git log //显示从最近到最远的提交日志
$ git log --pretty=oneline //显示简略信息
$ git reset --hard HEAD^ //回退到上一个版本
$ git reset --hard commit_id //回退到指定版本
$ git reflog　//查看命令历史
$ cat readme.md //查看当前文本内容
$ git diff HEAD -- readme.md //查看工作区和版本库里面最新版本的区别
$ git checkout -- readme.md 
$ git reset HEAD readme.txt //把暂存区的修改回退到工作区
$ rm readme.md //删除文件
$ git rm test.txt
$ git commit -m "remove test.txt"
```
### 说明：
> * 在Git中，用`HEAD`表示当前版本，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个^比较容易数不过来，所以写成`HEAD~100`。
> * `commit id`没必要写全，前四位就可以了
> * 命令`git checkout -- readme.md`意思就是，把`readme.md`文件在工作区的修改全部撤销，这里有两种情况：
一种是`readme.md`自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是`readme.md`已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
> * fhdi

```Git
```



