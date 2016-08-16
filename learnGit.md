###### 本文根据[廖雪峰教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)整理的笔记

#### 创建版本库 
- 初始化一个Git仓库：git init

- 添加文件到Git仓库：

    1.git add    可反复多次使用，添加多个文件
    
    2.git commit 
#### 版本 b
- 版本回退
 
    1.git reset --hard HEAD^  ：HEAD表示当前版本 两个版本HEAD^， 一百个版本HEAD~100

    2.git reset --hard commit-id

#### 工作区和暂存区
- git add命令实际上就是把要提交的所有修改放到暂存区（Stage），然后，执行git commit就可以一次性把暂存区的所有修改提交到分支

#### 撤销修改
git checkout -- file ： 丢弃工作区的修改

- 修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态
- 已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态

git reset HEAD file

- 回退版本，也可以把暂存区的修改回退到工作区
- HEAD 表示最新版本

#### 远程仓库
- 创建SSH
  1. 创建SSH Key ： ssh-keygen -t rsa -C "youremail@example.com"
  2. 登陆GitHub，打开“Account settings”，点“Add SSH， Key”在Key文本框里粘贴id_rsa.pub
- 添加远程库
  1. 登陆GitHub，创建新的repository
  2. git push -u origin master ： 推送到远程仓库
- 克隆 ：git clone git@github.com:youremail/repository.git

#### 分支管理
- 创建与合并分支
  1. git checkout -b dev ： 创建并切换分支
  2. git add，git commit ： 提交分支
  3. git merge dev ： 合并分支

#### git命令
- git status ：查看状态
- git diff ：若文件被修改，查看修改内容
- git log ： 查看提交历史，以便确定要回退到哪个版本 --pretty=oneline 美化
- git reflog ： 查看命令历史，以便确定要回到未来的哪个版本
- git remote add origin git@github.com:youremail/learngit.git ： 设置远程库的名称
- git branch ：查看分支
- git branch <name> ： 创建分支
- git checkout <name> ： 切换分支
- git merge <name> ： 合并某分支到当前分支
- git branch -d <name> ： 删除分支 


