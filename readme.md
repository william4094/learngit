# Git分布式版本控制系统 base on C


## Git安装：
	Debian&Ubuntu：$sudo apt-get install git
	Mac OS：homebrew、Xcode  
	Windows：下载安装文件（建议镜像）
$ git config --global user.name "Your Name"  
$ git config --global user.email "email@example.com"

## 创建版本库：  
#mkdir 创建子文件夹 后可跟 -命令  
$ mkdir learngit  
$ cd learngit  
#pwd 显示当前目录  
$ pwd  
#cat 查看文件内容  
$ cat <file>  

## 仓库初始化：  
#将当前目录建成一个仓库  
$ git init  
(ls -ah #查看隐藏文件)  

文件格式：建议UTF-8 二进制文件无法跟踪改动  

## 将文件添加进仓库：  
$ git add <file>  
#可add多个文件  
#commit 可一次提交所有已add的文件  
#-m 后加文件修改说明  
$ git commit -m <message>  

## 查看仓库状态：  
$ git status  


## 历史记录  
$ git log  
#简单信息输出  
$ git log --pretty=oneline  
#commit_id (版本号)由SHA1计算，16进制表示  
 
## 版本回退  
$ git reset --hard <commit_id[4]>  
#<commit_id[4]>/HEAD^/HEAD~1  
#查看HEAD更改日志  
$git reflow  
#强制推送到远程分支（远程回滚）  
 git push -f origin master

## 取消工作区修改  
#直接丢弃工作区修改  
$ git checkout -- <file>  
#取消暂存区的add  
$ git reset HEAD <file>  

## 删除文件  
#本地删除  
$ rm <file>  
#版本库删除 删除目录 rm -r  
$ git rm <filename>  
$ git commit -m <message>  

## 推送到GitHub  
#添加本地.ssh/id_isa.pub至GitHub  
$ ssh-keygen -t rsa -C "youremail@example.com"  
#关联远程库  
$ git remote add origin git@github.com:<GitHub_Name>/<repo_Name>.git  
#首次同步时使用 -u 将本地与github的master关联，简化后续推送命令  
$ git push -u origin master  
#以后可使下面简化命令  
$ git push origin master  

## 从GitHub克隆库  
#ssh协议(速度更快)  
$ git clone git@github.com:<GitHub_Name>/<repo_Name>.git  
#https协议  
$ git clone https://github.com/<GitHub_Name>/<repo_Name>.git  
#20231029
