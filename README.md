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




