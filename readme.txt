mkdir "directoryname"
cd "directoryname"
git init

create a file i.e example.txt
put this file in the "directoryname"(or subdirectories of this directory)

git add example.txt
git commit -m "something you want say"

Why do we need add and commit instead of just add?
because commit can commit many files so you can add different files many times.

ls:View all files in the current directory.

git status: check repository status

git diff "fileName":Check the revisions of the last and this time

git log:查看历史修改记录

HEAD:当前版本

HEAD^:上个版本 ^/1:一个版本 ^^/2

git reset --hard HEAD^:回退至上版本




