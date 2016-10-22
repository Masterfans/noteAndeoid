# git笔记

#git 简介
##什么是版本控制系统
> 版本控制透过文档控制,记录程序各个模组的改动,并为每次改动编上编号
## 版本控制系统的分类
### 集中式版本控制系统,典型代表 SNV
> 集中式版本控制系统: 版本库是集中存放在中央服务器的,而且工作的时候,用的都是自己的电脑,所以,
> 要先从中央服务器中取得最新的版本,然后在开始工作,工作完后, 把自己的版本库推送给中央服务器,中
> 央服务器好比一个图书馆,一要一本书,就必须先从图书馆解借出来,然后改完后,在放回图书馆,集中式版
> 本控制必须要联网才能工作,速度还受网络限制
### 分布式版本控制系统, 典型代表 git
> 分布式版本控制系统根本就没有"中央服务器",每个人的电脑上都有一个完整的版本库,这样,在工作的时候,就不需要联网,因为版本库就在自己的电脑上, 每个人的电脑上都有一个完整的版本库,那么多人如何协作呢? 比方只需要把各自的修改推送给对方,就可以相互看到对方修改的文件
> Linus 1991年创建了开源的Linux

#git环境配置
> suto apt-get install git linux安装git
> git config --global user.name "Your Name"
>
> git config --global user.emaill "emaill@example.com"

##创建版本库
> 版本库: 又叫仓库,repository,可以简单的理解为一个目录,这个目录里面的所有文件都可以被Git管理起来
> mkdir test 创建一个版本库 test为版本库的名字
> cd test 进入test目录
> git init 把该目录变成Git可以管理的仓库(空的仓库empty Git repository) 即在test目录下面生成一个.git的文件夹
> git add readme.md 添加readme.md文件
#Git的设计哲学
> 在使用git command的时候, 没有消息就是最好的消息



> 1. git add readme.txt 添加readme文件到仓库
> 2. git commit -m "wrote a readme file" 提交代码 "提交内容",
	git commit 命令 : -m 后面是本次提交说明 (注:提交是提交到本地仓库,并不是远程服务器)
> 3. 查询git仓库状态, git status 显示本地仓库和远程仓库的区别 ,提示working directory clean 代表本地和远程是完全一致的, 工作目录是干净的
> 4. git diff 查看具体修改了那些内容 ; git diff 就是difference

##版本回退
> 回到上一次修改的版本 git log 查看历史记录 显示历史提交记录
> q 键退出git log 
> git log --pretty==oneline 把日志排列显示
> ##测试
> git reset --hard HEAD^ 回退到上一个版本
>#^ 是键盘上的6666666
> git reflog 显示每一条git的记录 可以回退到删除以前的状态
> cat readme.md 查看文件
##昨晚加了一些文字说明,早上使用git diff 和git status的时候,竟然提示仓库是干净的,不需要提交,于是就有了这个,那就在提交一次吧

> 一天没摸了,快忘了,敲点什么记录一下,
> git 命令好像要在根目录使用,要不会提交错误
###配置git命令 D:/program files (x86)
##2016.10.22
> mkdir name 穿件文件夹
> git add 
> git commit
> git diff
> git status
> git branch 查看当前的分支
> git branch a 新建 a 分支
> git init
> git checkout a 切换到啊分支
> git checkout -b test 新建test分支,并且换回去
> git branch -d a 删除 a 分支
> git branch -D a 强制删除,不管没有没有, 没有提交的代码
> git tag tagv.1 创建 tagv.1这个版本,
> git checkout tagv.1 切换到tagv.1

#SSH
> SSH是一种网络协议 ,用于计算机之间的加密传输


## branch分支

## merge
> git merge a 把a分支的内容合并到当前分支
##关联仓库
> git remote add origin git@github.com:Masterfans/test.git
> 添加一个远程的仓库,地址为git@github.com:Masterfans/test.git
> origin是仓库的名字, 可以随便起名
> git remote -v 查看当前的项目有那些远程仓库
> git pull origin master 
> 默认向github的test目录提交代码,在master分支上
##配置邮箱等信息
> git config --global user.name Masterfans
> git config --global user.email Masterr_Robot@163.com
## alias 别名设置
> 最常用的git command
> git status 
> git commit
> git branch
> git checkout
##配置别名
> git config --global alias.co checkout
> git config --global alias.ci commit
> git config --global alias.st status
> git config --global alias.br branch
##格式化输出
>git log –graph –pretty=format:’%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset’ –abbrev-commit –date=relative 
> git diff <$id1> <$id2>   # 比较两次提交之间的差异
> git diff <branch1>..<branch2> # 在两个分支之间比较 
> git diff --staged   # 比较暂存区和版本库差异


##注销了以前的github账号
> 今天发现我的账号竟然是15年年底注册的,,,,,略感颓废啊,,,,现在才了解git





