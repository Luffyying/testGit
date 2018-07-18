# testGit
it is just a practice of git command


# modify the content of commit
git log --search for your choice
git rebase -i version --choice the version which is before what you want
edit:reword version info
modify:xxxx
esc :wq
git push 


# merge more than one commit
# merge to rear

git rebase -i version --choice the version which is before what you want
example:
p first commit 9090999
s second commit 9093999 
s third commit 6790999 
s fourth commit 8890999
now let we merge the following commit sqush on the first commit

esc :wq
esc :wq
git push 

