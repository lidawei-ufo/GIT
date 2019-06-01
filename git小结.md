设置用户名:
git config --global user.name “用户名”;
设置邮箱:
git config --global user.email”邮箱”;
创建版本库
mkdir 文件夹名;
初始化git仓库
git init

git add .
git add -A;添加当前目录的所有变化 添加到缓存区

加入到仓库中
git commit -m “日志” 文件名;
git commit -am 添加缓冲区的全部

删除
git rm 文件

查看仓库状态
git status;

查看本目录的日志
git log 

或者给远程地址设置别名
git remote add  别名   远程地址
然后  git push 别名 master

远程仓库的操作:
查看远程仓库:git remote
查看远程仓库:git remote -v（详细信息：地址）默认origin
删除远程仓库:git remote remove 仓库名          删除的是远程仓库的别名
添加远程仓库:git remote add origin git地址
修改仓库名称:git remote rename 原名 +新名

线上:
git clone 地址;
添加到缓冲区



git pull   拉取获取远程代码
git pull origin master           origin=>远程仓库  master=>分支

git push
设置免密登录(ssh登录)

日志:
git log                    查看日志
git log --pretty=oneline    日志在一行查看
git reflog        查看都干了什么
回退
git reset --hard HEAD^                   HEAD当前指针指向的版本 一般都是指向最新的版本    ^往前几个版本就几个^ 不好切换
git reset --hard +唯一id              切换到哪一个版本

不要轻易修改master 
分支:
查看分支:git branch;
查看全部分支：git branch -a
创建分支：git branch <name>
切换分支：git checkout <name>
创建并切换分支:git checkout  -b 分支名
分支的合并   先切换的主分支master上:git merge 分支名
分支的删除:git branch  -d  分支名
强制删除分支：git branch -D <name>
删除远程分支：git push origin --delete <name>
	          git push origin :<name>





删除远程仓库的http地址： git remote remove 仓库名    
添加ssh地址：git remote add origin （ssh地址）
//ssh地址:ssh-keygen.exe               一直回测
ssh-keygen -t rsa -C "邮箱   hulei@qq.com"     一路回车
去c:/用户/用户名/.ssh/id_rsa.pub 打开
全选复制；
去马云设置ssh公钥、


推送到远程仓库
git push 远程仓库地址   master                      master 主分支
首次推送      git push -u origin master
 
//常用命令
查看某个文件的修改状态
git diff aa.txt

把readme.txt文件在工作区的修改全部撤销
git checkout -- readme.txt

可以把暂存区的修改撤销掉（unstage），重新放回工作区
git reset HEAD 文件名

忽略文件
在Git工作区的根目录下创建一个特殊的.gitignore文件

强制添加该文件
git add -f App.class

查看.gitignore的问题
git check-ignore -v 文件名

配置别名
git config --global alias.st status
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"	
每个仓库的Git配置文件都放在.git/config文件中
[alias]
    co = checkout


git stash
git stash pop






