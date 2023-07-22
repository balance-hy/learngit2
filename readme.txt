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


git branch:查看分支

git branch <name>:创建分支

git switch <name>:切换分支

git merge <name>:合并某分支到当前分支

git branch -d <name>:删除分支 -D:强制删除


合并分支时，如果可能，Git会用Fast forward模式，但这种模式下，删除分支后，会丢掉分支信息
强制禁用Fastforward模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息

git merge --no-ff -m "commit的描述" <branchName>

--no-ff:禁用Fast forward


BUG分支

在dev正在进行工作，需要修复BUG，git stash存储并隐藏当前工作，转移到master，修复后合并
git stash list:查看已存储stash内容

git stash apply <stash@{0}>:恢复指定的存储的内容，但不删除stash内容

git stash drop:删除stash内容

git stash pop:恢复并删除stash内容

在master分支上修复了bug后,这个bug其实在当前dev分支上也存在

git cherry-pick <commit id>:复制一个特定的提交到当前分支


git log --graph --pretty=oneline --abbrev-commit:图表形式显示历史，abbrev：显示前七位commit id

多人协作

首先，可以试图用git push origin <branch-name>推送自己的修改；

如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；

如果合并有冲突，则解决冲突，并在本地提交；

没有冲突或者解决掉冲突后，再用git push origin <branch-name>推送就能成功！

如果git pull提示no tracking information，则说明本地分支和远程分支的链接关系没有创建，用
命令git branch --set-upstream-to=origin/<branch-name> <branch-name> 。


this is a test!

test3.