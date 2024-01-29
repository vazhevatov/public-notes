# CREATE SSH KEYS FOR GIT

ssh-keygen -t rsa -C "example@email.com"

# BASIC CONFIGURATION

git config --global user.name “Name Surname”

git config --global user.email “example@email.com”

git config --global core.editor "vim"

git config --global color.diff auto

git config --global color.status auto

git config --list --show-origin

# BASIC COMMANDS

git remote -v

git status

git add **filename**

git commit -m "commit message"

git log

git push

git blame **filename**

git fetch

git merge

git checkout -- **filename**

git checkout .

git clean -xdf

git reset HEAD^^ ==(HEAD~2) ^^ or ~2 = number of the commits==

git reset -- **filename**

# BRANCHING

git branch -b **branch_name** ==create branch branch_name and checkout to this branch==

git branch -d **branch_name** ==delete branch_name==

# DISK USAGE

git rev-list --disk-usage --objects --all
