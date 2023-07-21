mkdir "directoryname"
cd "directoryname"
git init

create a file i.e example.txt 创建一个文件
put this file in the "directoryname"(or subdirectories of this directory)
将文件放于文件夹目录或子目录下

git add example.txt //将文件加入暂存区
git commit -m "something you want say" //将暂存区内文件提交



ls:列出当前目录下所有文件

git status: check repository status //查看库状态

git diff "fileName":查看该文件修改记录，在add前使用

git log:查看历史修改记录

HEAD:当前版本

HEAD^:上个版本 ^/~1:一个版本 ^^/~2

git reset --hard HEAD^:回退至上版本

git reset --hard "版本号":回退至指定版本

git reflog：命令历史记录

git restore "filename":把"filename"文件在工作区的修改全部撤销

git reset HEAD "filename":把暂存区（即add后）的修改撤销，重新放回工作区

git rm "filename":删除文件    之后commit,真正删除



本地库推送至远程库
git remote add origin git@github.com:github账户名/本地库名.git

origin:git默认叫法，意为远程库

git push -u origin master //把当前分支master推送至远程库

-u:git不但会把本地的master分支内容推至远程新的master分支，还会把本地的master分支和
远程的master分支相关联，之后无需此参数

git remote -v:查看远程库信息

git remote rm origin:根据名字删除远程库,例如origin

远程库克隆至本地库

git clone git@github.com:github账户名/远程库名.git


branch test

