# testGit
it is just a practice of git command


# modify the content of commit

git log --search for your choice

git rebase find out the difference

git rebase -i version --choice the version which is before what you want

edit:reword version info

modify:xxxx

esc :wq

git push --hard



# merge more than one commit

# merge to rear

git rebase -i version --choice the version which is before what you want

example:

p first commit 9090999

f second commit 9093999 

f third commit 6790999 

f fourth commit 8890999

now let we merge the following commit merge on the first commit

(the latest item is on the bottom)

esc :wq

(esc :q not edit then quit,this is vim command)

esc :wq

git push --hard 

（merge在有冲突的时候仅需要处理一次，但是rebase要处理多次,且最好是在开发完毕后，使用rebase,不让强推后，造成很多冲突，带来不便利）

# merge use squash

example:

pick first commit 9090999

pick second commit 9093999 

pick third commit 6790999 

s fourth commit 8890999

explain:

let the version 8890999 squash to version 6790999  

# git commit --amend  

modify the commit information,not create the log 

# git checkout --file.text

尚未提交到暂存区的返回修改



# git reset HEAD 

# git checkout --file.text

已经提交到暂存区的返回修改

# git reflog

search for the history of commit 

reflog可以看到HEAD的移动记录，假如之前误删了一个分支，则可通过git reflog看到移动HEAD的哈希值

例如：在ying分支上把luffy分支删除了，执行如下命令，恢复luffy分支

git reflog

找到 748eebf HEAD@{2}:rebase:checkout luffy

git checkout 748eebf

git checkout -b luffy


# git reset

恢复版本到某一个版本
强制 git reset --force version 

# git fetch

get fetch origin master
get latest version from remote branch,but won't auto merge


git command:

1.esc退出编辑状态

2.i  进入编辑状态

3.dd 删除一行

4.u 撤销上一步操作


# git stash

save the current buffer like the stack

场景:本应该在子分支上开发，结果忘记了切分支，在master上开发起来，之前很蠢，拷贝下代码保存，然后还原

git stash

git checkout master

git stash apply(git stash pop)

如上可以帮你解决问题

git stash list 查看所有入栈的buffer

git stash pop 出栈

git stash clear 清空

git log --pretty=oneline  将记录仅显示一行

如果要回滚项目中某一个特定的文件：

git checkout 097799215a -- search/hash_search.js

some common vim command

dd:删除光标所在的那一整行

yy:复制光标所在的行

i:插入：在当前光标所在处插入输入的文字，已存在的字符会向后退

esc:退出编辑模式

:wq 保存并退出

:!wq 强制保存并退出

u 恢复前一个动作



在项目中如果对于文件大小写敏感，配置:git config core.ignorecase false


这样改成了驼峰就能识别改动了。



                            



